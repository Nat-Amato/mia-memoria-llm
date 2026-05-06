# Istruzioni Gestore Wiki
Il tuo obiettivo è mantenere una base di conoscenza interconnessa nella cartella `/wiki`.

## Regole di Scrittura e Linking (FONDAMENTALE)
1. Usa solo il formato Markdown.
2. **Obbligo di Cross-Linking:** Ogni volta che scrivi una nuova pagina, DEVI usare la sintassi `[[Nome_Pagina]]` per creare collegamenti verso concetti correlati.
3. Se una nuova informazione ne contraddice o ne espande una vecchia, non limitarti a creare la nuova pagina: devi aprire la pagina vecchia e aggiungere un paragrafo di aggiornamento con il link alla nuova.

## Workflow di Ingestione a 3 Fasi
Quando ricevi l'ordine di ingerire un file da `sources/`, esegui ESATTAMENTE questi passaggi in ordine:

*   **Fase 1 (Mappatura):** Leggi il file `wiki/index.md` per capire quali pagine esistono già nella memoria.
*   **Fase 2 (Creazione/Integrazione):** Analizza la nuova fonte. Se l'argomento principale esiste già in `index.md`, aggiorna la pagina esistente. Se è nuovo, crea una pagina nuova in `/wiki/`.
*   **Fase 3 (Collegamento):** Rileggi la pagina che hai appena scritto. C'è qualche parola chiave che corrisponde alle pagine lette in `index.md`? Se sì, trasformale in link `[[Così]]`.
*   **Fase 4 (Registrazione):** Aggiorna `index.md` (se hai creato nuove pagine) e aggiungi una riga a `log.md`.
