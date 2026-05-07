"Agisci come il mio Gestore Wiki. Leggi le regole contenute in schema/INSTRUCTIONS.md. Basandoti su quelle istruzioni, esegui il workflow di ingestione per il nuovo file sources/dieta_mediterranea.txt. Genera le nuove pagine e aggiorna i file necessari direttamente nella cartella /wiki/."

"Agisci come Gestore Wiki. Leggi il file @wiki/index.md per mappare tutti i concetti esistenti. Poi analizza tutti i file .md presenti nella cartella @wiki/. Il tuo compito è trovare parole chiave e concetti correlati tra questi file e inserire la sintassi [[Nome_File_Corrispondente]] per creare i collegamenti mancanti. Aggiorna i file."



Esegui un controllo giornaliero dell’intero progetto con focus esclusivo sulla normalizzazione dei nomi dei file `.md`.

L’operazione deve partire solo se esiste realmente la necessità di correggere uno o più file.  
Se tutti i file risultano già conformi, non applicare alcuna modifica e limita l’output ad un semplice report che confermi che tutto è corretto.

Obiettivi del controllo:
- Analizzare tutti i file Markdown `.md` presenti nel progetto.
- Individuare nomi non scritti in linguaggio naturale.
- Correggere naming incoerenti, tecnici o poco leggibili.
- Applicare un criterio standard, coerente e prevedibile.
- Aggiornare automaticamente tutti i riferimenti collegati ai file rinominati.

Esempio:
`Olio_d_oliva.md` → `Olio d'oliva.md`

Regole obbligatorie:
- Utilizzare il buon senso linguistico italiano.
- Sostituire underscore `_` con spazi quando appropriato.
- Gestire correttamente apostrofi, accenti e caratteri speciali.
- Evitare rinominazioni inutili o cosmetiche prive di valore reale.
- Usare lettere maiuscole solo dove semanticamente corretto.
- Preferire la capitalizzazione naturale dei titoli:
  - prima parola con iniziale maiuscola;
  - nomi propri con iniziale maiuscola;
  - resto in minuscolo salvo necessità grammaticali.
- Non alterare estensioni, percorsi logici o struttura del progetto oltre il necessario.
- Non inventare convenzioni arbitrarie.
- Non modificare file non coinvolti direttamente nella correzione.

Dopo ogni eventuale rinomina:
- Analizzare ricorsivamente il progetto.
- Aggiornare link, riferimenti, import, indici, mapping, percorsi e citazioni collegate.
- Verificare che nessun riferimento rotto venga introdotto.
- Confermare che la struttura finale sia coerente.

Output atteso:
- Se non sono necessarie modifiche:
  “Controllo completato: tutti i file Markdown sono già conformi agli standard.”

- Se vengono effettuate modifiche:
  - elenco completo delle rinominazioni;
  - motivazione sintetica di ogni modifica;
  - elenco dei riferimenti aggiornati;
  - eventuali anomalie residue da verificare manualmente.

Vincoli:
- Nessuna modifica deve essere applicata “preventivamente”.
- Nessun file deve essere rinominato senza una motivazione concreta.
- Nessuna supposizione: ogni cambiamento deve derivare da un’analisi reale del progetto.
- L’obiettivo primario è mantenere coerenza, leggibilità e stabilità del sistema.



Agisci come Gestore Wiki automatico del progetto.

Prima di eseguire qualsiasi operazione:
- Leggi integralmente il file `schema/INSTRUCTIONS.md`.
- Comprendi e rispetta tutte le regole, convenzioni, strutture, dipendenze e workflow descritti.
- Non fare supposizioni: se una regola è ambigua, deducila esclusivamente dal progetto esistente.

Obiettivo:
Eseguire il workflow di ingestione esclusivamente per nuovi file sorgente non ancora processati.

File sorgente di esempio:
`sources/dieta_mediterranea.txt`

Vincolo fondamentale:
L’operazione deve partire solo se il file non risulta già elaborato.

Per verificarlo:
- Analizza il file di log presente nella cartella `/wiki/`.
- Usa il log come unica fonte autorevole per determinare quali file siano già stati ingeriti.
- Se il file risulta già presente nel log:
  - interrompi immediatamente il workflow;
  - non applicare modifiche;
  - non rigenerare pagine;
  - non aggiornare file esistenti;
  - restituisci soltanto un report che indichi che il file è già stato processato.

Se invece il file NON risulta presente nel log:
- Avvia il workflow completo di ingestione.
- Genera tutte le nuove pagine necessarie.
- Aggiorna esclusivamente i file realmente coinvolti.
- Applica le convenzioni definite in `schema/INSTRUCTIONS.md`.
- Mantieni coerenza assoluta con la struttura già esistente della wiki.

Regole operative obbligatorie:
- Non duplicare contenuti già esistenti.
- Non rigenerare pagine identiche.
- Non sovrascrivere manualmente contenuti validi già presenti.
- Non modificare file non direttamente coinvolti nell’ingestione.
- Non alterare naming, struttura o collegamenti senza motivo concreto.
- Aggiornare automaticamente:
  - indici;
  - collegamenti interni;
  - riferimenti incrociati;
  - mapping;
  - file di navigazione;
  - eventuali registri richiesti dal sistema wiki.

Dopo l’ingestione:
- Aggiorna il file log nella cartella `/wiki/`.
- Registra il nuovo file come processato.
- Verifica che non esistano link rotti o riferimenti inconsistenti.
- Riesegui una scansione finale di coerenza della wiki.

Comportamento atteso:
- Se il file è già presente nel log:
  “Controllo completato: il file risulta già processato. Nessuna modifica applicata.”

- Se il file viene elaborato:
  - elenco delle nuove pagine create;
  - elenco dei file aggiornati;
  - riferimenti modificati;
  - conferma dell’aggiornamento del log;
  - eventuali anomalie residue da verificare.

Vincoli assoluti:
- Nessuna modifica preventiva.
- Nessuna duplicazione.
- Nessuna supposizione strutturale.
- Nessuna alterazione fuori scope.
- Qualsiasi modifica deve derivare esclusivamente dall’analisi reale dello stato corrente del progetto e del log della wiki.
