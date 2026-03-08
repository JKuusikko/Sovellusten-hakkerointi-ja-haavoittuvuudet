#### 1. Convert hex to base64


Aloitin tehtävän menemällä sivustolle: https://cryptopals.com/sets/1. Klikkasin kohtaa 1. Googletin convert hex to base64 ja tutkin siellä ratkaisuja (StackFlower), kokeilin seuraavaa koodia:

<img width="1070" height="920" alt="image" src="https://github.com/user-attachments/assets/1f416278-f68e-4931-bbe9-c3156812b4b6" />

Koodi muuntaa tallennetun teksti muuttujan aluksi hex tavuiksi, jonka jälkeen muuntaa tavut base64 tekstiksi.

Ajoin koodin: 

<img width="1050" height="200" alt="image" src="https://github.com/user-attachments/assets/f68b427d-00df-4d06-9df4-24a5e7561dab" />

ja näytti olevan oikein, tehtävä oli aika helppo.

#### 2. Fixed XOR

Avasin tehtävän ja rupesin netistä tutkimaan asiaa StackFlower sivustolta sain apua tehtävään ja tulin ratkaisuun: 

<img width="1074" height="418" alt="image" src="https://github.com/user-attachments/assets/2f37a70c-2504-46ec-968b-bffc777c2765" />

XOR vertaa kahta bittiä:
 1 + 1 = 0
 1 + 0 = 1

koodi ottaa kaksi hex-stringiä, muuntaa ne tavuiksi ja XOR jokaisen tavuparin yhteen.

Suorintin ohjelman ja tulosti:

<img width="720" height="246" alt="image" src="https://github.com/user-attachments/assets/1abae835-9bb7-4713-a48f-355ad0a07e5c" />

Näyttäisi olevan oikein.

#### 3. Single-byte XOR cipher

Viesti on salattu XORaamalla yksi ainoa merkki jokaiseen tavuun. Sama homma kuin edellisissä kohdissa, kun tutkin asiaa niin se oli selvä, että tehtävä oli haastavempi: kuitenkin netin avulla loin ratkaisun: 

<img width="1064" height="540" alt="image" src="https://github.com/user-attachments/assets/5b173c20-2da2-4cd6-8d81-afc2aab6d94d" />

Koodi kokeilee kaikki 256 mahdollista avainta:
avain 0:  XOR jokainen tavu numerolla 0 → onko se englantia?
avain 1:  XOR jokainen tavu numerolla 1 → onko se englantia?

Pisteytys:
Englannissa yleisimmät kirjaimet ovat e t a o i n s h r d l u. Jos purettu viesti sisältää paljon näitä → todennäköisesti englantia.

Lyhyesti: kokeile kaikki avaimet → pistytä → paras pisteet = oikea avain

ajoin ohjelman ja :

<img width="480" height="98" alt="image" src="https://github.com/user-attachments/assets/32dc58da-fdf2-4bc6-b809-e570726cb902" />

En tiedä onko ratkaisu oikein, mutta ainakin teksti on järkevä.

#### 4. Detect single-character XOR

Latasin tiedoston komennolla `wget https://cryptopals.com/static/challenge-data/4.txt`

Netistä saadulla avulla loin koodin:

<img width="1064" height="794" alt="image" src="https://github.com/user-attachments/assets/2df8446d-d997-46c2-891d-2ba496095581" />

Sama homma kuin 3. kohdassa eli koodi käy läpi tiedoston:
rivi 1:  kokeile kaikki 256 avainta → pistytä
rivi 2:  kokeile kaikki 256 avainta → pistytä

Rivit käyty läpi → parhaat pisteet kaikista = vastaus

Suorin koodin ja lopputulos:

<img width="474" height="106" alt="image" src="https://github.com/user-attachments/assets/749f2903-c0ce-40db-bfa1-78b65ea9e1c9" />

#### 5. Implement repeating-key XOR

Tehtävässä pitää tehdä nyt päin vastoin eli salataan teksti tietyllä avaimella "ICE". Jokainen kirjain XORrataan vuorotellen. Alla oleva koodi käy läpi jokaisen kirjaimen teksitstä ja valitsee oikean avaimen kirjaimen. Lopuksi tulos muunnetaan hex-muotoon:

<img width="1060" height="360" alt="image" src="https://github.com/user-attachments/assets/b28f8c78-608f-4d27-a03a-872617d87798" />

Kun suoritin koodin:

<img width="1042" height="132" alt="image" src="https://github.com/user-attachments/assets/aea7e847-2d25-4ba4-87c8-100f555015fd" />

Näytti olevan sama kuin nettisivulla.

Jatkan vielä myöhemmin loppu vaiheet, aihe oli erittäin mielenkiintoinen ja haluaisin tästä oppia vielä lisää. Tehtävät olivat tarpeeksi haastavia ja ne vei aikaa, kuitenkaan ei liikaa.

### Lähteet:

Cryptopals. s.a. the cryptopals crypto challenges: Crypto Challenge Set 1. Luettavissa: https://cryptopals.com/sets/1. Luettu: 7.3.2026.

Karvinen, T. 2026. Application hacking. Luettavissa: https://terokarvinen.com/application-hacking/. Luettu: 7.3.2026.

StackOverflow. Artikkelit: Hex to Base64 conversion in Python, Why XOR function does not print out the expected hex value & Single-Byte XOR Cipher (python). Luettavissa : https://stackoverflow.com/questions. Luettu: 7.3.2026.

Tekoäly: Tekoälyä käytin hankalampien käsitteiden selventämiseen.












