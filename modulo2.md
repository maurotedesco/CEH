markdown
# Modulo 2: Footprinting and Reconnaissance (CEHv13)

Ecco un elenco dettagliato di siti web e strumenti chiave utilizzati per le attività di footprinting e reconnaissance. Ricorda che l'obiettivo è raccogliere informazioni sul bersaglio in modo **passivo** (senza interazione diretta) o **semi-passivo** (interazione minima e difficile da tracciare).

## 1. Motori di Ricerca Generici (Informazioni Pubbliche & Google Dorking)

Questi sono fondamentali per cercare informazioni pubblicamente disponibili e sfruttare tecniche di ricerca avanzata (Google Dorking).

*   **Google:** `https://www.google.com/` (Il motore di ricerca più potente per query generali e dorking avanzato).
*   **Bing:** `https://www.bing.com/` (Un'alternativa valida con diverse caratteristiche di indicizzazione).
*   **DuckDuckGo:** `https://duckduckgo.com/` (Motore di ricerca orientato alla privacy, utile per ricerche che non vuoi siano tracciate).

## 2. Siti per la Ricerca di Informazioni su Domini e DNS

Questi strumenti aiutano a scoprire dettagli sul dominio bersaglio, come proprietario, server DNS, indirizzi IP associati e record vari.

*   **WHOIS Lookup (Generico):** Siti come `https://whois.com/` o `https://lookup.icann.org/` (Per ottenere dettagli sulla registrazione del dominio: registrante, contatti, nameserver, date importanti).
*   **MXToolbox:** `https://mxtoolbox.com/` (Eccellente per controllare i record DNS (MX, A, NS, SOA), testare server e-mail e controllare blacklist).
*   **DNSDumpster:** `https://dnsdumpster.com/` (Fornisce una mappa visuale e un elenco dettagliato dei record DNS e degli host correlati a un dominio).
*   **ViewDNS.info:** `https://viewdns.info/` (Offre una vasta gamma di strumenti di lookup DNS e IP in un unico posto).

## 3. Siti per la Ricerca di Informazioni su IP e Range di Rete

Utili per identificare a chi appartengono blocchi di indirizzi IP e la loro posizione geografica.

*   **Registri Regionali di Internet (RIRs):** Esempi includono:
    *   **ARIN:** `https://www.arin.net/` (Nord America)
    *   **RIPE NCC:** `https://www.ripe.net/` (Europa, Medio Oriente, Asia Centrale)
    *   **APNIC:** `https://www.apnic.net/` (Asia Pacifico)
    *   **LACNIC:** `https://www.lacnic.net/` (America Latina e Caraibi)
    *   **AFRINIC:** `https://www.afrinic.net/` (Africa)
    (Permettono di cercare l'organizzazione a cui è stato assegnato un blocco IP).
*   **IP Location Sites:** Siti come `https://www.iplocation.net/` (Per geolocalizzare un indirizzo IP su una mappa).

## 4. Archivi Web e Storia dei Siti

Permettono di vedere come un sito web appariva in passato.

*   **Internet Archive (Wayback Machine):** `https://archive.org/web/` (Archivia copie di pagine web nel tempo, utile per trovare contenuti rimossi o vecchie versioni).

## 5. Motori di Ricerca per Dispositivi Connessi (IoT, Server, ecc.)

Questi motori scansionano internet per trovare dispositivi, servizi esposti e porte aperte.

*   **Shodan:** `https://www.shodan.io/` (Il "motore di ricerca per l'Internet delle Cose", trova dispositivi basati su porte aperte, protocolli, città, ecc.).
*   **Censys:** `https://censys.io/` (Simile a Shodan, scansiona internet per raccogliere dati su host e certificati).

## 6. Siti e Strumenti per l'Analisi di Siti Web

Aiutano a identificare le tecnologie sottostanti utilizzate da un sito web.

*   **BuiltWith:** `https://builtwith.com/` (Rivela le tecnologie usate da un sito, come CMS, framework, server web, advertising, analytics, ecc.).
*   **Wappalyzer:** `https://www.wappalyzer.com/` (Estensione del browser che analizza le tecnologie di un sito visitato).
*   **Netcraft:** `https://www.netcraft.com/` (Offre report dettagliati sui siti, inclusa la storia dell'hosting, sistema operativo, server web, rating di sicurezza).

## 7. Framework e Risorse per l'OSINT (Open Source Intelligence)

Strumenti e risorse che facilitano la raccolta e l'organizzazione di informazioni da fonti aperte.

*   **OSINT Framework:** `https://osintframework.com/` (Una raccolta organizzata di link a vari strumenti e risorse OSINT).
*   *(Altri strumenti come Maltego, theHarvester ecc., spesso hanno siti web di progetto o repository GitHub, ma il Framework OSINT è un ottimo punto di partenza).*

## 8. Siti per la Ricerca su Social Media e Persone

Per raccogliere informazioni su individui o l'organizzazione bersaglio attraverso le loro presenze sui social network.

*   **LinkedIn:** `https://www.linkedin.com/` (Ideale per informazioni professionali su dipendenti e struttura aziendale).
*   **Twitter:** `https://twitter.com/` (Utile per opinioni, attività recenti, connessioni).
*   **Facebook:** `https://www.facebook.com/` (Informazioni personali, anche se la privacy può limitarne la visibilità).
*   *(Molti altri social media sono rilevanti a seconda del bersaglio).*

## 9. Siti per Verificare Breaches di Dati

Per scoprire se dati associati al bersaglio sono stati compromessi in passato.

*   **Have I Been Pwned:** `https://haveibeenpwned.com/` (Permette di cercare indirizzi email o numeri di telefono compromessi in data breaches noti).

## 10. Strumenti a Riga di Comando Comuni (Installati localmente, non siti web)

Anche se hai chiesto siti, è fondamentale menzionare gli strumenti da terminale usati nel footprinting.

*   `ping` (Verifica la raggiungibilità di un host - usalo con cautela nel footprinting passivo/semi-passivo).
*   `traceroute` / `tracert` (Mappa il percorso di rete verso un host - più "rumoroso" di `ping`).
*   `nslookup` / `dig` (Per eseguire query DNS e ottenere record specifici).
*   `whois` (Lo strumento da riga di comando per eseguire query WHOIS direttamente).
*   `theHarvester` (Spesso incluso in Kali Linux, automatizza la raccolta di email, subdomini, host da varie fonti pubbliche).

Spero questo formato in Markdown sia esattamente quello che cercavi! È un modulo ricco di strumenti e tecniche utili. Continua così! 👍
