## Aihe 2: tietokantaohjelmointi (JDBC) (DL su 2.2. klo 23:55)

Tällä viikolla opettelemme yhdistämään tietokantaan Java-ohjelmasta ja tekemään yksinkertaisia CRUD-toimenpiteitä (Create, Read, Update & Delete).

## JDBC – Java Database Connectivity

Javan standardikirjastoon määritelty JDBC (Java Database Connectivity) -ohjelmointirajapinta mahdollistaa Java-sovellusten yhdistämisen tietokantoihin ja erilaisten kyselyiden ja päivitysten tekemisen. JDBC ei rajoita lainkaan sitä, minkä SQL-pohjaisten tietokantojen kanssa sitä voidaan käyttää, vaan eri tietokantoja voidaan hyödyntää käyttämällä niille toteutettuja valmiita ajureita.

### SQLite
> SQLite is a relational database management system (RDBMS) contained in a C library. In contrast to many other database management systems, SQLite is not a client–server database engine. Rather, it is embedded into the end program.
> 
> SQLite is a popular choice as embedded database software for local/client storage in application software such as web browsers. It is arguably the most widely deployed database engine, as it is used today by several widespread browsers, operating systems, and embedded systems (such as mobile phones), among others. SQLite has bindings to many programming languages.
> https://en.wikipedia.org/wiki/SQLite

Tällä kurssilla käytettävä SQLite-tietokanta on paikallinen muisti- tai tiedostopohjainen tietokanta. Emme siis tarvitse erillistä palvelinta eikä meidän tarvitse huolehtia verkkoyhteyksistä tai salasanoista, vaan voimme keskittyä varsinaiseen ohjelmointiin. 

Samat Java-koodit toimisivat toki myös esim. MySQL tai MariaDB –tietokantoja hyödyntäen - käyttäisimme tällöin vain eri ajuria.


### JDBC:n SQLite-ajuri

Tietokannan käyttämiseksi Javasta käsin tarvitsemme erillisen JDBC-ajurin. Erilliset Java-Kirjastot jaellaan tyypillisesti `.jar`-tiedostoina (Java Archive), kuten tämä ajuri, ja ne asennetaan pääsääntöisesti automaatiotyökalujen avulla. Suosittuja automaatiotyökaluja Javalle ovat mm. Maven ja Gradle. Automaatiotyökalujen avulla monimutkaistenkin riippuvuuksien hallinta on kohtuullisen yksinkertaista.

Vielä tässä vaiheessa kurssia emme perehdy Maveniin, vaan haemme tarvittavan ajurin manuaalisesti Mavenin tietovarastosta: https://mvnrepository.com/artifact/org.xerial/sqlite-jdbc. Siirry sieltä uusimpaan versioon (kirjoitushetkellä 3.30.1) ja tallenna ajuri itsellesi "Jar (X.Y MB)". Kirjoitushetkellä viimeisimmän .jar-paketin lataus tapahtuu suoraan [tästä](https://repo1.maven.org/maven2/org/xerial/sqlite-jdbc/3.30.1/sqlite-jdbc-3.30.1.jar).

