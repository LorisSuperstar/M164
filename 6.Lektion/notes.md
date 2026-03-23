# subselect

ein subselect ist eine Abfrage innerhalb einer anderen Abfrage die eine andere Tabelle betrifft.

beispiel:

```
select *
FROM kunden
WHERE fk_ort_postleitzahl IN ( select id_postleitzahl FROM orte WHERE name = 'München');
```
