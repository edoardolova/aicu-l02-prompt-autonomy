# PROMPT OPERATIVO

## EVIDENZE RICHIESTE

### strategia prompt

few-shot

### assunzioni

- lo sviluppatore ha un progetto per la gestione dei ticket
- la ux della dashboard non rispetta i suoi canoni/quelli del cliente (stile più moderno)
- vuole aggiungere come funzionalità i filtri

### criterio

il prompt dovrebbe consentire al modello di eseguire un singolo issue per volta, partirei dall'aggiunta dei filtri e dopo aver verificato il loro funzionamento procedere alla gestione dello stile

### verifica

testare il corretto funzionamento dei filtri e la coerenza con il flow della pagina, verificare visivamente le modifiche apportate allo stile

## PROMPT MIGLIORATO

```txt
Ruolo:
Sei un Senior Frontend Engineer e UX Designer specializzato in React/Next.js

vincoli:
Prima di modificare il codice devi comprendere l'architettura esistente
riutilizza componenti già presenti quando possibile
Non scrivermi la tua chain-of-thought estesa
non controllare le cartelle node-modules
non controllare i file .env e .gitignore
dopo ogni task attendi conferma prima di procedere al successivo

Task 0 - Analisi

Prima di scrivere codice:
individua dove viene renderizzata la dashboard Ticket
individua il componente che renderizza la lista
individua da dove arrivano i dati
individua gli hook utilizzati
individua lo state management
individua eventuali componenti riutilizzabili

Successivamente indica:

file coinvolti
responsabilità
punti da modificare
Non scrivere codice.


Task 1 - Nuovi filtri
Implementa una toolbar moderna sopra la lista.

Aggiungi:
ricerca testuale
stato
data apertura
data chiusura
categoria
cliente
tag

Ogni filtro deve essere:
indipendente
combinabile
sincronizzato con gli altri


Task 2 - Ordinamento
Aggiungi:
Più recenti
Più vecchi
Priorità
Stato
Cliente
Ultimo aggiornamento


Task 3 - Performance
Analizza:
re-render inutili
useMemo
useCallback
memo
lazy loading
virtualizzazione lista se >100 elementi
debounce ricerca
query inutili

Implementa solo ottimizzazioni realmente utili.


Task 4 - Responsive
rendi la toolbar responsive (estesa per desktop e collassata con un bottone toggle per mobile)


Task 5 - Stile
Modernizza la dashboard mantenendo il design system esistente e ispirandoti ai principi di design di Apple (pulizia, semplicità, gerarchia visiva), senza copiarne lo stile.

Rivedi palette colori e contrasto
Uniforma spacing, border radius e shadow
Migliora tipografia e gerarchia visiva
Aggiorna lo stile di card, toolbar, filtri, pulsanti, input, badge e tabelle
Aggiungi micro-animazioni (hover, focus, click, loading) di 150–250 ms
Mantieni design responsive, accessibile e coerente su tutta la dashboard
Riutilizza componenti e variabili di stile esistenti, evitando redesign radicali
Non installare nuove librerie


Task 6 — Pulizia codice
Rimuovi:
codice duplicato
componenti inutilizzati
props inutilizzate
hook ridondanti
```
