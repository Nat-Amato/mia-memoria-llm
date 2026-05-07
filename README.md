# Gestore Wiki Automatico
![License](https://img.shields.io/badge/license-AGPLv3-blue.svg)

Questo progetto implementa un Gestore Wiki Automatico basato su prompt per modelli linguistici (LLM). L'obiettivo è trasformare documenti testuali grezzi in una base di conoscenza strutturata e interconnessa in formato Markdown, mantenendo un indice centrale e un registro cronologico delle attività.

Il sistema risolve il problema della frammentazione e della disorganizzazione delle informazioni. Automatizza i processi di ingestione, l'estrazione di concetti chiave, la creazione di nuove pagine tematiche e il cross-linking intelligente tramite la sintassi wiki `[[Nome_Pagina]]`.

## 📑 Indice
- [Architettura e Struttura](#%EF%B8%8F-architettura-e-struttura)
- [Prerequisiti e Dipendenze](#-prerequisiti-e-dipendenze)
- [Installazione e Setup](#-installazione-e-setup)
- [Utilizzo](#-utilizzo)
- [Flussi di Lavoro e CI/CD](#-flussi-di-lavoro-e-cicd)
- [Contribuire e Licenza](#-contribuire-e--licenza)

## 🏗️ Architettura e Struttura
Il progetto segue un approccio "prompt-driven", dove non vi è codice sorgente eseguibile tradizionale, ma piuttosto un insieme di istruzioni testuali e regole che guidano un agente LLM nella gestione dei file.

La struttura delle directory è organizzata come segue:

```text
.
├── LICENSE
├── Prompt.md               # Prompt principali per istruire l'LLM al ruolo
├── schema/
│   └── INSTRUCTIONS.md     # Regole core di formattazione e workflow a 3 fasi
├── sources/                # Directory di input: file grezzi da elaborare
└── wiki/                   # Directory di output: la base di conoscenza generata
    ├── index.md            # Indice di tutti i concetti e le pagine esistenti
    └── log.md              # Registro cronologico delle ingestioni
```

## 📦 Prerequisiti e Dipendenze
Essendo un sistema documentale guidato da prompt per LLM, non vi sono dipendenze software da compilare o librerie da installare tramite package manager.

- **Strumenti richiesti:** Un client, API o un ambiente compatibile con Large Language Models in grado di leggere e scrivere file (es. un agente LLM locale).
- **Competenze:** Familiarità con la sintassi Markdown e la gestione di knowledge base.

> Note: Mancano file di configurazione (es. package.json, requirements.txt) poiché il progetto non utilizza uno stack tecnologico software convenzionale.

## 🚀 Installazione e Setup
Clona il repository sul tuo ambiente locale per iniziare a utilizzare la wiki:

```bash
git clone <url-del-repository>
cd nome-del-repository
```

Non sono richiesti ulteriori comandi per l'installazione di dipendenze.

> Note: Mancano istruzioni per la configurazione di variabili d'ambiente in quanto l'interazione avviene fornendo l'accesso ai file locali all'agente LLM.

## 💻 Utilizzo
L'utilizzo si basa sull'interazione con un LLM incaricato di eseguire i comandi definiti. Fornisci all'LLM l'accesso ai file del repository e utilizza i prompt preimpostati.

**1. Avviare un'ingestione:**
Per ingerire un nuovo documento, invia il seguente comando (come documentato in `Prompt.md`):

```text
Agisci come il mio Gestore Wiki. Leggi le regole contenute in schema/INSTRUCTIONS.md. Basandoti su quelle istruzioni, esegui il workflow di ingestione per il nuovo file sources/dieta_mediterranea.txt. Genera le nuove pagine e aggiorna i file necessari direttamente nella cartella /wiki/.
```

**2. Mappare e generare collegamenti:**
```text
Agisci come Gestore Wiki. Leggi il file @wiki/index.md per mappare tutti i concetti esistenti. Poi analizza tutti i file .md presenti nella cartella @wiki/. Il tuo compito è trovare parole chiave e concetti correlati tra questi file e inserire la sintassi [[Nome_File_Corrispondente]] per creare i collegamenti mancanti. Aggiorna i file.
```

## 🔄 Flussi di Lavoro e CI/CD
Il workflow principale di ingestione si articola in 4 fasi manuali o guidate dall'agente:
1. **Mappatura:** Lettura di `wiki/index.md` per il contesto esistente.
2. **Creazione/Integrazione:** Analisi della fonte e creazione o aggiornamento dei documenti.
3. **Collegamento:** Rilettura e inserimento dei cross-link.
4. **Registrazione:** Aggiornamento dei file `index.md` e `log.md`.

> Note: Mancano flussi di CI/CD automatizzati (es. GitHub Actions, pipeline Docker) e mancano le istruzioni per i test, poiché i processi di verifica e normalizzazione vengono eseguiti tramite prompt di controllo invece che tramite script di test standard.

## 🤝 Contribuire e 📄 Licenza
**Contribuire:** I contributi sono benvenuti per espandere le regole di formattazione in `schema/INSTRUCTIONS.md` o per perfezionare i comandi in `Prompt.md`. Assicurati che ogni modifica mantenga la coerenza della base di conoscenza.

**Licenza:** Il progetto è distribuito sotto la licenza **GNU Affero General Public License v3.0 (AGPLv3)**. Consulta il file `LICENSE` per i dettagli completi.
