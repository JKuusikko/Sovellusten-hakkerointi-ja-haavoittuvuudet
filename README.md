# Sovellusten hakkerointi ja haavoittuvuudet (Application Hacking)

Tässä repositoriossa on **Sovellusten hakkerointi ja haavoittuvuudet** -kurssin (ICI012AS3A)
tehtäväraportit, joka on edistynyt eettisen hakkeroinnin kurssi, joka keskittyy sovellusten
haavoittuvuuksien löytämiseen ja korjaamiseen sekä käänteismallinnukseen (reverse
engineering) — tavoitteena löytää viat ennen kuin rikolliset ehtivät.

## Harjoitukset
Tehtävät on dokumentoitu tiedostoihin **h1–h7**: jokaisessa tehtävänanto, käytetyt
komennot ja työkalut, havainnot ja tulokset sekä merkityt lähteet.

| Tiedosto | Aihe | Keskeiset työkalut / tekniikat |
|----------|------|-------------------------------|
| h1 | Standardit ja viitekehykset | OWASP, raportointi |
| h2 | Web-haavoittuvuuksien murtaminen ja korjaaminen lähdekoodista | Broken Access Control, SQL-injektio, ffuf, PortSwigger Labs |
| h3 | Staattinen analyysi ilman lähdekoodia | `strings`, binäärien tarkastelu, obfuskointi (C) |
| h4 | Käänteismallinnus (disassembly) | Ghidra, binäärin muokkaus, NoraCodes crackmes |
| h5 | Dynaaminen analyysi ja debuggaus | gdb, crackme-tehtävät |
| h6 | Sulautetut järjestelmät ja tiedostojen kerrosanalyysi | binwalk, JADX, APK/bytecode-analyysi |
| h7 | Kryptografia ja salauksen murtaminen | Cryptopals Set 1, XOR, AES (ECB), Python |

## Osaaminen
- Web-sovellusten haavoittuvuuksien löytäminen **ja korjaaminen lähdekoodista**
- Staattinen analyysi: tiedon kaivaminen binääreistä ennen ajoa (`strings`, Ghidra)
- Käänteismallinnus ja binäärien muokkaus ilman lähdekoodia
- Dynaaminen analyysi ja debuggaus (gdb)
- Tiedostojen ja pakettien analyysi (binwalk, APK-purku: JADX, bytecode-viewer)
- Salauksen murtaminen tavallisten ohjelmointivirheiden kautta (XOR, AES-ECB)

## Ohjelmointi
Kurssi edellyttää ohjelmointitaitoja: koodin lukemista ja kirjoittamista (mm. C ja
Python) sekä haavoittuvuuksien korjaamista lähdekooditasolla.

## Vastuullisuus
Kaikki harjoitukset on tehty luvallisesti kurssin harjoitusmaaleissa ja -ympäristöissä.
Esitetyt tekniikat ovat sallittuja vain omissa tai erikseen luvan saaneissa järjestelmissä.

## Tekijä
Jari Kuusikko — github.com/JKuusikko
