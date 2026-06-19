# PROMPT OPERATIVO

## EVIDENZE RICHIESTE

### strategia prompt

zero-shot

### assunzioni

- lo sviluppatore ha un progetto per la gestione dei ticket
- esiste una lista di ticket aperti

### criterio

il prompt dovrebbe dopo aver analizzato il progetto dovrebbe individuare quali file è necessario modificare e come

### verifica

vedere se i file evidenziati dal modello siano coerenti con la richiesta e verificare che le verificare che eventuali modifiche non disturbino il flusso logico

## PROMPT MIGLIORATO

```txt
Analizza la dashboard Ticket e identifica i file da modificare per implementare un empty state quando non ci sono ticket aperti. Non scrivere codice: elenca i file coinvolti, il loro ruolo e il motivo della modifica. Segnala eventuali componenti riutilizzabili.

vincoli:
Non scrivere codice
Non scrivermi la tua chain-of-thought estesa
non controllare le cartelle node-modules
non controllare i file .env e .gitignore
```
