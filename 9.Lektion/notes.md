Teil 1: Theorie (Papier, ohne Hilfsmittel)

1. Mengenlehre (Set Theory in SQL)

    UNION: Vereinigt zwei Ergebnismengen (entfernt Duplikate).

    UNION ALL: Vereinigt zwei Ergebnismengen (behält Duplikate).

    INTERSECT: Nur Datensätze, die in beiden Mengen vorkommen.

    EXCEPT / MINUS: Datensätze, die in der ersten, aber nicht in der zweiten Menge vorkommen.

2. Konsistenz & Referenzielle Integrität

    Konsistenz (Consistency): Der Zustand, in dem die Daten alle definierten Regeln (Constraints) erfüllen.

    Referenzielle Integrität: Stellt sicher, dass Fremdschlüssel immer auf existierende Primärschlüssel verweisen. Keine "Waisen-Einträge".

3. Beziehungs-Constraints

    Primary Key (PK): Eindeutige Identifikation, darf nicht NULL sein.

    Foreign Key (FK): Verweist auf einen PK einer anderen Tabelle.

    Unique: Wert darf nur einmal vorkommen.

    Not Null: Feld darf nicht leer bleiben.

    Check: Überprüft Bedingungen (z.B. Alter >= 18).

4. Aggregatfunktionen

    COUNT(), SUM(), AVG(), MIN(), MAX().

    Wichtig: Werden oft mit GROUP BY verwendet. Filterung nach Aggregation erfolgt mit HAVING, nicht mit WHERE.

5. Bulk-Import & Datensicherung

    Bulk-Import: Schnelles Einlesen großer Datenmengen (z.B. CSV via LOAD DATA INFILE).

    Datensicherung: mysqldump erzeugt ein SQL-Skript (Struktur + Daten).
