---
icon: square-code
---

# Lista Script PowerShell Ufficiali

Gli script PowerShell sono strumenti potenti per automatizzare ricerche complesse e raccogliere dati in modo efficiente. Per garantire sicurezza e standardizzazione, è obbligatorio utilizzare esclusivamente gli script presenti in questa lista, eseguiti tramite i comandi forniti. L'uso di script non autorizzati o modificati è severamente proibito.

> **Nota sull'Esecuzione:** Tutti i comandi forniti includono `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`. Questo permette l'esecuzione dello script solo per la sessione corrente del terminale, senza modificare permanentemente le policy di sicurezza del sistema del player.

***

**Categoria: Raccolta e Analisi Forense Completa**

* **RL Collector (RedLotus Collector)**
  * **Autore:** Red Lotus (basato su strumenti di Eric Zimmerman)
  * **Scopo:** Esegue una raccolta forense completa e automatizzata di un'ampia gamma di artefatti critici (Prefetch, SRUM, Registry Hives, Event Logs, Activities Cache, ShellBags, etc.), salvandoli in una cartella strutturata per un'analisi approfondita. È lo strumento ideale da eseguire all'inizio di un'indagine complessa per preservare le prove.
  * [Guida allo script](https://i.e-z.host/qal5twsgvclz8iw.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell -Command "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; Invoke-Expression (Invoke-RestMethod 'https://pastebin.com/raw/Eb6r6Vau')"
      ```
* **Master Timeline Script**
  * **Autore:** Red Lotus Community
  * **Scopo:** Script di post-analisi da utilizzare sui dati raccolti da `RL Collector`. Aggrega i numerosi file `.csv` prodotti dai vari parser in un'unica "master timeline" cronologica, trasformando dati sparsi in una narrazione sequenziale degli eventi.
  * [Guida allo script](https://i.e-z.host/f7h7u52nv55wrtb.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      # Aprire il link, copiarne il contenuto ed eseguirlo in una finestra PowerShell
      https://pastebin.com/raw/u7HAmWe1
      ```

***

**Categoria: Analisi di File e Integrità**

* **RedLotus Signatures**
  * **Autore:** bacanoicua / Red Lotus
  * **Scopo:** Analizza una lista di percorsi di file da un file `paths.txt` e verifica lo stato della firma digitale Authenticode di ciascuno. Fondamentale per identificare rapidamente eseguibili o DLL non firmati, manomessi (`HashMismatch`) o non attendibili.
  * [Guida allo script](https://i.e-z.host/lrbb4jzyep4gurv.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/bacanoicua/Screenshare/main/RedLotusSignatures.ps1)
      ```
* **RedLotus Prefetch Integrity Analyzer**
  * **Autore:** bacanoicua / Red Lotus
  * **Scopo:** Scansiona la cartella Prefetch alla ricerca di anomalie e tecniche di tampering. Controlla attributi (es. `Read-Only`), validità dell'header ("MAM") e rileva hash duplicati, che possono indicare manipolazioni come il "type" o "echo" bypass.
  * [Guida allo script](https://i.e-z.host/43h2ztg44hw3btg.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/bacanoicua/Screenshare/main/RedLotusPrefetchIntegrityAnalyzer.ps1)
      ```
* **HabibiModAnalyzer**
  * **Autore:** HadronCollision
  * **Scopo:** Automatizza l'analisi delle mod di Minecraft. Confronta gli hash dei file `.jar` con il database di Modrinth, esegue una scansione per stringhe di cheat comuni e analizza il `Zone.Identifier` per determinare l'origine del download.
  * [Guida allo script](https://i.e-z.host/uyjimjyuw54ge2o.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/HadronCollision/PowershellScripts/refs/heads/main/HabibiModAnalyzer.ps1)
      ```

***

**Categoria: Analisi di Artefatti Specifici**

* **RedLotus BAM Script (BAM Parser)**
  * **Autore:** PureIntent / spokwn
  * **Scopo:** Estrae e visualizza le voci del Background Activity Moderator (BAM), mostrando l'orario di esecuzione, il percorso del file e lo stato della firma digitale. La versione di spokwn genera un report HTML interattivo.
  * **Comando di Esecuzione (PureIntent):**
  *   [Guida allo script](https://i.e-z.host/f4o0p10o93m9p4a.jpg)

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/PureIntent/ScreenShare/main/RedLotusBam.ps1)
      ```
  * **Comando di Esecuzione (spokwn):**
  *   [Guida allo script](https://i.e-z.host/0o3j9whgs6hdr22.jpg)

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/spokwn/powershells/refs/heads/main/bamparser.ps1)
      ```
* **Streams Script**
  * **Autore:** spokwn
  * **Scopo:** Scansiona una cartella (anche ricorsivamente) per identificare file con Alternate Data Streams (ADS), mostrando dettagli come nome, hash, proprietario e contenuto dello stream `Zone.Identifier`.
  * [Guida allo script](https://i.e-z.host/d5rdbs9rfax4h5g.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/spokwn/powershells/refs/heads/main/Streams.ps1)
      ```
* **ActivitiesCache Parser Script**
  * **Autore:** spokwn
  * **Scopo:** Automatizza il download e l'esecuzione di un parser per il database della `ActivitiesCache.db` (Windows Timeline), filtrando le attività relative alla sessione di logon corrente.
  * [Guida allo script](https://i.e-z.host/kttit2kecjuuaua.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/spokwn/powershells/refs/heads/main/activitiescache.ps1)
      ```
* **Task Scheduler Parsers (N0LW & Rio)**
  * **Autore:** N0LW, Rio/ObsessiveBf
  * **Scopo:** Una suite di script per l'analisi del Task Scheduler. `ManualTasks` elenca le attività create dall'utente, `SuspiciousScheduler` flagga quelle che eseguono comandi sospetti, e il parser di Rio estrae comandi e argomenti dai file XML delle attività.
  * **Comando ManualTasks (N0LW):**
  *   [Guida allo script](https://i.e-z.host/j1nmkky2iz2dyye.jpg)

      ```powershell
      powershell -Command "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/nolww/project-mohr/refs/heads/main/ManualTasks.ps1')"
      ```
  * **Comando SuspiciousScheduler (N0LW):**
  *   [Guida allo script](https://i.e-z.host/x8niii7khridy18.jpg)

      ```powershell
      powershell -Command "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/nolww/project-mohr/refs/heads/main/SuspiciousScheduler.ps1')"
      ```
  * **Comando Task Parser (Rio):**
  *   [Guida allo script](https://i.e-z.host/r1djkp65t0qd9dd.jpg)

      ```powershell
      powershell -Command "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/ObsessiveBf/Task-Scheduler-Parser/main/script.ps1')"
      ```

***

**Categoria: Utility e Raccolta Informazioni**

* **RedLotus HardDiskVolume Converter**
  * **Autore:** bacanoicua / Red Lotus
  * **Scopo:** Converte i percorsi in formato `\Device\HarddiskVolumeX` (comuni nei log del DPS) in percorsi con lettera di unità standard (es. `C:\...`), rendendoli leggibili e utilizzabili.
  * [Guida allo script](https://i.e-z.host/gm22j1pchnhry09.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/bacanoicua/Screenshare/main/RedLotusHardDiskVolumeConverter.ps1)
      ```
* **Services.ps1 (Lilith-PS)**
  * **Autore:** praiselily
  * **Scopo:** Raccoglie e visualizza un riepilogo dettagliato delle informazioni di sistema, tra cui orario di avvio, uptime, drive connessi, stato dei servizi critici, impostazioni di registro e cronologia degli eventi (cancellazioni, shutdown, cambi di orario).
  * [Guida allo script](https://i.e-z.host/q07hz9q7b7c4ux9.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://raw.githubusercontent.com/praiselily/lilith-ps/refs/heads/main/Services.ps1)
      ```
* **Alt Account Finder**
  * **Autore:** Red Lotus Community
  * **Scopo:** Scansiona le directory di gioco e i file di log alla ricerca di stringhe (come "user" o "username") per trovare prove di account alternativi.
  * [Guida allo script](https://i.e-z.host/7540s9neco4lk28.jpg)
  *   **Comando di Esecuzione:**

      ```powershell
      powershell Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass && powershell Invoke-Expression (Invoke-RestMethod https://pastebin.com/raw/LBGh2Cyb)
      ```
