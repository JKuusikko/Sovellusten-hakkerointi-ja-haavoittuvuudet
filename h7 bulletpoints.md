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



