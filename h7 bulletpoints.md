### Read/watch/listen and summarize

#### 1) Schneier 2015: Applied Cryptography, 20ed: Chapter 1: Foundations:

##### 1.1 Terminology

- Sender and Receiver: Viesti pitää saada perille niin, ettei ulkopuolinen pääse lukemaan sitä.

- Messages and Encryption: Selkokielinen viesti (plaintext/cleartext) salataan salaustekstiksi (ciphertext) salausalgoritmilla (encryption). Prosessi käännetään purkualgoritmilla (decryption) takasisin. Kryptografia tarkoittaa viestien suojaamisen taitoa ja tiedettä.kryptoanalyysi puolestaan niiden murtamista.

- Authentication, Integrity, and Nonrepudiation: Luottamuksellisuuden lisäksi kryptografialta vaaditaan muutakin:

- viestin alkuperä pitää voida varmentaa (todennus)
- sen muuttumattomuus on voitava tarkistaa (eheys)
- lähettäjä ei saa pystyä jälkikäteen kiistämään viestiään (kiistämättömyys)

Nämä ovat tietokoneviestinnän perusvaatimuksia.

- Algorithms and Keys: Turvallisuus ei perustu algoritmin salassapitoon vaan avaimeen eli algoritmi voi olla julkinen. Salauksessa käytetään yhtä tai kahta avainta. Kryptosysteemi = algoritmi + mahdolliset plaintextit, ciphertextit ja avaimet.

- Symmetric Algorithms: Yleisin salaustyyppi symmetrinen algoritmi, jossa lähettäjällä ja vastaanottajalla on sama salainen avain eli kuin yhteinen lukkokoodi. Algoritmit toimivat kahdella tavalla: virtasalaimet (stream algorithms) ja lohkosalaimet (block algorithms).

- Public-Key Algorithms: Julkisen avaimen salauksessa on kaksi avainta: julkinen avain jonka voi jakaa kaikille ja jolla kuka tahansa voi salata viestin, sekä yksityinen avain jonka vain vastaanottaja tietää ja jolla viesti puretaan. Vaikka avaimet liittyvät matemaattisesti toisiinsa, yksityistä avainta ei käytännössä pysty laskemaan julkisesta. Tämä ratkaisee symmetrisen salauksen keskeisen ongelman: salaista avainta ei tarvitse enää erikseen sopia etukäteen.

- Cryptanalysis: Hyökkäykset luokitellaan käytettävissä olevan tiedon mukaan — pelkästä salatekstistä valittuun selkokieleen. Kerckhoffsin periaatteen mukaan turvallisuuden on perustuttava yksinomaan avaimeen, ei algoritmin salassapitoon eli paras algoritmi on julkinen ja silti murtamaton.

- Security of Algorithms: Algoritmi on riittävän turvallinen, kun sen murtamisen kustannus ylittää suojattavan datan arvon. Murtaminen voi tarkoittaa avaimen löytämistä (täydellinen murtaminen) tai pelkän selkotekstin paljastumista. Ainoastaan kertakäyttöinen avain on ehdottoman turvallinen.

- Historical Terms: Koodi salaa kokonaisia sanoja tai lauseita, salakirjoitus (cipher) yksittäisiä merkkejä tai bittejä ja toimii siksi joustavammin missä tahansa tilanteessa.

##### 1.4 Simple XOR

XOR-operaatio on yksinkertainen bittitasin laskutoimitus, joknka keskeinen ominaisuus on se, että sama avain salaa ja purkaa viestin. Algoritmia käytetään paljon kaupallisissa ohjelmistoissa, mutta se on täysin murrettavissa minuuteissa . Avainpituus selviää tilastollisella menetelmällä (coincidence index), minkä jälkeen selkoteksti paljastuu suoraan. XOR suojaa korkeintaan uteliailta sivullisilta, ei todelliselta kryptoanalyytikolta.

##### 1.7 Large Numbers

Kryptografiassa käytetyt luvut, kuten 2¹²⁸ mahdollista avainta ovat niin isoja, että ne on vaikea edes hahmottaa. Kirjassa havainnollistettiin niitä fysikaalisilla vertailukohdilla: esimerkiksi maailmankaikkeuden atomien määrä on vain noin 2²⁶⁵. Riittävän suuri avainavaruus siis tekee raa an voiman hyökkäyksen kirjaimellisesti maailmankaikkeuden mittakaavassa mahdottomaksi.

#### Karvinen 2024: Python Basics for Hackers

- Käytä REPL:iä ja F5-käännöstä nopean palautesilmukan saamiseksi esimerkeissä testattiin piniä asioita kerrallaan

- Numeromuunnokset (ord(), chr(), hex(), bin()) ja str/bytes-ero ovat kryptohaasteissa välttämättömiä perustaitoja

- XOR (^) bittitasolla on yksinkertaisen salauksen ydin: sama avain salaa ja purkaa kuten kirjassa jo mainittiin

- Frekvenssitaulukot (ETAOIN SHRDLU) ja tulosten pisteytyksellä lajittelu auttavat murtamaan salauksia automaattisesti

- Debuggaukseen riittää usein pelkkä tulostus; monimutkaisiin tapauksiin breakpoint() ja ipdb

#### Karvinen 2024: Get Started Micro Editor

- Micro on koodaajille suunnattu teksti editori, jossa on helpoin TUI. Se tarjoaa silti IDE:n kaltaisia ominaisuuksia
- Asennus onnistuu `sudo apt-get install` komennolla ja hyödylliset lisäosat (runit, jump ja palettero)


####  Karvinen 2024: Getting Started with Cryptopals using Python

- Cryptopals on käytännönläheinen harjoitussarja salausten, tehtävissä ei tarvitse olla maisteri tai tohtori, mutta koodaaminen pitää hallita

- tehtävät kannattaa tehdä järjestyksessä eikä kopioida valmiita vastauksia, harjoituksen pointti on oppia itse murtamaan salauksia

- Vinkkejä kannattaa katsoa vasta kun on ensin yrittänyt itse; jos vinkit eivät riitä, verkosta löytyy valmiita ratkaisuja useilla kielillä

- Suositeltava ympäristö: Python, Debian/Kali ja micro-editori



### Lähteet: 

Karvinen, T. 2024. Get Started Micro Editor. Luettavissa: https://terokarvinen.com/get-started-micro-editor/. Luettu: 7.3.2026.

Karvinen, T. 2024. Getting Started with Cryptopals using Python. Luetavissa: https://terokarvinen.com/getting-started-python-cryptopals/. Luettu: 7.3.2026.

Karvinen, T. 2024. Python Basics for Hackers. Luettavissa: https://terokarvinen.com/python-for-hackers/. Luettu: 7.3.2026.

Schneier, B. 2015. Applied Cryptography: Protocols, Algorithms and Source Code in C. 20. painos. John Wiley & Sons, Inc. E-kirja. Luettu: 7.3.2026.




