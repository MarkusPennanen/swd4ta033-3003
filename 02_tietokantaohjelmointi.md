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

### Ostoslista-tietokanta sekä CRUD-operaatiot

Tällä viikolla sinun tulee toteuttaa mahdollisimman yksinkertainen Java-ohjelma, joka toimii käyttöliittymänä ostoslistan tuotteet sisältävälle tietokannalle. Tietokannassa on vain yksi taulu eikä sinun tarvitse huolehtia esimerkiksi siitä, voisiko ohjelmassa olla samanaikaisesti useita eri käyttäjien ostoslistoja.



Hyvä dokumentti: [http://tutorials.jenkov.com/jdbc/index.html](http://tutorials.jenkov.com/jdbc/index.html)

Dokumentin etusivu: [https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html](https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html)

[https://docs.oracle.com/javase/tutorial/jdbc/basics/connecting.html](https://docs.oracle.com/javase/tutorial/jdbc/basics/connecting.html)

[https://docs.oracle.com/javase/tutorial/jdbc/basics/processingsqlstatements.html](https://docs.oracle.com/javase/tutorial/jdbc/basics/processingsqlstatements.html)

[https://docs.oracle.com/javase/tutorial/jdbc/basics/prepared.html](https://docs.oracle.com/javase/tutorial/jdbc/basics/prepared.html)

Dynamic Web Project:in luominen: [https://video.haaga-helia.fi/media/Eclipse+++Dynamic+Web+Project/0\_9q4oyjib](https://video.haaga-helia.fi/media/Eclipse+++Dynamic+Web+Project/0_9q4oyjib)

Luo tietokanta ja CRUD-operaatiot ShoppingListItem-taululle.

**SQLiten käyttäminen ja web-projektin luonti**

[**SQLite tools**](https://video.haaga-helia.fi/media/SQLite+tools/0_pez4r54j) 8:18
Chinook-tietokannan testikäyttöä SQLite:n komentorivikäyttöliittymässä.

[**Eclipse / Dynamic Web Project**](https://video.haaga-helia.fi/media/Eclipse+++Dynamic+Web+Project/0_9q4oyjib) 2:12
Tässä videossa luodaan Eclipseen uusi Dynamic Web Project tulevan harjoitustyön pohjaksi.


## Chinook-tietokanta

Käytämme harjoitustyössä Chinook-tietokantaa. Sama tietokanta on saatavilla yleisimmille  tietokantapalvelimille (SQLite, MySQL…)

Tietokanta sisältää tietoja mm. musiikkikappaleista, levyistä ja artisteista. Tietokanta on lisensoitu siten, että sen käyttäminen, muuttaminen ja levittäminen on sallittua.

Tallenna itsellesi kopio tietokannasta osoitteesta: https://github.com/lerocha/chinook-database/ ChinookDatabase -> DataSources -> Chinook_SQLite.sqlite

Voit tallentaa tiedoston esimerkiksi C-asemalle uuteen hakemistoon C:\sqlite\ tai soveltaen Linux/Mac -järjestelmääsi.




## Tietokantaan yhdistäminen

```java
import java.sql.Connection;
import java.sql.DriverManager;

public class ChinookDatabase {
    // JDBC-polku pitää sisällään käytettävän ajurin nimen ja tietokannan sijainnin
    private static final String URL = "jdbc:sqlite:M:\\sqlite\\Chinook_Sqlite.sqlite";

    public Connection connect() throws SQLException, ClassNotFoundException {
        // Tietokanta-ajurin luokan lataus
        Class.forName("org.sqlite.JDBC");

        // Yhteyden muodostaminen tietokantaan
        return DriverManager.getConnection(URL);
    }
}

``` 
`ChinookDatabase.java`

MySQL-tietokantaan yhdistettäisiin vastaavasti esim. osoitteella `"jdbc:mysql://127.0.0.1:3306/chinook"` sekä käyttämällä edellä MySQL-ajuria.

## Yhteyksien ja resurssien sulkeminen

TODO: esimerkkikoodi, linkki varsinaiseen ChinookDatabase-luokkaan
```java
db.close(results, statement, connection);
```

### Tarkistetun poikkeuksen kääriminen

Edellisessä koodiesimerkissä toteuttamamme `connect`-metodi on määritelty heittämään kaksi erilaista tarkistettua poikkeusta: `throws SQLException, ClassNotFoundException`. Tämän esimerkkiprojektin puitteissa olemme valinneet [kääriä nämä poikkeukset ajonaikaisiksi poikkeuksiksi](https://www.google.com/search?q=wrap+checked+exception+in+runtimeexception), jotta esimerkiksi tietokanta-ajurin puuttumisesta aiheutuvaa `ClassNotFoundException`-poikkeusta ei tarvitse erikseen käsitellä muissa tietokantaluokissa.

```java
try {
    Class.forName("org.sqlite.JDBC");
    return DriverManager.getConnection(URL);

} catch (SQLException | ClassNotFoundException e) {
    throw new RuntimeException(e);
}
```
Nyt metodi heittää siis virhetilanteessa `RuntimeException`-tyyppisen poikkeuksen.

### Extra: Tietokannan osoitteen siirtäminen ympäristömuuttujaan

Tietokannan osoitteen "kovakoodaaminen" Java-luokkaan on usein huono idea. Selkein syy tähän on se, että sovellusta kehitettäessä on tyypillisesti tarve erilaisille ympäristöille, kuten kehitysympäristö, testausympäristö ja tuotantoympäristö. Jokaisessa näistä ympäristöistä käytetään eri tietokantaa, joten sovelluksesta tulisi muokata aina jokaista ympäristöä varten.

Parempi tapa on asettaa ympäristökohtaisesti vaihtuvat arvot ympäristömuuttujiin, jolloin sovellus käyttää ajoympäristöstään riippuen kehitys-, testi- tai tuotantokantaa. Ympäristömuuttujien arvoja voidaan Javassa lukea `System.getenv`-metodilla:

```java
import java.sql.Connection;
import java.sql.DriverManager;

public class ChinookDatabase {
    // Luetaan tietokannan osoite ympäristömuuttujasta:
    private static final String URL = System.getenv("JDBC_DATABASE_URL");

    public Connection connect() {
        try {
            Class.forName("org.sqlite.JDBC");
            return DriverManager.getConnection(URL);

        } catch (SQLException | ClassNotFoundException e) {
            throw new RuntimeException(e);
        }
    }
}

``` 
TODO: Linkki lähdekoodiin

Lue lisää osoitteesta: https://devcenter.heroku.com/articles/connecting-to-relational-databases-on-heroku-with-java#using-the-database_url-in-plain-jdbc

## JDBC-luokat

![JDBC-kyselyssä tarvittavat luokat](assets/tietokannat/jdbc_classes.png)

## Kyselyn tulosten läpikäynti: ResultSet, next ja get

* JDBC-kyselyiden tuloksina saadaan ResultSet-olioita

* ResultSet-olion kautta on mahdollista käsitellä **vain yhtä tulosriviä kerrallaan**

* Käsiteltävä tulosrivi voidaan vaihtaa seuraavaksi kutsumalla next-metodia:
  * next palauttaa true, jos käsiteltävää dataa on jäljellä
  * next palauttaa false, jos dataa ei ole enempää

* Nykyiseltä tulosriviltä voidaan kysyä eri sarakkeiden arvot get-metodeilla, esim:
  * `getString("Name")`
  * `getLong("ArtistId")`

```java
// Avataan yhteys
Connection connection = DriverManager.getConnection(URL);

// Muodostetaan kysely
PreparedStatement statement = connection.prepareStatement("SELECT * FROM Album LIMIT 5");

// Suoritetaan kysely
ResultSet results = statement.executeQuery();

// Käydään tulokset läpi
while (results.next()) { 
    // Tulostetaan albumien nimet
    System.out.println(results.getString("Title")); 
}

// Suljetaan kaikki resurssit
results.close(); 
statement.close(); 
connection.close();
```

1. Alussa `ResultSet` ei kohdistu millekään riville. `next()`-metodia on kutsuttava ennen tietojen lukemista.
1. `next()`-metodin kutsuminen ensimmäistä kertaa asettaa ResultSetin käsittelemään ensimmäistä riviä tuloksista (`AlbumId = 1`) ja palauttaa arvoksi `true`.
1. Seuraavat `next`-metodin kutsut siirtävät `ResultSet`in käsittelemään aina seuraavaa tulosriviä, kunnes rivit loppuvat ja `next()` palauttaa arvon `false`.

```
AlbumId | Title                                  | ArtistId
--------|----------------------------------------|-----
1       | For Those About To Rock We Salute You  |1
2       | Balls to the Wall                      |2
3       | Restless and Wild                      |2
4       | Let There Be Rock                      |1
5       | Big Ones                               |3
```

### Eri tietotyyppien lukeminen tietokannasta saadulta riviltä

Tietokannasta saatu data käydään läpi ResultSet-olion kautta rivi kerrallaan ja sarake kerrallaan. Esimerkiksi Chinook-tietokannan `Track`-taulun eri sarakkeiden arvot voidaan lukea seuraavasti:

```java
ResultSet results = statement.executeQuery();

while (results.next()) {
    long id = results.getLong("TrackId");
    String name = results.getString("Name");
    String mediaType = results.getString("MediaTypeName");
    String genre = results.getString("GenreName");
    long albumId = results.getLong("AlbumId");
    long milliseconds = results.getLong("Milliseconds");
    double unitPrice = results.getDouble("UnitPrice");

    tracks.add(new Track(id, name, albumId, mediaType, genre, milliseconds, unitPrice));
}
```
TODO: Linkki lähdekoodiin

## Kyselyiden tekeminen turvallisesti (`PreparedStatement`)

Yksi tunnetuimmista ohjelmistojen haavoittuvuustyypeistä on ns. SQL injektio, joka syntyy silloin, kun kyselyyn syötetään dataa,joka tulkitaan virheellisesti osaksi itse kyselyä tai uudeksi kyselyksi. 

> SQL injection is an attack in which malicious code is inserted into strings that are later passed to an instance of SQL Server for parsing and execution. - [*Microsoft Docs, SQL Injection*](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms161953(v=sql.105))

Älä siis koskaan muodosta SQL-kyselyitä käsin yhdistelemällä merkkijonoja:

```java
// Ei koskaan näin:
connection.prepareStatement("SELECT * FROM Artist WHERE Name = \"" + name + "\"");
```

Kyselyn teko merkkijonoja yhdistelemällä aiheuttaa mm. tietoturvaongelmia, kuten alla oleva esimerkki havainnollistaa:

[![Exploits of a Mom](https://imgs.xkcd.com/comics/exploits_of_a_mom.png)](https://xkcd.com/327/)

### Parametrisoidut kyselyt

Kyselyn "käsin rakentamisen" sijaan kyselyssä tarvittavat muuttuvat arvot asetataan kyselyyn parametreina, jotka tietokanta-ajuri asettaa kyselyyn tarvittavien muunnosten jälkeen. 

* Kun kyselyissä tarvitaan ajonaikaisesti muodostettavia parametreja (id:t, nimet…), ne tulee asettaa paikalleen `PreparedStatement`-luokan metodeilla
* `PreparedStatement`-luokan SQL-kyselyihin parametrien tilalle kirjoitetaan kysymysmerkit (`?`), joiden kohdille asetetaan set-metodeilla arvot:

```java
PreparedStatement statement = 
connection.prepareStatement("SELECT * FROM Artist WHERE Name = ?");

statement.setString(1, name);
```

* `setString` asettaa kyselyyn merkkijonon, `setLong` vastaavasti kokonaisluvun.
* set-metodien ensimmäisenä parametrina annetaan aina indeksi, joka kertoo mikä kyselyn parametreista asetetaan 
* **parametrien indeksit alkavat 1:stä, ei nollasta! 😱**

TODO: Linkki ja koodiesimerkki esimerkkiprojektista


# Tehtävä

Kirjoita luokka `PrintTitlesByArtist`, jonka main-metodissa: 
1. kysyt artistin nimeä käyttäjältä
2. listaat kaikki kyseisen artistin albumit

```
Write the name of an artist: Metallica

Found albums:
Garage Inc. (Disc 1)
Black Album
Garage Inc. (Disc 2)
Kill 'Em All
Load...
```

TODO: Poista mallivastaus ja lisää jonnekin ohje SQLExceptionin käsittelystä

```java
public class PrintTitlesByArtist {

    public static void main(String[] args) throws SQLException {
        String sql = "SELECT * FROM Album WHERE ArtistId = (SELECT ArtistId FROM Artist WHERE Name = ?)";

        Scanner scanner = new Scanner(System.in);
        ChinookDatabase db = new ChinookDatabase();

        Connection conn = db.connect();
        PreparedStatement statement = conn.prepareStatement(sql);

        System.out.print("Write the name of an artist: ");
        String artistName = scanner.nextLine();

        statement.setString(1, artistName);
        ResultSet results = statement.executeQuery();

        System.out.println("Found albums:");
        while (results.next()) {
            System.out.println(results.getString("Title"));
        }

        db.close(results, statement, conn);
        scanner.close();
    }
}
```


# Tietokantalogiikan eriyttäminen muusta koodista

TODO: MVC-mallin intro?

## DAO-luokat (Data Access Object)

Edellisissä esimerkeissä esiintyy hyvin paljon tietokannan käyttöön liittyviä yksityiskohtia: yhteyksien luomista ja sulkemista, SQL-kyselyitä, tulosten läpikäyntiä.

Sovelluksen kehittämisen, testauksen ja ylläpidon kannalta on haastavaa, mikäli tietokantaa käytetään lukuisissa eri paikoissa.

Tietokantaa käytetäänkin usein Data Access Object -luokkien (DAO) kautta. DAO-luokat huolehtivat yhteyksien käytöstä ja kyselyiden muodostamisesta. DAO-luokkien metodit palauttavat aivan tavallisia Java-olioita joko yksinään tai kokoelmina.

## Model-luokat

TODO: model-luokkien intro

> Tietokantataulut ja luokat ovat hyvin samankaltaisia. Tietokantatauluissa määritellään sarakkeet ja viiteavaimet, luokissa määritellään attribuutit ja viitteet. Ei liene yllättävää, että tietokantatauluja kuvataan usein luokkien avulla.
> * https://web-palvelinohjelmointi-s19.mooc.fi/osa-2/3-tietokantojen-kasittely

`Artist`-tietokantataulua voidaan varsin suoraviivaisesti mallintaa esimerkiksi seuraavan `Artist`-luokan avulla:

```java
public class Artist {

    private long id;
    private String name;

    public Artist(long id, String name) {
        this.id = id;
        this.name = name;
    }

    // getterit ja setterit...
}
```

Huomaa, että tietokannassa pääavain on sarakkeessa `ArtistId` kun Java-luokassa vastaavan oliomuuttujan nimi on `id`. Voimme itse vapaasti valita joko samat tai toisistaan poikkeavat muuttujanimet.

## Dao-luokat

TODO: Dao-luokkien intro, motivaatio

```java
public class ArtistDao {

    public List<Artist> getAllArtists() {
        ChinookDatabase db = new ChinookDatabase();

        Connection connection = db.connect();
        PreparedStatement statement = null;
        ResultSet results = null;

        List<Artist> list = new ArrayList<>();
        try {
            statement = connection.prepareStatement("SELECT * FROM Artist ORDER BY Name ASC");
            results = statement.executeQuery();

            while (results.next()) {
                long id = results.getLong("ArtistId");
                String name = results.getString("Name");
                list.add(new Artist(id, name));
            }
        } catch (SQLException e) {
            throw new RuntimeException(e);
        } finally {
            db.close(results, statement, connection);
        }
        return list;
    }
}
```

Chinook-tietokantaa hyödyntävässä verkkosovelluksessa voisi olla esimerkiksi seuraavat Model-luokat sekä niitä vastaavat DAO-luokat seuraavine metodeineen:

**Artist + ArtistDAO**
* `Artist findArtist(long id)`
* `List<Artist> findAllArtists()`
* `List<Artist> findArtistsByName(String name)`

**Album + AlbumDAO**
* `Album findAlbum(long id)`
* `List<Album> findAlbumsByArtist(Artist artist)`
* `List<Album> findAlbumsByTitle(String title)`

**Track + TrackDAO**
* `List<Track> findTracksByAlbum(Album album)`



## Lisenssi

Tämä oppimateriaali on lisensoitu [Creative Commons BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/) -lisenssillä.
