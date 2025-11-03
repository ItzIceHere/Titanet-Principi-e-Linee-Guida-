---
icon: wrench
---

# Lista Strumenti Ufficiali

Di seguito è riportata la lista completa e tassativa di tutti i software approvati per l'utilizzo durante gli screenshare su Titanet. L'uso di qualsiasi strumento non presente in questo elenco è severamente proibito.

***

**Strumenti di Analisi di Sistema e Processi**

* **System Informer**
  * **Descrizione:** Un potente task manager avanzato che permette l'analisi in tempo reale di processi, thread, servizi, connessioni di rete e utilizzo della memoria. Fondamentale per ispezionare la memoria dei processi alla ricerca di tracce di cheat.
* **Search Everything**
  * **Descrizione:** Un'utility di ricerca per file e cartelle estremamente rapida. Indicizza i volumi NTFS quasi istantaneamente, permettendo di trovare file per nome, data, dimensione o attributi in tempo reale.

***

**Suite di Strumenti Forensi di Eric Zimmerman**

* **Registry Explorer**
  * **Descrizione:** Un visualizzatore avanzato per il Registro di Sistema di Windows. È in grado di leggere i file "hive" del registro, mostrare chiavi e valori cancellati e include bookmark per le posizioni forensi più importanti.
* **PECmd (Prefetch Explorer Command Line)**
  * **Descrizione:** Un tool a riga di comando per analizzare in profondità i file Prefetch (.pf). Estrae tutte le informazioni di esecuzione, inclusi gli ultimi 8 orari di avvio e i file caricati.
* **MFTECmd (MFT Explorer Command Line)**
  * **Descrizione:** Un tool a riga di comando per analizzare la Master File Table (MFT) del file system NTFS. Permette di ricostruire la cronologia dei file, inclusi quelli cancellati, e di rilevare il timestomping.
* **JLECmd (JumpList Explorer Command Line)**
  * **Descrizione:** Un tool a riga di comando per analizzare le Jump List di Windows, che contengono informazioni sui file e le applicazioni a cui si è avuto accesso di recente.
* **SrumECmd (SRUM Explorer Command Line)**
  * **Descrizione:** Un tool a riga di comando per analizzare il database del System Resource Usage Monitor (SRUM), che traccia l'attività dei processi e l'uso della rete per un periodo fino a 30-60 giorni.
* **bstrings**
  * **Descrizione:** Un'utility avanzata per l'estrazione di stringhe da file o dump di memoria, con capacità di ricerca e filtraggio superiori rispetto a tool standard.

***

**Suite di Strumenti di NirSoft**

* **WinPrefetchView**
  * **Descrizione:** Strumento fondamentale per analizzare i file di Prefetch (`.pf`). Mostra quali programmi sono stati eseguiti, quando e quante volte. È cruciale per stabilire una timeline di esecuzione e per analizzare quali file (`.dll`, `.jar`) sono stati caricati da un processo.
* **LastActivityView**
  * **Descrizione:** Aggrega in un'unica interfaccia cronologica le attività recenti del sistema. Raccoglie dati da Prefetch, chiavi di registro (come `RecentDocs` e `UserAssist`), log degli eventi e altro, fornendo una rapida panoramica delle azioni dell'utente.
* **ExecutedProgramsList**
  * **Descrizione:** Si concentra sull'analisi di diverse chiavi di registro (tra cui `UserAssist`) per elencare i programmi che sono stati eseguiti sul computer. Utile per corroborare le prove di esecuzione trovate con altri strumenti.
* **UserAssistView**
  * **Descrizione:** Decodifica e visualizza le informazioni contenute nelle chiavi di registro `UserAssist`. Queste chiavi tracciano l'avvio di applicazioni tramite l'interfaccia grafica, registrando il conteggio delle esecuzioni e l'ultimo avvio.

**Analisi del File System e dei File**

* **AlternateStreamView**
  * **Descrizione:** Scansiona il file system alla ricerca di file che contengono Alternate Data Streams (ADS). Questa è una tecnica comune per nascondere file malevoli all'interno di file apparentemente innocui.
* **HashMyFiles**
  * **Descrizione:** Calcola gli hash (MD5, SHA1, SHA256) di uno o più file. Indispensabile per verificare l'integrità di un file e confrontarlo con database di cheat noti (come VirusTotal) anche se è stato rinominato.
* **RecentFileCacheParser** (`.bcf` parser)
  * **Descrizione:** Analizza il file `RecentFileCache.bcf`, un artefatto che memorizza i percorsi dei file eseguiti di recente. Può contenere tracce di esecuzione anche se altri log sono stati cancellati.
