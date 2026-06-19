# PROMPT OPERATIVO

## EVIDENZE RICHIESTE

### strategia prompt

few-shots

### assunzioni

- lo sviluppatore ha un progetto per la gestione dei ticket
- esiste una lista di ticket aperti
- ha già effettuato una pianificazione

### criterio

il prompt dovrebbe dopo che aver approvato il piano dovrebbe apportare il minor numero di modifiche necessarie affinchè compaia un messaggio in caso di empty state della lista dei ticket attivi

### verifica

verificare se compare il messaggio in caso di empty state e scompare mostrando invece i ticket aperti in caso contrario

## PROMPT MIGLIORATO

```txt
Dopo l'approvazione del piano, modifica solo i file identificati e implementa l'empty state con il minor numero possibile di cambiamenti, senza introdurre refactoring o nuove dipendenze

vincoli:
Prima di scrivere codice, il piano deve essere esplicitamente approvato.
Se il piano non è approvato, indica in modo sintetico cosa non va o cosa è incompleto.
Non includere chain-of-thought estesa: fornisci solo conclusioni e motivazioni brevi.
Escludi dall’analisi node_modules, .env, .gitignore e file generati o di terze parti.
Non proporre modifiche strutturali non necessarie
```
