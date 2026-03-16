# Warum geht Herbert oft laufen

WGHOL:

## Where

## Group By

## Having

Eine zusätzliche where klausel

## Order By

### Ascending

### Descending

## Limmit

funktioniert nur bei Mysql.
Man kann angeben 1, 100 und dann gibt es nur die datensätze von 0 bis 100.

# Daten aus Datenbank entfernen

Einfach Daten zu löschen ist nicht immer Schlau, zum Beispiel bei einer Bank währe es ja doch wichtig zu wissen was ein Mitarbeiter getan hat obwohl er gekündigt hat. Um das Problem zu lösen könnte man zb. einfach ein boolean Feld hinzufügen und dort einfach is_fired = true;

# Integrität

## Datenintegrität

- Stellt sicher das die Daten korekt sind.

### Eindeutigkeit und Datenkonsistenz

Jeder Datensatz soll eindeutig Identifizierbar sein z. B. durch einer Id.

### Referenzielle Integrität

- Saubere Referenzen.
- Saubere Löschung.
- ON DELETE
- CASCADE

### Datentypen

es sollten immer die passenden Datentypen benutzt werden.
Es ist nicht nur wichtig das es möglich ist mit dem Datentyp sondern auch das es so klein wie möglich ist.

### Datenbeschränkungen

- zb. das ein Datum nur ein spezifische Format möchte
