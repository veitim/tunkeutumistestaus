# h2 Täysin Laillinen Sertifikaatti

## x) tiivistelmä

### OWASP 2021: OWASP Top 10:2021

*

A01:2021 – Broken Access Control

*

A10:2021 – Server-Side Request Forgery (SSRF)

*

### PortSwigget Academy:

Insecure direct object references (IDOR)

*

Path traversal

*

Server-side request forgery (SSRF)

*

Cross-site scripting

*

## a) Totally Legit Sertificate ja b) kettumaista

Aloitin asentamalla zaproxyn kali-virtuaalikoneeseeni komennolla "sudo apt-get install zaproxy".
Käynnistin ohjelman komennolla "zaproxy"

Navigoin Karvisen vinkeistä löytyvien ohjeiden avulla zapissa: Tools -> Options -> Network -> Server Certificate

![a](imagess/h2_a1.png)

Ja tallenna. Seuraavaksi menin firefox selaimen Privacy & Security asetuksiin, josta avasin sertifikaatit "view certificates..."

![a](imagess/h2_a2.png)

Täältä import.

![a](imagess/h2_a3.png)

Tänne laitetaan juuri tallennettu sertifikaatti.

![a](imagess/h2_a4.png)

Seuraavaksi konfiguroin firefoxin käyttämään zappia proxynä. Firefoxin asetuksista general välilehdeltä löytyi alhaalta networksettings minne pääsi proxy osoitteen lisäämään.

![a](imagess/h2_a5.png)

Zapin dokumentaatiossa sanottiin, että yleensä localhost osoitteella mennään, joten tätä käytin (ip addr terminaaliin ja portti on 8080)
Firefox ei näköjään suostu tätä osoitetta käyttämään proxynä (lukee suoraan asetuksissa). Joten asensin tämän tehtävän yhteydessä myös foxyproxyn.

Firefoxista lisäosien kautta hain foxyproxyä ja asensin standard version.

![a](imagess/h2_a6.png)

Laitoin asetuksista samat proxy asetukset, kuin firefoxista eli localhost osoitteen. Lisäsin kanssa "proxy by patterniin" portswigger.net osoitteen, koska en halua käyttää proxyä muiden sivujen kautta (sekä Teron materiaaleissa näin lukee).

![a](imagess/h2_a7.png)

Sitten aktivoin proxy by patternsin.

![a](imagess/h2_a10.png)

Nyt proxy toimii vain portswiggerin kohdalla. Eli zappiin ei tule tietoa muista sivustoista. Testaan vielä.

![a](imagess/h2_a8.png)

Wikipedian avattua ei tule mitään uutta.

![a](imagess/h2_a9.png)

Portswigger ilmaantuu pyyntöihin. Eli nyt on zappi ja foxyproxy.

## PortSwigger labrat

### c) PortSwigger - Cross Site Scripting: Reflected XSS into HTML context with nothing encoded

Tarkoituksena 

### d) PortSwigger - Cross Site Scripting: Stored XSS into HTML context with nothing encoded

### e) PortSwigger - Path Traversal: File path traversal, simple case

### f) PortSwigger - Path Traversal: File path traversal, traversal sequences blocked with absolute path bypass

### h) PortSwigger - Path Traversal: File path traversal, traversal sequences stripped non-recursively

### i) PortSwigger - Insecure Direct Object Reference (IDOR): Insecure direct object references

### j) PortSwigger - Server Side Request Forgery (SSRF): Basic SSRF against the local server

### k) PortSwigger - Server Side Template Injection (SSTI): Server-side template injection with information disclosure via user-supplied objects

## l)

## m)

## Lähteet:

Karvinen, T. 2024: Tunkeutumistestaus. Luettavissa: (https://terokarvinen.com/tunkeutumistestaus/) Luettu 8.4.2025

OWASP Top 10:2021: A01:2021 – Broken Access Control. Luettavissa: (https://owasp.org/Top10/A01_2021-Broken_Access_Control/) Luettu 8.4.2025

OWASP Top 10:2021: A10:2021 – Server-Side Request Forgery (SSRF). Luettavissa: (https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29/) Luettu 8.4.2025

PortSwigger: Insecure direct object references (IDOR). Luettavissa: (https://portswigger.net/web-security/access-control/idor) Luettu 8.4.2025

PortSwigger: Path traversal. Luettavissa (https://portswigger.net/web-security/file-path-traversal) Luettu 8.4.2025

PortSwigger: Server-side request forgery (SSRF). Luettavissa (https://portswigger.net/web-security/ssrf) Luettu 8.4.2025

PortSwigger: Cross-site scripting. Luettavissa (https://portswigger.net/web-security/cross-site-scripting) Luettu 8.4.2025

Zap by checkmarx: Configuring Proxies. Luettavissa: (https://www.zaproxy.org/docs/desktop/start/proxies/) Luettu 8.4.2025