* **JumpListsView**
  * **Descrizione:** Analizza i file delle Jump List di Windows, che contengono la cronologia dei file aperti di recente da specifiche applicazioni. Può rivelare l'interazione con file di configurazione o cheat.
* **OpenSaveFilesView**
  * **Descrizione:** Elenca i file che sono stati aperti o salvati tramite le finestre di dialogo standard di Windows. Utile per scoprire se un injector ha "aperto" una `.dll` o se sono stati salvati file di log sospetti.

**Analisi Hardware e di Rete**

* **USBDeview**
  * **Descrizione:** Fornisce una cronologia dettagliata di tutti i dispositivi USB (in particolare chiavette e dischi esterni) che sono stati collegati al sistema. Mostra l'ultima data di connessione e disconnessione, fondamentale per rilevare il "cheat su chiavetta".
* **TurnedOnTimesView**
  * **Descrizione:** Analizza i log degli eventi di Windows per determinare gli intervalli di tempo in cui il computer è stato acceso. Utile per stabilire una timeline generale e verificare la durata delle sessioni.

**Analisi del Registro di Sistema**

* **RegScanner**
  * **Descrizione:** Un'utility di ricerca per il Registro di Sistema molto più veloce e potente del `regedit` integrato. Permette di trovare rapidamente chiavi, valori o dati specifici in base a criteri avanzati.

***

#### Strumenti della Community (Sviluppatore: Spokwn)

Questa sezione elenca gli strumenti sviluppati da Spokwn, approvati per l'uso durante i controlli su Titanet. Questi tool sono noti per la loro efficacia e per l'integrazione di molteplici tecniche di analisi forense.

***

**Strumenti Principali di Analisi**

* **JournalTrace**
  * **Descrizione:** Un'interfaccia grafica (GUI) per l'analisi del USN Journal. È uno strumento fondamentale per ricostruire la cronologia delle operazioni sui file (creazione, cancellazione, rinomina, modifica degli attributi). La sua forza risiede nel potente sistema di filtri avanzati (`&&` per AND, `!!` per NOT, `||` per OR) che permette di isolare eventi specifici con grande precisione, come la cancellazione di file `.pf` o la manipolazione di permessi.
* **Paths Parser**
  * **Descrizione:** Un tool versatile che analizza una lista di percorsi di file (tipicamente estratti dalla memoria di un processo come `csrss.exe`). Per ogni file, verifica l'esistenza, la firma digitale, e applica una serie di regole euristiche (dette "generics") per identificare caratteristiche sospette comuni in cheat e malware. Integra anche un controllo sul USN Journal per rilevare tentativi di sostituzione (file replacement).
* **BAM Parser**
  * **Descrizione:** Un parser con interfaccia grafica dedicato all'analisi delle voci del Background Activity Moderator (BAM). Oltre a estrarre l'orario di esecuzione dei programmi, integra controlli sulla firma digitale, euristiche di rilevamento (generics) e la verifica del USN Journal per identificare sostituzioni di file, fornendo un'analisi molto più approfondita rispetto a una semplice lettura del registro.

***

**Strumenti Specifici per Artefatti**

* **Prefetch Parser**
  * **Descrizione:** Un'utility per l'analisi dei file Prefetch. Simile a WinPrefetchView, offre un'interfaccia per visualizzare i dati di esecuzione, ma integra funzionalità aggiuntive come la verifica della firma digitale, l'analisi del BAM e la possibilità di eseguire regole YARA sul file eseguibile associato.
* **pcasvc-executed**
  * **Descrizione:** Un tool specifico per analizzare gli artefatti di esecuzione lasciati dal Program Compatibility Assistant Service (PcaSvc). Estrae le informazioni sui programmi avviati e, come altri tool di Spokwn, integra controlli di firma digitale e regole euristiche per identificare software sospetto.
* **ActivitiesCache-execution**
  * **Descrizione:** Analizza il database della Windows Activities Cache (`ActivitiesCache.db`), che alimenta la funzione "Timeline". Estrae la cronologia delle attività dell'utente, come l'avvio di applicazioni e l'apertura di file, applicando controlli di firma e regole YARA per identificare attività sospette.
* **Replaceparser**
  * **Descrizione:** Un semplice parser focalizzato su un unico compito: analizzare il USN Journal per rilevare specificamente le operazioni di sostituzione di file (file replacement). Utile per un'indagine mirata su questa specifica tecnica di bypass.

***

**Strumenti Avanzati e di Analisi di Memoria**

* **Kernel-Live-Dump-Analyzer**
  * **Descrizione:** Uno strumento avanzato che analizza i dump della memoria del kernel (Kernel Live Dump). Automatizza la ricerca di comandi, script e stringhe associati a tecniche di bypass comuni (es. esecuzioni fileless, manipolazione di servizi via CMD/PowerShell), accelerando notevolmente un processo di analisi altrimenti lungo e complesso.

