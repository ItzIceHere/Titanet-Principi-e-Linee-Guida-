---
icon: wrench
---

# Lista Strumenti Ufficiali

Di seguito è riportata la lista completa e tassativa di tutti i software approvati per l'utilizzo durante gli screenshare su Titanet. L'uso di qualsiasi strumento non presente in questo elenco è severamente proibito.

{% hint style="success" %}
[**Forensic Toolkit Hub**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fitzicehere-tool-downloader.vercel.app%2F)\
Per facilitare il download di tutti gli strumenti approvati, è stato creato un sito web centralizzato chiamato **Forensic Toolkit Hub**. All'interno troverete i link di download diretti e verificati per ogni tool elencato in questa guida.
{% endhint %}

***

#### Downloader di Strumenti

* [**RedLotus Tool Downloader**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2FItzIceHere%2FRedLotus-Tool-Downloader%2Freleases%2Fdownload%2FRL%2FRedLotus.Downloader.exe)\
  **Descrizione:** Un hub centralizzato progettato per scaricare automaticamente l'intera suite di strumenti approvati in questa guida. Scarica le versioni più recenti e sicure di tutti i software necessari (NirSoft, Sysinternals, Spok, Zimmerman) in pochi secondi, garantendo la standardizzazione del controllo.
* [**RedLotus Task Sentinel**](https://github.com/ItzIceHere/RedLotus-Task-Sentinel/releases/download/RL/RedLotusTaskSentinel.exe)\
  **Descrizione:** Analizzatore forense avanzato per il Task Scheduler di Windows. Rileva meccanismi di persistenza nascosti come Ghost Tasks e hijacking IFEO, integrando scansioni YARA e verifica delle firme. Monitora le modifiche post-boot tramite il Journal NTFS per identificare tentativi di evasione e binari sospetti invisibili ai tool standard.
* [RedLotus Mod Analyzer](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2FItzIceHere%2FRedLotus-Mod-Analyzer%2Freleases%2Fdownload%2FRL%2FRedLotusModAnalyzer.exe)\
  **Descrizione:** Analizzatore forense per mod di Minecraft che combina scansione della memoria e del disco. Utilizza un engine di analisi del bytecode per rilevare cheat, offuscamento e native injections. Monitora il file system in tempo reale tramite USN Journal per identificare mod eliminate o modificate dopo l'avvio del gioco, verificando automaticamente l'integrità dei file tramite hash.
* [**RedLotus Alt Checker**](https://github.com/ItzIceHere/RedLotusAltChecker/releases/download/RL/RedLotusAltChecker.exe) \
  **Descrizione:** Utility focalizzata sulla rilevazione di ban evasion nel rispetto della privacy. Esegue una scansione incrociata su piattaforme multiple (Minecraft, Steam, Discord, Windows) utilizzando algoritmi "fuzzy" per identificare variazioni di username. Analizza la storia del file system tramite USN Journal per esporre la cancellazione o la modifica di file di gioco negli ultimi 14 giorni. Opera interamente offline, estraendo solo identificativi pubblici senza accedere a dati sensibili.

***

#### Strumenti di Analisi di Sistema e Processi

* [**System Informer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fsysteminformer.sourceforge.io%2F)\
  **Descrizione:** Task manager avanzato e open-source che consente un'analisi approfondita e in tempo reale dei processi, della memoria e delle connessioni di rete del sistema. È essenziale per ispezionare la memoria dei processi alla ricerca di stringhe sospette (tracce di cheat).
* [**Search Everything**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.voidtools.com%2Fdownloads%2F)\
  **Descrizione:** Utility di ricerca file ultra-rapida che indicizza istantaneamente i nomi di file e cartelle sui volumi NTFS leggendo la Master File Table (MFT). Fondamentale per localizzare file per nome e per analizzare l'attività recente del file system ordinando i risultati per data di modifica.

***

#### Suite di Strumenti Forensi di Eric Zimmerman

* [**TimeLine Explorer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FTimelineExplorer.zip)\
  **Descrizione:** Strumento per visualizzare e analizzare timeline forensi aggregate da vari artefatti di sistema. Permette di unire gli output di diversi tool (come PECmd, MFTECmd, SrumECmd) in un'unica vista cronologica per ricostruire la sequenza degli eventi.
* [**JumpList Explorer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FJumpListExplorer.zip)\
  **Descrizione:** Utility grafica per analizzare i file delle Jump List di Windows, che registrano la cronologia dei file e delle applicazioni a cui un utente ha avuto accesso di recente, utile per ricostruire l'attività dell'utente.
* [**ShellBags Explorer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FShellBagsExplorer.zip)\
  **Descrizione:** Tool grafico per decodificare e visualizzare le chiavi di registro ShellBags, che memorizzano le preferenze di visualizzazione delle cartelle. È fondamentale per provare che un utente ha avuto accesso a specifiche directory, anche se sono state cancellate.
* [**Registry Explorer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FRegistryExplorer.zip)\
  **Descrizione:** Visualizzatore avanzato del Registro di Windows con un focus forense. È in grado di leggere i file "hive" del registro, mostrare chiavi e valori cancellati, e include bookmark per le posizioni forensi più importanti.
* [**PECmd**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FPECmd.zip)\
  **Descrizione:** Tool a riga di comando per analizzare in profondità i file Prefetch (.pf). Estrae tutte le informazioni di esecuzione, inclusi gli ultimi 8 orari di avvio e i file caricati da un programma, come DLL o JAR.
* [**MFTECmd**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FMFTECmd.zip)\
  **Descrizione:** Utility a riga di comando per analizzare la Master File Table (MFT) del file system NTFS. Permette di ricostruire la cronologia completa dei file, inclusi quelli cancellati, e di rilevare la manipolazione dei timestamp (timestomping).
* [**JLECmd**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FJLECmd.zip)\
  **Descrizione:** Analizzatore a riga di comando per le Jump List di Windows, alternativa al tool grafico JumpList Explorer.
* [**SrumECmd**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FSrumECmd.zip)\
  **Descrizione:** Tool CLI per analizzare il database del System Resource Usage Monitor (SRUM), che traccia l'attività storica dei processi e l'uso della rete per un periodo fino a 30-60 giorni, fornendo una visione a lungo termine.
* [**bstrings**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2Fbstrings.zip)\
  **Descrizione:** Utility avanzata per l'estrazione di stringhe (sequenze di testo) da qualsiasi tipo di file o da dump di memoria, con capacità di ricerca e filtraggio superiori ai tool standard.
* [**RecentFileCacheParser**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ericzimmermanstools.com%2Fnet9%2FRecentFileCacheParser.zip)\
  **Descrizione:** Analizza il file RecentFileCache.bcf, un artefatto che memorizza i percorsi dei file eseguiti di recente, utile per trovare tracce di esecuzione anche se altri log sono stati cancellati.

***

#### Suite di Strumenti di NirSoft

* [**WinPrefetchView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fwinprefetchview-x64.zip)\
  **Descrizione:** Utility grafica per analizzare i file Prefetch (.pf). Mostra quali programmi sono stati eseguiti, quando, quante volte e, soprattutto, quali file (DLL, JAR) sono stati caricati da un processo.
* [**LastActivityView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Flastactivityview.zip)\
  **Descrizione:** Aggrega le attività recenti del sistema (da Prefetch, registro, log eventi) in un'unica timeline cronologica, fornendo una rapida panoramica delle azioni dell'utente.
* [**ExecutedProgramsList**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fexecutedprogramslist.zip)\
  **Descrizione:** Elenca i programmi eseguiti su un computer analizzando diverse chiavi di registro, tra cui le note chiavi UserAssist.
* [**UserAssistView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fuserassistview.zip)\
  **Descrizione:** Decodifica e visualizza i dati contenuti nelle chiavi di registro UserAssist, che tracciano l'avvio di applicazioni tramite l'interfaccia grafica, registrando il conteggio delle esecuzioni e l'ultimo avvio.
* [**AlternateStreamView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Falternatestreamview-x64.zip)\
  **Descrizione:** Scansiona il file system alla ricerca di file che contengono Alternate Data Streams (ADS), una tecnica comune per nascondere file malevoli all'interno di file apparentemente innocui.
* [**HashMyFiles**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fhashmyfiles-x64.zip)\
  **Descrizione:** Calcola gli hash crittografici (MD5, SHA1, SHA256) di uno o più file. Indispensabile per verificare l'integrità di un file e confrontarlo con database di cheat noti, anche se è stato rinominato.
* [**JumpListsView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fjumplistsview.zip)\
  **Descrizione:** Analizza i file delle Jump List di Windows, che contengono la cronologia dei file aperti di recente da specifiche applicazioni.
* [**OpenSaveFilesView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fopensavefilesview-x64.zip)\
  **Descrizione:** Elenca i file che sono stati aperti o salvati tramite le finestre di dialogo standard di Windows, utile per scoprire se un injector ha "aperto" una DLL o se sono stati salvati file sospetti.
* [**USBDeview**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fusbdeview-x64.zip)\
  **Descrizione:** Fornisce una cronologia dettagliata di tutti i dispositivi USB (in particolare chiavette e dischi esterni) che sono stati collegati al sistema, mostrando l'ultima data di connessione e disconnessione.
* [**TurnedOnTimesView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fturnedontimesview.zip)\
  **Descrizione:** Analizza i log degli eventi di Windows per determinare gli intervalli di tempo in cui il computer è stato acceso, utile per stabilire una timeline generale e verificare la durata delle sessioni.
* [**RegScanner**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fregscanner-x64.zip)\
  **Descrizione:** Un'utility di ricerca per il Registro di Sistema molto più veloce e potente del regedit integrato. Permette di trovare rapidamente chiavi, valori o dati specifici in base a criteri avanzati.
* [**BrowserDownloadsView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fbrowserdownloadsview-x64.zip)\
  **Descrizione:** Visualizza la cronologia dei file scaricati dai principali browser web (Chrome, Firefox, Edge), mostrando URL di origine, percorso del file e data del download.
* [**Clipboardic**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fclipboardic.zip)\
  **Descrizione:** Monitora e salva automaticamente il contenuto della clipboard di Windows, archiviando testi e immagini copiati per una revisione successiva.
* [**DriverView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fdriverview-x64.zip)\
  **Descrizione:** Elenca tutti i driver dei dispositivi attualmente caricati sul sistema, fornendo dettagli come versione, produttore e percorso del file. Utile per identificare driver non standard o sospetti.
* [**FileAccessErrorView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Ffileaccesserrorview-x64.zip)\
  **Descrizione:** Mostra informazioni dettagliate sugli errori di accesso ai file (apertura, lettura, scrittura) generati dalle applicazioni, aiutando a diagnosticare problemi o comportamenti anomali.
* [**FullEventLogView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fpreviousfilesrecovery-x64.zip)\
  **Descrizione:** Permette di visualizzare e analizzare i log degli eventi di Windows da un'unica interfaccia, aggregando tutti i log di sistema e delle applicazioni.
* [**PreviousFilesRecovery**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fpreviousfilesrecovery-x64.zip)\
  **Descrizione:** Scansiona il disco alla ricerca di copie shadow (VSS) create da Windows, permettendo di recuperare versioni precedenti dei file che potrebbero essere state modificate o cancellate.
* [**RecentFilesView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Frecentfilesview.zip)\
  **Descrizione:** Mostra l'elenco dei file aperti più di recente dal sistema operativo.
* [**ShellBagsView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fshellbagsview.zip)\
  **Descrizione:** Visualizza le informazioni memorizzate nelle chiavi di registro ShellBags, che tracciano le preferenze di visualizzazione delle cartelle e provano l'accesso a determinate directory.
* [**TaskSchedulerView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Ftaskschedulerview-x64.zip)\
  **Descrizione:** Visualizza l'elenco di tutte le attività pianificate dall'Utilità di pianificazione di Windows in un'unica tabella.
* [**UninstallView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Funinstallview-x64.zip)\
  **Descrizione:** Raccoglie informazioni su tutti i programmi installati da varie fonti (registro, file di installazione) in un'unica interfaccia, alternativa al pannello di controllo.
* [**USBDriveLog**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.nirsoft.net%2Futils%2Fusbdrivelog.zip)\
  **Descrizione:** Estrae un log dettagliato di tutti i dispositivi di archiviazione USB collegati al computer, mostrando orari di connessione/disconnessione e dettagli del dispositivo.

***

#### Strumenti della Community (Sviluppatore: Spokwn)

* [**JournalTrace**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2FJournalTrace%2Freleases)\
  **Descrizione:** Interfaccia grafica (GUI) per l'analisi del USN Journal. È uno strumento fondamentale per ricostruire la cronologia delle operazioni sui file (creazione, cancellazione, rinomina) grazie a un potente sistema di filtri.
* [**Paths Parser**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2FPathsParser%2Freleases)\
  **Descrizione:** Tool versatile che analizza una lista di percorsi di file (tipicamente estratti dalla memoria di un processo) per verificare l'esistenza, la firma digitale e applicare regole euristiche per identificare caratteristiche sospette.
* [**BAM Parser**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2FBAM-parser%2Freleases)\
  **Descrizione:** Parser con interfaccia grafica dedicato all'analisi delle voci del Background Activity Moderator (BAM), che registra le esecuzioni dei programmi, integrando controlli sulla firma digitale e rilevamento di anomalie.
* [**Prefetch Parser**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2Fprefetch-parser%2Freleases)\
  **Descrizione:** Utility per l'analisi dei file Prefetch che integra funzionalità aggiuntive come la verifica della firma digitale, l'analisi del BAM e la possibilità di eseguire regole YARA sul file eseguibile associato.
* [**pcasvc-executed**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2Fpcasvc-executed%2Freleases)\
  **Descrizione:** Tool specifico per analizzare gli artefatti di esecuzione lasciati dal Program Compatibility Assistant Service (PcaSvc), applicando controlli di firma digitale e regole euristiche.
* [**ActivitiesCache-execution**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2FActivitiesCache-execution%2Freleases)\
  **Descrizione:** Analizza il database della Windows Timeline (ActivitiesCache.db), che registra la cronologia delle attività dell'utente come l'avvio di applicazioni e l'apertura di file.
* [**Replaceparser**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fspokwn%2FReplaceparser%2Freleases)\
  **Descrizione:** Un semplice parser focalizzato su un unico compito: analizzare il USN Journal per rilevare specificamente le operazioni di sostituzione di file (file replacement).
* [BAM Deleted Keys](https://github.com/spokwn/BamDeletedKeys/releases)\
  **Descrizione:** Tool specializzato nel rilevamento di tecniche anti-forensi mirate al Background Activity Moderator (BAM). Confronta l'hive di registro SYSTEM in tempo reale con una copia storica per identificare con precisione le chiavi BAM che sono state eliminate. Poiché la cancellazione di queste chiavi è un metodo comune per nascondere l'esecuzione di programmi, questo strumento fornisce una prova diretta e inconfutabile di manomissione delle prove.
* [**Utility Tool**](https://github.com/spokwn/Tool/releases)\
  **Descrizione:** Agisce come un versatile toolkit multi-funzione che aggrega diverse utility e controlli rapidi in un'unica interfaccia. Progettato per accelerare le operazioni comuni durante uno screenshare, può includere funzioni come la raccolta rapida di informazioni di sistema, l'esecuzione di comandi diagnostici predefiniti o scorciatoie per accedere a percorsi di artefatti forensi, ottimizzando l'efficienza dell'analisi.

***

#### Analisi Forense del File System

* [**FTK Imager**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fd1kpmuwb7gvu1i.cloudfront.net%2FImgr%2F4.7.3.81%2520Release%2FExterro_FTK_Imager_%2528x64%2529-4.7.3.81.exe)\
  **Descrizione:** Strumento forense essenziale per l'analisi a basso livello del file system. Permette di visualizzare la struttura grezza di un disco, accedere a file bloccati (come hive del registro o metadati NTFS) e analizzare partizioni non-NTFS come FAT32 ed exFAT, comuni su USB.
* [**Recuva**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.ccleaner.com%2Frcsetup154.exe)\
  **Descrizione:** Utility specializzata nel recupero di file cancellati. È particolarmente utile per tentare di recuperare prove che sono state eliminate, specialmente su drive che non supportano il journaling (come le chiavette USB in FAT32).

***

#### Analisi di File Eseguibili e Codice

* [**Detect It Easy (DiE)**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fhorsicq%2FDIE-engine%2Freleases)\
  **Descrizione:** Utility di identificazione per file eseguibili. Rileva se un file è stato "impacchettato" (packed) o protetto con software di offuscamento, analizza l'entropia del file e identifica il compilatore utilizzato.
* [**HxD Hex Editor**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fmh-nexus.de%2Fdownloads%2FHxDPortableSetup.zip)\
  **Descrizione:** Un editor esadecimale leggero e veloce, fondamentale per l'analisi a basso livello del contenuto binario di un file. Permette di visualizzare dati grezzi, cercare stringhe specifiche o identificare modifiche manuali.
* [**PEStudio**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fwww.winitor.com%2Ftools%2Fpestudio%2Fcurrent%2Fpestudio.zip)\
  **Descrizione:** Un potente strumento per l'analisi statica di file eseguibili (PE) che raccoglie una grande quantità di informazioni su un file (.exe, .dll), incluse librerie importate, stringhe e firma digitale.
* [**Strings (Sysinternals)**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.sysinternals.com%2Ffiles%2FStrings.zip)\
  **Descrizione:** Utility a riga di comando che estrae le stringhe di testo (sia ASCII che Unicode) da file binari. È un metodo rapido per ottenere indizi sulla funzionalità di un programma senza eseguirlo.
* [**BinText**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Ffiles1.majorgeeks.com%2F400376550b320e37264e5ab1318d2973a41a3689%2Foffice%2Fbintext303.zip)\
  **Descrizione:** Un'alternativa grafica a "Strings" che estrae testo, incluse stringhe ASCII e Unicode, da qualsiasi tipo di file binario, rendendo l'analisi più visuale.

***

#### Analisi di Mod (Specifico per Minecraft)

* [**Luyten**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2Fdeathmarine%2FLuyten%2Freleases)\
  **Descrizione:** Un decompilatore Java open-source semplice e ampiamente utilizzato. È uno strumento essenziale per un'analisi rapida del contenuto di mod e client di Minecraft in formato .jar.
* [**Recaf**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2FCol-E%2FRecaf%2Freleases)\
  **Descrizione:** Un moderno decompilatore ed editor di bytecode Java, considerato un'alternativa più potente a Luyten. Offre funzionalità avanzate per un'analisi interattiva e approfondita di file .jar complessi.

***

#### Analisi di Sistema e Rete (Sysinternals Suite)

* [**Process Explorer**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.sysinternals.com%2Ffiles%2FProcessExplorer.zip)\
  **Descrizione:** Un'alternativa molto più potente al Task Manager di Windows. Mostra informazioni dettagliate sui processi, incluse le librerie .dll caricate, gli handle aperti e le connessioni di rete, con integrazione VirusTotal.
* [**Autoruns**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.sysinternals.com%2Ffiles%2FAutoruns.zip)\
  **Descrizione:** Lo strumento più completo per analizzare le "posizioni di avvio automatico" in Windows. Controlla non solo le chiavi Run, ma anche servizi, driver e scheduled task per scovare meccanismi di persistenza.
* [**ProcMon (Process Monitor)**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.sysinternals.com%2Ffiles%2FProcessMonitor.zip)\
  **Descrizione:** Uno strumento di monitoraggio in tempo reale che mostra l'attività del file system, del registro e dei processi. Estremamente potente per l'analisi dinamica (vedere cosa fa un programma quando viene eseguito).
* [**TCPView**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fdownload.sysinternals.com%2Ffiles%2FTCPView.zip)\
  **Descrizione:** Mostra un elenco dettagliato di tutte le connessioni di rete TCP e UDP attive in tempo reale, includendo l'indirizzo locale/remoto e il processo associato. Utile per identificare connessioni sospette.

***

#### Parser degli Eventi

* [**Hayabusa**](https://www.google.com/url?sa=E\&q=https%3A%2F%2Fgithub.com%2FYamato-Security%2Fhayabusa%2Freleases%2F)\
  **Descrizione:** Un parser di log eventi di Windows estremamente veloce e potente, scritto in Rust. Utilizza le regole Sigma per la caccia alle minacce (threat hunting), rendendolo ideale per analizzare rapidamente grandi quantità di log alla ricerca di attività malevole.
