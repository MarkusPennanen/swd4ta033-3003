# Ohjelmointi 2, SWD4TA033-3003 (Java, 5 op)

Tervetuloa kurssille!

Tällä opintojaksolla sovellamme aiemmin oppimianne ohjelmointitaitoja tietokantojen ohjelmallisessa käyttämisessä ja verkkopalveluiden toteuttamisessa. Syvennymme kielen syntaksin ja tarvittavien kirjastojen lisäksi myös ymmärrettävän koodin kirjoittamiseen, yksikkötestaukseen sekä versionhallinnan alkeisiin.

Opettajana kurssilla toimii Teemu Havulinna (`etunimi.sukunimi@haaga-helia.fi`).

## Kurssin aikataulu ja aiheet:

### [Aihe 1: Yksikkötestauksen perusteet ja koodin laatu](01_yksikkotestaus.md) (DL su 26.1. klo 23:55)

### [Aihe 2: tietokantaohjelmointi (JDBC)](02_tietokantaohjelmointi.md) (DL su 2.2. klo 23:55)

### (Tulossa) Aihe 3: Tietokannan eriyttäminen (DAO) + yksikkötestaaminen (JUnit) (DL su 9.2. klo 23:55)

### (Tulossa) Aihe 4: Verkkosovellus (Servlet) (DL su 16.2. klo 23:55)

### (Tulossa) Aihe 5: Verkkosovelluksen kolmikerrosarkkitehtuuri (JSP, JSTL) (DL su 23.2. klo 23:55)

### (Tulossa) Aihe 6: Ajax ja datan lisääminen sivulle dynaamisesti (DL su 1.3. klo 23:55)

### (Tulossa) Aihe 7: Harjoitustyö (DL su 22.3. klo 23:55)



## Viestintäkanavat

Tällä kurssilla käytetään viestintään pääasiassa Microsoftin Teams -palvelua. Teams on osoittautunut oivalliseksi tueksi itseopiskelussa ja se tarjoaa luontevamman kanavan kysyä ja keskustella kuin esimerkiksi Moodle. Jos jäät jumiin koodisi kanssa tai et ymmärrä materiaaleja tai tehtävänantoja, kysy rohkeasti vinkkejä Teamsissa. Todennäköisesti samaa ongelmaa pohtii kanssasi myös moni muu, joten lähetäthän sisältöä ja tehtävänantoja koskevat kysymykset yhteiselle kanavalle (eikä yksityisviestinä opettajalle).

Teamsissa voi myös esittää toivomuksia kurssin kehittämiseksi jo kurssin aikana niin yksityisviesteinä opettajalle kuin yhteisillä kanavilla. Tämä kurssi ei ole suinkaan valmis, vaan sitä kehitetään kurssin etenemisen mukaan. Tarpeen mukaan voimme järjestää esimerkiksi chat- tai videochat-aikoja etukäteen sovittavina ajankohtina.

Teams on saatavilla puhelimien sovelluskaupoista sekä työpöytäsovelluksena, tai voit käyttää sitä selaimen web-käyttöliittymässä ilman asennuksia. Kirjautuminen Teamsiin tapahtuu Haaga-Helian opiskelijatunnuksella.

* [Teams Quick Start -ohje (pdf)](https://download.microsoft.com/download/D/9/F/D9FE8B9E-22F5-47BF-A1AB-09539C41FCD0/Teams%20QS.pdf)
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
