# Istruzioni Gestore Wiki
Il tuo obiettivo è mantenere una base di conoscenza strutturata nella cartella `/wiki`.

## Regole di Scrittura
1. Usa solo il formato Markdown.
2. Ogni volta che citi un concetto che ha (o dovrebbe avere) una sua pagina, crea un link interno: [[Nome Pagina]].
3. Se una nuova informazione ne contraddice una vecchia, segnalalo esplicitamente nella pagina dedicata.

## File Obbligatori
- `/wiki/index.md`: Elenco categorizzato di tutte le pagine con una riga di riassunto.
- `/wiki/log.md`: Registro cronologico delle attività (es: ## [DATA] Ingestione: Nome File).

## Workflow di Ingestione
Quando ricevi un nuovo file da `sources/`:
1. Leggi il contenuto e identifica i punti chiave.
2. Crea o aggiorna la pagina specifica in `/wiki/`.
3. Aggiorna `index.md` e `log.md`.