Ajurin käyttöönotto projektissasi edellyttää sen lisäämistä projektin "build path":iin, eli listalle hakemistoista joissa ohjelmasi käyttämät Java-luokat sijaitsevat. Helpoiten tämä onnistuu luomalla projektiisi uuden `lib`-hakemiston, laittamalla `.jar`-tiedoston hakemistoon ja lopuksi lisäämällä hakemiston "build path":iin esimerkiksi [tämän Stack Overflow -vastauksen mukaisesti](https://stackoverflow.com/a/23420543).

### Extra: SQLite-tietokannan käyttäminen Javan ulkopuolelta

Tietokannan käyttäminen Java-ohjelmasi ulkopuolella ei ole tällä kurssilla välttämätöntä, mutta kyselyitä on helpompi suunnitella ja kokeilla ennen niiden koodaamista osaksi ohjelmaa. Tietokannan luonti ja rakenteen muuttaminen ovat myös luonnollista tehdä erillisellä työkalulla.

Erilaisten graafisten käyttöliittymien lisäksi SQLite:lle on saatavissa SQLite:n oma komentorivityökalu.

Voit ladata itsellesi `sqlite3.exe`-komentorivityökalun osoitteesta: https://sqlite.org/download.html -> sqlite-tools-win32-x86-VERSIO.zip. Ohjelma voidaan suorittaa ilman erillisiä asennuksia. Tallenna `sqlite3.exe`-tiedosto esim. samaan kansioon tietokantasi kanssa käynnistä se valitsemaltasi komentoriviltä, kuten cmd tai PowerShell.

Tiedostossa [02b_sqlite_tools.md](02b_sqlite_tools.md) on esimerkki tämän työkalun käyttämisestä laajemman musiikkitietokannan tutkimisessa. Lisää ohjeita komentorivityökalun käyttöön löydät osoitteesta: https://sqlite.org/cli.html tai videosta https://video.haaga-helia.fi/media/SQLite+tools/0_pez4r54j


## Lukutehtävät

*Lukutehtävät kannattaa tehdä rinnakkain tämän viikon koodiharjoituksen tekemisen kanssa, jotta voit kokeilla lukemaasi heti käytännössä.*

Jenkov.com -palvelussa on laaja tutoriaali JDBC-teknologioista ja se käsittelee kattavasti tietokantojen Javasta käyttämiseksi tarvittavat toimenpiteet. Tutoriaali itsessään käyttää H2-tietokantaa, mutta ei tietokanta-ajurin luokan nimeä ja yhteysosoitetta lukuun ottamatta poikkea SQLite:n käytöstä. 

**Lue tutoriaalista seuraavat osat:**

1. http://tutorials.jenkov.com/jdbc/index.html
1. http://tutorials.jenkov.com/jdbc/overview.html
1. http://tutorials.jenkov.com/jdbc/driver-types.html <br />
    (valinnainen, syventävää tietoa ajureista)
1. http://tutorials.jenkov.com/jdbc/connection.html <br /> 
    (voit ohittaa transaktioita koskevat kappaleet)
1. http://tutorials.jenkov.com/jdbc/query.html
1. http://tutorials.jenkov.com/jdbc/update.html
1. http://tutorials.jenkov.com/jdbc/statement.html
1. http://tutorials.jenkov.com/jdbc/resultset.html <br />
    (voit ohittaa kappaleet "Updating a ResultSet", "Inserting Rows into a ResultSet" ja "ResultSet Holdability")
1. http://tutorials.jenkov.com/jdbc/preparedstatement.html

Edellä ohjeistetun Jenkov.com:in tutoriaalin lisäksi myös Oraclella on [kattava oppimateriaali](https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html) JDBC:n opetteluun. Hyviä ohjeita löytyy myös YouTubesta sekä Googlettamalla tarkemmin yksittäisiä JDBC-aiheita.

### Yhteyden muodostaminen SQLite-tietokantaan

Muodostaessasi yhteyden tietokantaan `DriverManager.getConnection(url)`-metodin avulla, tulee sinun antaa parametrina merkkijono, joka on tietokanta-ajurikohtainen "connection url". Yhteysosoitteet alkavat aina tekstillä `jdbc:` ja ajurin nimellä. Ajurin nimen jälkeen kirjoitetaan kaksoispiste, ja sen jälkeen esimerkiksi tietokannan sijainti levyllä (SQLite) tai verkossa (MySQL).

SQLite-tietokannalle yhteysosoite on muotoa `jdbc:sqlite:C:\polku\tietokanta.sqlite` tai `jdbc:sqlite:/users/me/database.sqlite` riippuen käyttöjärjestelmästäsi. Kun kirjoitat SQLite-osoitteen Java-merkkijonoksi, huomaa, että kenoviivat (`\`) ovat Javan merkkijonoissa varattu erikoismerkeille, ja tavallisen kenoviivan tuottamiseksi merkkijonoon kirjoitetaan (`\\`). 

Java-koodissasi yhteys tietokantaan `C:\databases\my_cool_database.sqlite` määritellään siis näin:

```java
String url = "jdbc:sqlite:C:\\databases\\my_cool_database.sqlite";
```

MySQL-tietokantaan yhdistettäisiin vastaavasti esim. osoitteella `"jdbc:mysql://127.0.0.1:3306/my_cool_database"` ja käyttämällä projektissa MySQL-ajuria.


## Tehtävä (DL su 2.2. klo 23:55)

### Ostoslista ja CRUD-operaatiot

Tällä viikolla sinun tulee toteuttaa mahdollisimman yksinkertainen Java-ohjelma, joka toimii käyttöliittymänä ostoslistan tuotteet sisältävälle tietokannalle. Tietokannassa on vain yksi taulu eikä sinun tarvitse huolehtia esimerkiksi siitä, voisiko ohjelmassa olla samanaikaisesti useita eri käyttäjien ostoslistoja. Käyttöliittymän kautta tulee voida tehdä CRUD-operaatiot (Create, Read, Update & Delete) tietojen päivittämistä lukuun ottamatta.

Ostoslistan sisällöksi riittää kutakin tuoteriviä kohden uniikki id sekä ostettava tuote tekstinä. Voit hyödyntää tässä tehtävässä valmista [SQLite-tietokantatiedostoa](sql/shoppingList.sqlite) johon on ajettu seuraava luontikäsky ja muutama esimerkkirivi:

```sql
CREATE TABLE ShoppingListItem (
   id INTEGER PRIMARY KEY,
   title TEXT NOT NULL
);

```

Huomaa, että SQL-kyselyjen muodostaminen merkkijonoja yhdistelemällä aiheuttaa mm. tietoturvaongelmia, kuten alla oleva esimerkki havainnollistaa:

[![Exploits of a Mom](https://imgs.xkcd.com/comics/exploits_of_a_mom.png)](https://xkcd.com/327/)

Muista siis käyttää edellä linkitetyissä tutoriaaleissa esiteltyä `PreparedStatement`-luokkaa aina muodostaessasi kyselyitä, joihin syötetään dynaamisesti parametreja!



