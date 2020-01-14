# Ohjelmointi 2, SWD4TA033-3003 (Java, 5 op)

Tervetuloa kurssille!

Tällä opintojaksolla sovellamme aiemmin oppimianne ohjelmointitaitoja tietokantojen ohjelmallisessa käyttämisessä ja verkkopalveluiden toteuttamisessa. Syvennymme kielen syntaksin ja tarvittavien kirjastojen lisäksi myös ymmärrettävän koodin kirjoittamiseen, yksikkötestaukseen sekä versionhallinnan alkeisiin.

Opettajana kurssilla toimii Teemu Havulinna (`etunimi.sukunimi@haaga-helia.fi`).

## Viestintäkanavat

Tällä kurssilla käytetään viestintään pääasiassa Microsoftin Teams -palvelua. Teams on osoittautunut oivalliseksi tueksi itseopiskelussa ja se tarjoaa luontevamman kanavan kysyä ja keskustella kuin esimerkiksi Moodle. Jos jäät jumiin koodisi kanssa tai et ymmärrä materiaaleja tai tehtävänantoja, kysy rohkeasti vinkkejä Teamsissa. Todennäköisesti samaa ongelmaa pohtii kanssasi myös moni muu, joten lähetäthän sisältöä ja tehtävänantoja koskevat kysymykset yhteiselle kanavalle (eikä yksityisviestinä opettajalle).

Teamsissa voi myös esittää toivomuksia kurssin kehittämiseksi jo kurssin aikana niin yksityisviesteinä opettajalle kuin yhteisillä kanavilla. Tämä kurssi ei ole suinkaan valmis, vaan sitä kehitetään kurssin etenemisen mukaan. Tarpeen mukaan voimme järjestää esimerkiksi chat- tai videochat-aikoja etukäteen sovittavina ajankohtina.

Teams on saatavilla puhelimien sovelluskaupoista sekä työpöytäsovelluksena, tai voit käyttää sitä selaimen web-käyttöliittymässä ilman asennuksia. Kirjautuminen Teamsiin tapahtuu Haaga-Helian opiskelijatunnuksella.

