## Yksikkötestauksen perusteet ja koodin laatu (DL su 26.1. klo 23:55)

Tällä viikolla tutustumme yksikkötestaukseen ja testaamme valmista virheellisesti toimivaa ja tyylillisesti heikosti toteutettua metodia. Tutustumme lisäksi koodin laatuun vaikuttaviin tekijöihin ja sovellamme niitä annetun valmiin koodin parantamiseksi.

### Koodin laatu

Tähän asti olet ohjelmointiopinnoissasi kenties keskittynyt lähinnä saamaan ohjelmasi toimimaan tehtävänannon mukaisesti kiinnittämättä suurempaa huomiota sen ymmärrettävyyteen tai jatkokehitettävyyteen. Ammatillisessa ohjelmistokehityksessä on harvinaista, että koodia kirjoitettaisiin kerran ja vain yhden kehittäjän toimesta. Päinvastoin, koodia kirjoitetaan isoissa tiimeissä, joissa kehittäjät vaihtuvat ja olemassa oleviin ominaisuuksiin tehdään jatkuvasti muutoksia. 

Tulet itse jatkokehittämään jonkun toisen vuosia sitten kirjoittamaa koodia, aivan kuten joku muu tulee jatkokehittämään sinun koodiasi. Tällöin on erittäin tärkeää, että koodi on muokattavissa ilman odottamattomia rikkoutumisia ja että muut kehittäjät ymmärtävät toistensa koodia ja pystyvät muokkaamaan sitä uusien vaatimusten mukaiseksi.

---

### Suositellut materiaalit

#### Kalvot:

[Johdanto yksikkötestaukseen](https://haagahelia.sharepoint.com/:p:/t/Ohjelmointi2/EWUtzb5VgiFHpudvOuDYRSUBEUziXja02btfg2bYoNV_ug?e=GhRhpc) (vaatii kirjautumisen 🙁)

#### Videot:

[**JUnit-testin luonti ja assertiot**](https://video.haaga-helia.fi/media/JUnit-testin+luonti+ja+assertiot/0_pl76xbuy) 9:21

Testiluokan luominen, annotaatiot, testimetodit, assertiot ja testin suorittaminen.

[**Luokan testaaminen JUnit-työkalulla**](https://video.haaga-helia.fi/media/Luokan+testaaminen+JUnit-ty%C3%B6kalulla/0_1gkcscbe) 7:10

Luokan metodien testaaminen erillisen testiluokan ja JUnit-kirjaston avulla.

[**Testin alustaminen ja @BeforeEach**](https://video.haaga-helia.fi/media/Testin+alustaminen+ja+%40BeforeEach/0_poklvdms) 3:54

Useille testimetodeille yhteisten alustustoimenpiteiden tekeminen erillisessä alustusmetodissa.

**Edistynyttä sisältöä:** [Testivetoinen kehitys: palindromin tarkastaminen](https://video.haaga-helia.fi/media/Testivetoinen+kehitysA+palindromin+tarkastaminen/0_m8y5zv8k) 26:15

Tässä videossa koodataan logiikka palindromien tunnistamiseksi testivetoisen kehittämisen menetelmällä. Yksittäisen metodin toteutus jaetaan erillisiin vaiheisiin, joiden toteuttaminen aloitetaan testin kirjoittamisella. Kun yksittäinen testitapaus saadaan läpi, jatketaan kirjoittamalla seuraava testitapaus ja sen toteutus, ja tätä toistetaan, kunnes metodi lopulta toimii toivotulla tavalla.

Tutustu lisäksi MIT:n sivuun, videoihin ja tehtäviin osoitteessa: [https://web.mit.edu/6.005/www/fa16/classes/04-code-review/](https://web.mit.edu/6.005/www/fa16/classes/04-code-review/)

---

### Tehtävä

Tämän osion tehtävänäsi on toteuttaa JUnit-testitapaukset MIT:n esimerkkikoodille "dayOfYear" ([https://web.mit.edu/6.005/www/fa16/classes/04-code-review/](https://web.mit.edu/6.005/www/fa16/classes/04-code-review/)). Esimerkkikoodi on saatavilla kokonaisena luokkana kurssin Git-repositoriossa tiedostossa [src/yksikkotestaus/DayOfYear.java](src/yksikkotestaus/DayOfYear.java). Yksinkertaisuudessaan metodi saa parametreinaan päivämäärän kolmena kokonaislukuna, ja palauttaa kokonaisluvun väliltä 1-366, joka on annetun päivämäärän järjestysnumero kyseisenä vuonna.

#### **Vaihe 1: kirjoita dayOfYear-metodille JUnit-yksikkötestit**

Kirjoita testiluokka DayOfYearTest, jossa hyödynnät JUnit-testikirjastoa testataksesi valmiin metodin toimivuuden osoittamiseksi vaadittavat testitapaukset. Testiluokan tulee osoittaa testattavan luokan virheellisyys (vinkki: liittyy karkausvuoteen).

#### **Vaihe 2: korjaa dayOfYear-luokan bugi(t)**

Korjattuasi bugi(t) edellisessä vaiheessa kirjoittamasi testiluokan kaikkien testien tulee mennä hyväksytysti läpi.

#### **Vaihe 3: Muokkaa koodi hyvien ohjelmointikäytäntöjen mukaiseksi**

`dayOfYear`-metodissa on käytetty ohjelmoinnin perusrakenteita melko suppeasti, ja se koostuukin erittäin pitkästä `if-else`-rakenteesta ja kokonaislukujen yhteenlaskuista. Tehtäväsi tässä vaiheessa on refaktoroida koodi hyvien ohjelmointitapojen mukaiseksi. Refaktoroidun koodin tulee siis olla ymmärrettävämpää ja ylläpidettävämpää.

Tutustu vähintään seuraaviin "koodin hajuihin" esimerkkikoodissa ja parantele koodia parhaasi mukaan:

- Don't Repeat Yourself
- Comments Where Needed
- Fail Fast
- Avoid Magic Numbers
- One Purpose For Each Variable

Edellä mainittu lista on käyty tämän esimerkkikoodin yhteydessä läpi osoitteessa https://web.mit.edu/6.005/www/fa16/classes/04-code-review/, mutta voit käyttää myös muita lähteitä. Saat halutessasi muuttaa metodin parametreja esimerkiksi siten, että int-arvojen sijaan käytät enum-arvoja tai olioita.

### Tehtävän palauttaminen

Palauta luokat `DayOfYear` ja `DayOfYearTest` Teamsissa olevaan palautuslaatikkoon sunnuntaihin 26.1. klo 23:55 mennessä.

**Huom!** Javan `LocalDate`-luokassa on olemassa valmis toteutus `dayOfYear`-laskennalle. Oikeassa ohjelmistoprojektissa sinun tulisi ehdottomasti käyttää tätä, eikä yrittää toteuttaa omaa versiotasi. Tämän harjoituksen tavoitteena on kuitenkin opetella jäsentämään koodi uudella tavalla, eikä valmiin toteutuksen olemassaolo ole sen suhteen haitallista.

**Huom!** Javan `java.time`-paketista löytyvät `Month`- ja `Year`-luokat voivat olla refaktoroinnissa  erittäin hyödyllisiä.

---

### Loppusanat

Vaikka ohjelmiston kaikki osat toimisivat itsenäisinä täydellisesti, voi järjestelmä silti olla kokonaisuutena viallinen. Siksi ohjelmistoprojekteissa testaus ei usein rajoitu pelkkään yksikkötestaamiseen, vaan menetelminä käytetään mm. integraatiotestejä ja järjestelmätestejä. Katso esimerkiksi Googlen kuvahaku humoristisista tilanteista, joissa yksittäiset asiat toimivat, mutta lopputulos ei silti täytä odotuksia: "[two unit tests, no integration tests](https://www.google.com/search?q=two%20unit%20tests,%20no%20integration%20tests&amp;tbm=isch)".