***

#### Strumenti Aggiuntivi Ufficiali

Questi strumenti, provenienti da vari sviluppatori o dalla stessa Microsoft, sono approvati per l'uso durante i controlli su Titanet. Coprono aree specifiche dell'analisi forense non coperte dagli strumenti di suite più grandi.

***

**Analisi Forense del File System**

* **FTK Imager (AccessData/Exterro)**
  * **Descrizione:** Uno strumento forense essenziale per l'analisi a basso livello del file system. Permette di visualizzare la struttura grezza di un disco, accedere a file bloccati dal sistema operativo (come gli "hive" del registro o i metadati NTFS), ed è fondamentale per analizzare partizioni con file system non-NTFS come **FAT32** ed **exFAT**, che sono comuni sui dispositivi USB.
* **Recuva**
  * **Descrizione:** Un'utility specializzata nel recupero di file cancellati. È particolarmente utile per tentare di recuperare prove che sono state eliminate dal Cestino o tramite Shift+Delete, specialmente su drive che non supportano il journaling (come le chiavette USB in FAT32), dove altri metodi di tracciamento sono inefficaci.

***

**Analisi di File Eseguibili e Codice**

* **Detect It Easy (DiE)**
  * **Descrizione:** Un tool di identificazione per file eseguibili. Rileva se un file è stato "impacchettato" (packed) o protetto con software di offuscamento (come Themida o VMProtect), analizza l'**entropia** del file per rilevare sezioni crittografate o compresse, e identifica il compilatore utilizzato. Indispensabile per una prima valutazione di un eseguibile sospetto.
* **HxD Hex Editor**
  * **Descrizione:** Un editor esadecimale leggero e veloce. È fondamentale per l'analisi a basso livello del contenuto binario di un file. Permette di visualizzare e modificare i dati grezzi, utile per cercare stringhe specifiche, analizzare le intestazioni (header) dei file o identificare modifiche manuali (hex editing).
* **PEStudio**
  * **Descrizione:** Un potente strumento per l'analisi statica di file eseguibili (PE). Raccoglie una quantità enorme di informazioni su un file (.exe, .dll), inclusi header, sezioni, librerie importate, funzioni esportate, risorse, stringhe e firma digitale. Eccellente per una valutazione rapida della "pericolosità" di un file.
* **Strings (Sysinternals)**
  * **Descrizione:** Un'utility a riga di comando della suite Sysinternals di Microsoft. Estrae le stringhe di testo (sia ASCII che Unicode) da file binari. È un metodo rapido per ottenere indizi sulla funzionalità di un programma senza doverlo eseguire o decompilare.

***

**Analisi di Mod (Specifico per Minecraft)**

* **Luyten**
  * **Descrizione:** Un decompilatore Java open-source semplice e ampiamente utilizzato. È uno strumento essenziale per un'analisi rapida del contenuto di mod e client di Minecraft in formato .jar, permettendo di ispezionare il codice alla ricerca di funzionalità sospette o di codice offuscato.
* **Recaf**
  * **Descrizione:** Un moderno decompilatore ed editor di bytecode Java, considerato un'alternativa più potente a Luyten. Offre funzionalità avanzate come la modifica del codice al volo e una ricerca di riferimenti più completa, rendendolo ideale per un'analisi interattiva e approfondita di file .jar complessi.

***

**Analisi di Sistema e Rete (Sysinternals Suite)**

* **Process Explorer**
  * **Descrizione:** Un'alternativa molto più potente al Task Manager di Windows. Mostra informazioni dettagliate sui processi, incluse le librerie .dll caricate, gli handle aperti e le connessioni di rete. La sua capacità di verificare le firme digitali al volo e l'integrazione con VirusTotal lo rendono eccellente per l'analisi dei processi in tempo reale.
* **Autoruns**
  * **Descrizione:** Lo strumento più completo per analizzare le "posizioni di avvio automatico" in Windows. Controlla non solo le chiavi Run, ma anche servizi, driver, scheduled task e molto altro. Fondamentale per scovare meccanismi di persistenza.
* **ProcMon (Process Monitor)**
  * **Descrizione:** Uno strumento di monitoraggio in tempo reale che mostra l'attività del file system, del registro e dei processi. Estremamente potente per l'analisi dinamica (vedere cosa fa un programma quando viene eseguito), ma considerato uno strumento per utenti più esperti.
* **TCPView**
  * **Descrizione:** Mostra un elenco dettagliato di tutte le connessioni di rete TCP e UDP attive, includendo l'indirizzo locale/remoto e il processo associato. Utile per identificare connessioni sospette in tempo reale.
