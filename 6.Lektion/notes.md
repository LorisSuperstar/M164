# subselect

ein subselect ist eine Abfrage innerhalb einer anderen Abfrage die eine andere Tabelle betrifft.

beispiel:

```
select *
FROM kunden
WHERE fk_ort_postleitzahl IN ( select id_postleitzahl FROM orte WHERE name = 'München');
```

- Das subselect ist immer in Klammern einzuschliessen.
- Achten Sie auf den Operator, mit dem Sie das Ergebnis der Unterabfrage vergleichen: (skalar oder nicht-skalar)
  ![SkalarVSnichtSkalar](image.png)

## Skalare Unterabfrage

- Eine skalare Unterabfrage gibt nur eine Spalte mit nur einer Zeile zurück.
- Wenn man bestimmte operatoren verwendet muss die abfrage Skalar sein. (=, >, >=, < und <=)
- Beispiel:

```
SELECT city_destination, ticket_price, travel_time, transportation FROM one_way_ticket
  WHERE ticket_price < (
      SELECT MIN(ticket_price) FROM one_way_ticket
      WHERE city_destination = 'Bariloche' AND city_origin = 'Paris'
      )
  AND city_origin = 'Paris';

```

- Ergebniss:
  | City_Destination | Ticket_Price | Travel_Time | Transportation |
  | :--- | :--- | :--- | :--- |
  | Bariloche | 830.00 | 11hr 30min | air |

## Nicht-skalare Unterabfrage

- Beispiel:

```
SELECT name, age, country
FROM users
WHERE country IN
(  -- hier beginnt Subquery:
   SELECT name FROM country WHERE region = 'Europa'
)

```

- In diesem Beispiel werden die Namen und Altersangaben von Benutzern aus der Tabelle users abgerufen, die in europäischen Ländern leben.

## Hauptunterschied

- Bei einer skalaren unterabfrage bekommt man nur eine einzige zeile zurück.