* [Kurssin Teams-työtila](https://teams.microsoft.com/l/team/19%3aad52d8cfc8cd4d91869e5d911dcf7194%40thread.skype/conversations?groupId=7194424b-0503-4f63-af38-be4c5e1a9f48&tenantId=a9e39483-dd21-4c25-b848-2a625cff7939)
* [https://teams.microsoft.com/downloads](https://teams.microsoft.com/downloads)

## Palautettavat tehtävät

Kurssilla on pakollisia tehtäviä, jotka tulee palauttaa annettuihin määräaikoihin mennessä Teamsissa sijaitseviin palautuslaatikoihin. Tehtävät arvioidaan asteikolla täydennettävä/hyväksytty. Hyväksytyn tehtävän ei tarvitse olla oikein tehty täydellinen suoritus, vaan myös osittainen palautus hyväksytään, kunhan siinä näkyy riittävästi yritystä.

Tehtävän esimerkkiratkaisu julkaistaan aina seuraavalla viikolla. Myöhästyneitä tehtäviä ei oteta vastaan, jotta mallivastauksen julkaisu ei antaisi etua myöhästyneille palautuksille.

Useat kurssin tehtävät rakentuvat saman aihealueen ympärille ja edellisten tehtävien ratkaisuilla on merkitystä seuraavan tehtävän ratkaisemisen kannalta. Mikäli jokin tehtävä jää sinulta toimimattomaksi tai puutteelliseksi, voit hyödyntää malliratkaisua jatkaessasi seuraavan viikon tehtävän parissa. Merkitse kuitenkin myös mallivastauksen käyttäminen lähteeksi (ks. lähteiden käyttäminen).

Apua tehtävien tekoon on saatavissa kurssin Teams-kanavalla niin opettajalta kuin muiltakin opiskelijoilta.

## Kurssin harjoitustyö

Kurssin viimeisillä viikoilla sovellette aikaisempina viikkoina harjoiteltuja taitoja toteuttaessanne itsenäisesti oman tietokantapohjaisen web-sovelluksen. Harjoitustyö arvioidaan asteikolla 0-5 ja arvosanan perusteella määräytyy myös kurssin loppuarvosana. Vaikka harjoitustyö tehdään itsenäisesti, saatte keskustella siitä esimerkiksi Teamsissa kuten aikaisemmilla tehtäväkierroksilla. Kriteerinä on, että jokainen kirjoittaa itse oman koodinsa.

Tarkempi ohjeistus arvioinnin perusteista ja toteutettavan työn ominaisuuksista julkaistaan kurssin aikana.

## Tekniset työkalut

Kurssin ohjeet ja esimerkit on tehty Eclipse-sovelluskehittimellä ja Windows-käyttöjärjestelmällä, joten Linux- tai Mac-käyttäjien tulee soveltaa ohjeita ja esimerkkejä omien käyttöjärjestelmiensä mukaisesti.

Tässä vaiheessa on hyvä varmistaa, että käytössäsi on _"Eclipse IDE for Enterprise Java Developers"_, _"Eclipse Java EE IDE for Web Developers"_ tai vastaavalla nimellä kutsuttu jakelupaketti, joka sisältää verkkosovellusten tekoon tarvitut liitännäiset. Tämä selviää "Help"-valikosta kohdasta "About Eclipse IDE". Mikäli Eclipse-versiosi ei ole soveltuva, asenna uusi versio [https://www.eclipse.org/downloads/](https://www.eclipse.org/downloads/) -osoitteesta löytyvällä asennusohjelmalla.

Kurssin työkalut ovat erittäin yleisesti käytössä, joten hyviä ohjeita ja esimerkkejä löytyy melko varmasti netistä. Kannattaa myös kysyä ongelmatilanteissa apua Teamsissa.

## Git-versionhallinta

Kurssin tehtäväpohjien ja malliratkaisujen jakelussa hyödynnetään ohjelmistokehityksen alalla erittäin vakiintunutta Git-versionhallintaa ja GitHub-palvelua. Voit kloonata itsellesi kurssin projektin osoitteesta [https://github.com/haagahelia/swd4ta033-3003/](https://github.com/haagahelia/swd4ta033-3003/). Kurssin edetessä projektiin lisätään uusia tiedostoja, jotka voit päivittää itsellesi Git:in avulla.

Gitin käytön opetteluun voit käyttää esimerkiksi Helsingin yliopiston erinomaista "Tietokone Työvälineenä" -kurssin Git-materiaalia: [https://tkt-lapio.github.io/git/](https://tkt-lapio.github.io/git/). Vaikka Git tuntuisi aluksi vaikealta tai ahdistavalta, sinun ei tarvitse opetella kaikkea kerralla, vaan tee vain sen verran mistä on sinulle välitöntä hyötyä.

## Lähteiden käyttäminen

Tämän kurssin materiaali perustuu suurelta osin valmiisiin netistä löytyviin dokumentaatioihin ja tutoriaaleihein. Tällä sivulla eri aihealueiden yhteydessä tarjotaan linkkejä aihetta koskeviin materiaaleihin, mutta **joudut sen lisäksi merkittävissä määrin etsimään itse tietoa aiheista**.

Ohjelmointiongelmiin löytyy usein valmiita tai osittaisia ratkaisuja ympäri Internetiä niin keskustelupalstoilta kuin tutoriaaleista. Huonossa tapauksessa löydät toimivan ratkaisun ongelmaasi, mutta et osaa aivan tulkita mitä löytämäsi koodi tekee ja miksi se ratkaisee ongelmasi. Ammattimaisessa ohjelmistokehityksessä tästä seuraa mahdollisesti suuriakin vahinkoja.

Nettilähteiden hyödyntäminen ja niistä mallin ottaminen on sallittua ja kannustettavaa, mutta et saa vain kopioida ratkaisuja, vaan sinun tulee ymmärtää, miten koodisi toimii. Lisäksi, erityisesti koska kyseessä on korkeakoulun opintojakso, sinun tulee merkitä lähteet lainatessasi esimerkiksi StackOverflow:sta löytämääsi koodia. Lähdeviitteeksi riittää esimerkiksi verkkosivun osoite Java-kommenttina lainatun koodin yhteydessä, tai käyttämäsi lähteen käyttöehtojen mukainen muu lähdeviite.

## Esitietovaatimukset

> Opiskelija on suorittanut opintojakson Ohjelmointi 1 (SWD4TA014) tai hänellä on vastaavat tiedot ja taidot. Opiskelija suorittaa samanaikaisesti opintojakson Tietokannat ja tiedonhallinta (SWD1TA003) tai hänellä on vastaavat tiedot ja taidot.
>
> [*opintojaksokuvaus*](https://opinto-opas.haaga-helia.fi/fi/realization/SWD4TA033-3003) 

Mikäli et osaa Javan perusteita, nousee tämän kurssin suorittamisessa nopeasti seinä vastaan.

Mikäli SQL-osaamisessasi on puutteita, suosittelen perehtymään netistä vapaasti löytyviin lähteisiin sekä tutoriaaleihin, kuten [sqlzoo.net](https://sqlzoo.net/).

## Kurssin aikataulu

Kurssi päättyy perjantaina 20. maaliskuuta.

----

## Aihe 1: yksikkötestauksen perusteet ja koodin laatu (DL su 26.1. klo 23:55)

Tällä viikolla tutustumme yksikkötestaukseen ja testaamme valmista virheellisesti toimivaa ja heikosti toteutettua metodia. Tutustumme lisäksi koodin laatuun vaikuttaviin tekijöihin ja sovellamme niitä annetun valmiin koodin parantamiseksi.

### Koodin laatu

Tähän asti olet ohjelmointiopinnoissasi kenties keskittynyt lähinnä ohjelmasi toimivuuteen kiinnittämättä suurempaa huomiota sen ymmärrettävyyteen tai jatkokehitettävyyteen. Ammatillisessa ohjelmistokehityksessä on harvinaista, että koodia kirjoitettaisiin kerran ja vain yhden kehittäjän toimesta. Päinvastoin, koodia kirjoitetaan isoissa tiimeissä, joissa kehittäjät vaihtuvat ja olemassa oleviin ominaisuuksiin tehdään jatkuvasti muutoksia.

Tällöin on erittäin tärkeää, että koodi on muokattavissa ilman odottamattomia rikkoutumisia ja että muut kehittäjät ymmärtävät toistensa koodia ja pystyvät muokkaamaan sitä uusien vaatimusten mukaiseksi.

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

Vaikka ohjelmiston kaikki osat toimisivat itsenäisinä täydellisesti, voi järjestelmä silti olla kokonaisuutena viallinen. Siksi ohjelmistoprojekteissa testaus ei usein rajoitu pelkkään yksikkötestaamiseen, vaan menetelminä käytetään mm. integraatiotestejä ja järjestelmätestejä. Katso esimerkiksi Googlen kuvahaku humoristisista tilanteista, joissa yksittäiset asiat toimivat, mutta lopputulos ei silti täytä odotuksia: "[two unit tests, no integration tests](https://www.google.com/search?q=two%20unit%20tests,%20no%20integration%20tests&amp;tbm=isch)".


----

## Aihe 2: tietokantaohjelmointi (JDBC) (DL su 2.2. klo 23:55)

Tämän aiheen sisältö julkaistaan seuraavaksi.

## Aihe 3: Tietokannan eriyttäminen (DAO) + yksikkötestaaminen (JUnit) (DL su 9.2. klo 23:55)

Tämän aiheen sisältö julkaistaan kurssin aikana.

## Aihe 4: Verkkosovellus (Servlet) (DL su 16.2. klo 23:55)

Tämän aiheen sisältö julkaistaan kurssin aikana.

## Aihe 5: Verkkosovelluksen kolmikerrosarkkitehtuuri (JSP, JSTL) (DL su 23.2. klo 23:55)

Tämän aiheen sisältö julkaistaan kurssin aikana.

## Aihe 6: Ajax ja datan lisääminen sivulle dynaamisesti (DL su 1.3. klo 23:55)

Tämän aiheen sisältö julkaistaan kurssin aikana.

## Aihe 7: Harjoitustyö (DL su 22.3. klo 23:55)

Tämän aiheen sisältö julkaistaan kurssin aikana.