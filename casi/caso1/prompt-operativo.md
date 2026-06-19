# PROMPT OPERATIVO

## EVIDENZE RICHIESTE

### strategia prompt

zero-shot

### assunzioni

- lo sviluppatore ha un progetto per la gestione dei ticket
- la renderizzazione della lista dei ticket avviene ma non sa in quale componente viene gestita.

### criterio

il prompt dovrebbe consentire al modello di capire dove avviene la renderizzazione all'interno del progetto

### verifica

verificare se esiste il file indicato dal modello e se effettivamente contiene la logica e la lista ticket che stavomo cercando

## PROMPT MIGLIORATO

```txt

Analizza il progetto e individua il punto in cui viene renderzzata la lista dei ticket (TicketList)

segui questi passi:
1 Individua il componente o la pagina che mostra la lista dei ticket.
2 Ricostruisci il flusso di navigazione fino a quel componente.
3 Indica quali componenti sono coinvolti nella renderizzazione (parent e child).

Per ogni file rilevante indica il percorso del file

Vincoli
Non modificare file.
Non scrivermi la tua chain-of-thought estesa
non controllare le cartelle node-modules
non controllare i file .env e .gitignore

```
