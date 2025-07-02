
# Modulo 3: Scanning Networks (CEHv13)

Questo modulo si concentra sull'interazione diretta o semi-diretta con il network del bersaglio per scoprire host attivi, porte aperte, servizi in esecuzione e potenziali vulnerabilità. La maggior parte degli strumenti sono software installati localmente.

## 1. Strumenti Principali di Network e Port Scanning

Questi sono i cavalli di battaglia per scoprire cosa c'è "vivo" su una rete e quali porte sono accessibili.

*   **Nmap (Network Mapper):**
    *   **Sito Ufficiale:** `https://nmap.org/`
    *   **Descrizione:** Lo scanner di rete più famoso e versatile. Utilizzato per host discovery, port scanning, OS detection (identificazione del sistema operativo), service version detection (identificazione della versione dei servizi) e molto altro tramite il suo scripting engine (NSE). È uno strumento a riga di comando ma include anche una GUI chiamata Zenmap.
*   **hping3:**
    *   **Sito Ufficiale / Repository:** Spesso si trova su repository come `https://github.com/antirez/hping3` (Antirez è l'autore originale).
    *   **Descrizione:** Un packet crafter e analizzatore di rete basato su riga di comando. Permette di creare e inviare pacchetti TCP/IP personalizzati. Utile per firewalking, scanning avanzato, denial-of-service testing (con cautela e solo in ambienti autorizzati!).
*   **Netcat (nc):**
    *   **Sito Ufficiale / Informazioni:** È uno strumento standard presente nella maggior parte delle distribuzioni Linux/Unix e versioni di Windows. Non ha un singolo "sito ufficiale" del progetto principale facilmente identificabile come nmap. Puoi cercare documentazione per la tua versione (es. `man nc` su Linux). Versioni come `https://nc110.sourceforge.io/` o `https://nmap.org/ncat/` (Ncat è la versione di Netcat inclusa con Nmap) sono punti di riferimento.
    *   **Descrizione:** Chiamato il "coltellino svizzero" del networking. Può leggere e scrivere dati attraverso connessioni di rete usando i protocolli TCP o UDP. Utilissimo per banner grabbing manuale, connettersi a porte, trasferire file, creare shell inverse/bind.
*   **Telnet:**
    *   **Sito Ufficiale / Informazioni:** Un protocollo e strumento client molto vecchio, solitamente preinstallato nei sistemi operativi (anche se il server è sconsigliato per sicurezza). Cerca documentazione specifica per il tuo OS (es. `man telnet`).
    *   **Descrizione:** Può essere usato per testare la connessione a una porta TCP e per eseguire un basic banner grabbing (se il servizio invia un banner all'inizio della sessione). Meno potente di Netcat per questo scopo, ma semplice.

## 2. Strumenti di Vulnerability Scanning

Questi strumenti automatizzano la ricerca di vulnerabilità note su host e servizi.

*   **Nessus:**
    *   **Sito del Prodotto (Tenable):** `https://www.tenable.com/products/nessus`
    *   **Descrizione:** Uno dei principali scanner di vulnerabilità commerciali. Identifica vulnerabilità, configurazioni errate e problemi di sicurezza. Esiste una versione gratuita molto capace per uso non commerciale (Nessus Essentials).
*   **OpenVAS (Open Vulnerability Assessment System) / Greenbone Community Edition:**
    *   **Sito Ufficiale (Greenbone Networks):** `https://www.greenbone.net/en/openvas/` o `https://www.greenbone.net/en/community-edition/`
    *   **Descrizione:** Potente framework open-source per la scansione delle vulnerabilità. Spesso trovato preinstallato o facilmente installabile su distribuzioni come Kali Linux (parte della Greenbone Community Edition).
*   *(Nota: Altri scanner commerciali come Rapid7 InsightVM/Nexpose o Qualys sono spesso menzionati per completezza, ma Nessus e OpenVAS sono i più probabili da usare nei lab CEH).*

## 3. Database di Vulnerabilità (Per capire cosa cercano gli scanner)

Questi siti non sono strumenti di scansione, ma sono fondamentali per capire le vulnerabilità che gli scanner cercano e riportano.

*   **CVE (Common Vulnerabilities and Exposures):**
    *   **Sito Ufficiale (MITRE):** `https://cve.mitre.org/`
    *   **Descrizione:** Un dizionario pubblico di vulnerabilità di sicurezza informatica conosciute. Ogni vulnerabilità ha un identificatore CVE univoco (es. CVE-2023-XXXXX).
*   **NVD (National Vulnerability Database):**
    *   **Sito Ufficiale (NIST):** `https://nvd.nist.gov/`
    *   **Descrizione:** Costruito sul database CVE, il NVD aggiunge analisi, punteggi di gravità (CVSS - Common Vulnerability Scoring System) e riferimenti. È una risorsa ricca per ricercare dettagli su specifiche CVE.

## 4. Strumenti di Anonymization (Per mascherare la sorgente della scansione)

Usati per rendere più difficile tracciare le scansioni alla sorgente originale.

*   **Tor Project:**
    *   **Sito Ufficiale:** `https://www.torproject.org/`
    *   **Descrizione:** Fornisce il software e gestisce la rete Tor, che consente comunicazioni anonime tramite una rete decentralizzata di relay. Utile per navigazione anonima o per instradare il traffico degli strumenti (se configurati correttamente) per mascherare la sorgente.
*   *(Nota: Anche VPN e proxy server sono discussi come concetti, ma non c'è un singolo sito web per tutti i fornitori).*

## 5. Strumenti a Riga di Comando Comuni (Ricapitolazione e Contesto)

Alcuni strumenti base dei moduli precedenti sono ancora rilevanti qui.

*   `ping` (Utile per l'host discovery iniziale, anche se meno "stealthy").
*   `traceroute` / `tracert` (Mappa il percorso di rete verso un host, può rivelare informazioni sull'infrastruttura di rete).
*   `nslookup` / `dig` (Per eseguire query DNS e ottenere record specifici).
*   `whois` (Lo strumento da riga di comando per eseguire query WHOIS direttamente).
*   `theHarvester` (Spesso incluso in Kali Linux, automatizza la raccolta di email, subdomini, host da varie fonti pubbliche).
