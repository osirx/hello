# Házi feladat:

## 1. Markdown text-file formázás tutorial (remélem tetszeni fog)

2017.11.24-25

https://www.markdowntutorial.com/

Ezzel gyakorlod kicsit az angolt és az md (markdown) formázással is megismerkedsz.

Vagy ezt is olvashatod, ez kompaktabb:
http://agea.github.io/tutorial.md/

# A dolgozathoz vázlat

## I. Bevezetés: a probléma leírása (bejelentõ :))

Napjaink szoftver-rendszereire jellemzõ a gyors fejlesztés, a nagy méret és komplexitás. Azt ellenõrizni, 
hogy az elkészült termék megfelel az ügyfél igényeinek és hibamentesen mûködik, teszteléssel tudjuk. A 
változásokat tesztelni manuálisan rövid idõ alatt nem lehetséges vagy nagyon költséges (sok emberóra 
ráfordítást igényel), ezért a gyors, minõségi szoftverfejlesztés nem megoldható automatizált tesztelés nélkül.

A dolgozat célja, hogy a tesztelési módszereket röviden összefoglalja, a napjainkban használt legelterjedtebb 
módszereket részletesen bemutassa azok elõnyeivel és hátrányaival együtt, kitérjen az alkalmazhatóságuk 
követelményeire, illetve hogy az adott módszer a szoftver mely tulajdonságát teszteli, méri. A dolgozatban 
áttekintjük a rendelkezésre álló eszközöket és könyvtárakat, amelyek segítségével az ismertetett módszereket 
alkalmazni lehet.


## II. Rövid leírás a tesztelésrõl: 

Emberi tévedés, hiba, információhiány, bonyolult, összetett feladat->hiba a programban/dokumentációban ->hibás mûködést okozhat.
Hibásan mûködõ szoftver->bosszúság, anyagi kár, üzleti jóhírnév elvesztése, sérülés...

A tesztelés célja:
- hibák feltárása/megelõzése,  elõfordulásának csökkentése: ezzel csökkentve a mûködési hiba valószínûségét
- a szoftver megfelel-e a meghatározott követelményeknek? (funkcionális, nem funkcionális elvárások)
- szoftver minõségének biztosítása, javítása (hatékonyság, megbízhatóság, használhatóság, karbantarthatóság...)

Hiba a szoftverfejlesztés bármelyik szakaszában elõfordulhat; minél késõbb derül-ki egy hiba, annál költségesebb 
lehet a javítása, ezért cél, hogy a fejlesztési életciklus lehetõ legkorábbi szakaszában a lehetõ legtöbb 
hibát feltárjuk.->  A tesztelésnek végig kell kísérnie a teljes fejlesztési folyamatot. 

Sikeres tesztelés nem bizonyítja, hogy a termék hibátlan, de csökkenti a hibák elõfordulásának valószínûségét.  
Nem  jelenti automatikusan, hogy a rendszer helyes: pl. ha nem a megrendelõ elvárásait valósítja meg.

```
Ez  így tök jó eddig. :)
```

### A) Teszttípusok: (Különféle típusok aszerint, hogy  milyen tulajdonságokat tesztel)

- Funkcionális teszt: a szoftver funkcionálisan helyes-e, azt csinálja-e, amit elvárunk tõle. Fekete doboz. 
```
Nem mindig fekete doboz. A fekete boboz teszteles az csak annyit tesz, hogy nem ismerjük a kódot, amit tesztelünk. :)
A funkcionális teszt a program algoritmikus helyességét teszteli, azt, hogy megoldja-e a kitűzütt feladatot/problémát.
```

(Nem funkcionális teszt: a szoftver valamit hogyan csinál, mennyire felel meg adott feltétlenek, számszerûsíthetõ jellemzõk.)

- futási idõ ellenõrzés: milyen gyorsan mûködik, teljesíti-e a specifikációban meghatározott elvárást. Minõség szempontjából számít, hogy milyen gyorsan végzi el az egyes mûveleteket.
- specifikáció része lehet, hogy a szoftver mennyi felhasználót szolgáljon ki. Ennek ellenõrzése is része a tesztelésnek.
- longevity test: vizsgálja, hogyan mûködik hosszú távon a rendszer. Elvárás, hogy pl. egy adatbázis növekedése mellett is megfelelõen mûködjön. (specifikáció szerint)	
- terheléses teszt (load test): a rendszer "teherbíró képességét" vizsgálja, mekkora terhelés az (az elvárt terhelés fölött), amit már nem tud kezelni, összeomlik.
...

### B) Teszt szintek: (Mit tesztelünk, mi a tesztelés tárgya)
- egységteszt: a szoftver önálló egységeinek mûködését vizsgálja. Önmagában teszteli a rendszer komponenseit.
- integrációs teszt: a rendszer a kapcsolódó egységek együttmûködését vizsgálja, helyesen mûködnek-e együtt a komponensek.
(- Rendszerteszt
- Elfogadási teszt)

### Tesztelés menete
Tesztvégrehajtás történhet manuálisan és automatizáltan.
Manuális: ember hajtja végre a tesztlépéseket-> az emberi képességek (rugalmasság, intuíció) kihasználhatók. Nagy mennyiségû, 
vagy túl összetett teszt végrehajtására nem alkalmas. Pl. ilyenkor alkalmazható az automatizált tesztelés (emberi beavatkozás 
nélkül, elõny, hátrány...)... Egymást kiegészítõ technikák. ->Java könyvtárak

Absztrakt leírás arról, hogy mit, milyen eredményt várunk el. Konkrét tesztesetekre ellenõrizzük, hogy 
ez teljesül-e. Kellõen nagy és jó mintavétel esetén jól mûködhet a teszt.


## III. Konkrét eszközök: Vizsgált eszközök bemutatása. Mit lehet használni, szoftverek bemutatása. A barátom. :)

```
Természetesen van olyan, amit nagyon nehéz automatizálni, pl esztétikus-e egy GUI, mennyire kényelmes használni, stb, de a 
legtöbb tesztelési feladat jól automatizálható.

Ajánlott olvasmány:
- testNG - ez test framework, azaz egy eszköz, amiben a teszteket meg tudjuk írni, futtatni, etc
- létezik egy csomó másik fajta teszt eszköz is, de azok vagy sokkal szűkebb, specifikus területet fednek le (pl csak funkcionális tesztelés), 
vagy nem annyira elterjedtek, vagy valami miatt nem olyan kényelmes a használatuk 
(Pl:
gherkin - cucumber -- functional acceptance testing
selenium - web-es alkalmazások tesztelése az alkalmazás grafikus felületén keresztül, stbstb)
```
## TestNG

* tesztelési keretrendszer
* célja, hogy egyszerűsítse a tesztelési feladatokat
* alkalmazható unit teszt, integrációs teszt esetén

Az annotációk a tesztfuttató számára adnak információt, amelyekkel a teszt futása szabályozható: mi fut és hogyan.

* **@Test**: ez jelöli, hogy mit futtasson a tesztfuttató rendszer, innen tudja, hogy ez része a tesztnek.
* **@BeforeClass**: egyszer fut le az összes teszt előtt, mielőtt az adott osztály első tesztmetódusa futna. (pl. konstansok beállítására)
* **@AfterClass**: egyszer fut le, miután az osztály összes tesztje lefutott.
* **@BeforeMethod**: minden egyes teszt előtt lefut
* **@AfterMethod**: minden egyes teszt után lefut

Az annotációkhoz attribútumok adhatóak meg, amelyekkel finomhangolhatjuk a teszt futtatását.

@Test annotáció attribútumai pl.:

* **alwaysRun**: igaz érték esetén a teszt metódus mindig lefut, függetlenül attól, hogy az a metódus, amitől függ, hibás, elbukott.
* **dependsOnGroups**: csoportok listája, amitől a metódus függ. Ezzel szabályozhatjuk, hogy a metódus a csoportokban szereplő metódusok/osztályok/csoportok után kerüljön végrehajtásra
* **dependsOnMethods**: mely metódusoktól függ, mely metódusok után kerüljön végrehajtásra a teszt.
* **description**: a teszthez leírás adható meg, ami a teszt futása során megjelenik, információt adhat.
* **expectedExceptions**: kivételek listája, amit elvárunk a tesztesettől. Negatív teszt. Azt vizsgáljuk, hogyan reagál hibára, kivételt kell dobnia, ha ez megtörténik, akkor átment. Ezen kivételek listája adható meg itt.
* **groups**: csoportosíthatjuk a metódusokat, osztályokat különböző szempontok szerint. Ezeket a csoportokat aztán együtt kezelhetjük. Ezzel a paraméterrel adhatjuk meg a csoportok neveit, amikhez tartozik a annotációval jelölt metódus, osztály.
* **invocationCount**: hányszor szükséges futtatni a metódust.
* **timeOut**: mennyi idő alatt kell lefutnia a tesztnek. Ezredmásodpercben kell megadni. Ha ennyi idő alatt nem fut le, sikertelen.

...

A tesztmetódusok általában olyan hívásokat tartalmaznak, amelyek vagy kivételt dobnak, vagy az eredménnyel kapcsolatos elvárásokat írják le: adott bemenethez milyen eredményt várunk el, és ezt az elvárt eredményt hasonlítjuk össze a kapott eredménnyel (Assert osztály).

Egy-egy tesztmetódust kellően nagy számú bemenet esetén szükséges vizsgálni, csökkentve a hiba valószínűségét. DataProvider használatával egyszerűen megoldható, hogy ugyanaz a teszt sokszor, különböző adatkészletekkel futtatni tudjuk.

**@DataProvider** annotáció: az így jelölt metódus két dimenziós Object[][] tömböt ad vissza, amelyeket átad a rá hivatkozó tesztnek. A tömb egy sora egy teszteset paramétereit adja meg. A **@Tes**t annotáció _dataProvider_ paraméterével hivatkozhatunk a megfelelő DataProvider-re.

(**@Factory** annotáció: az így jelölt metódusok visszatérési értéke egy Object[] tömb. Ha a tesztosztály konstruktora tartalmaz paramétert, abban az esetben Factory metódust alkalmazva különböző pareméterekkel példányosíthatjuk az adott tesztosztályt. A tesztosztályok példányait adja vissza; Kb. mind a DataProvider, csak osztály esetén?)


Sikeres a teszt, ha nem dobott kivételt, vagy olyan kivételt dobott, amit elvártunk.

A TestNG által nyújtott funkciók biztosítják:

* jó tesztlefedettséget érjünk el azáltal, hogy könnyen írhatunk teszteket, melyeket ezután egyszerűen futtathatunk nagy számú, eltérő bemeneti értékek és elvárt eredmény esetén
* ellenőrizhető a szoftver funkcionalitása
* mérhető a teszt futási ideje
* terheléses teszt végzésére alkalmas

...
## Tesztvezérelt fejlesztés 


A tesztvezérelt fejlesztés (Test Driven Development - TDD) egy szoftverfejlesztési módszer, melynek lényeg, hogy a kódfejlesztés és a tesztírás folyamata nem válik szét, a futtatandó tesztek alapján történik a kód implementációja.

A programot ciklikusan fejlesztik a **tesztírás - implementáció - refaktorálás** lépéseket ismételve,  amíg a kívánt programrészlet el nem készül.

* **1. lépés: tesztírás**  
Tesztvezérlet fejlesztés során először a teszteket írják meg. Ez a _tests first_ megközelítés. Ebben a fázisban olyan teszt írása a cél, amin a program elbukik, hiszen az implementáció még nem készült el.

* **2. lépés: implementáció**  
A követekző fázisban a tesztnek megfelelő kód implementálása történik. A kódot addig fejlesztik, amíg sikeresen át nem megy a teszten.

* **3. lépés: refaktorálás**  
A harmadik fázisban a kód optimalizációja, minőségének javítása történik, ezzel párhuzamosan a tesztek minőségének javítása, karbantartása is szükséges. A kód minden módosítása után futtanti kell a teljes tesztkészlet, ezzel folyamatosan biztosítva, hogy az elkészült programrészlet az elvárások szerint működjön. 

Ezután ismét a tesztírás lépése következik, a ciklus folytatódik, az iterációk során kis lépésekkel egyre bővítve a tesztkészletet és a kódot.

A TDD szemlélete rákényszeríti a fejlesztőket, hogy eleve a teszteknek - így az elvárt működésnek - megfelelő implementációt valósítsanak meg, ami a felhasználó/megrendelő nézőpontját tükrözi. Továbbá a tesztkészlet a program működésének dokumentációját is magában hordozza.

## Viselkedésvezérelt fejlesztés

A Viselkedésvezérelt fejlesztés (Behavior Driven Development - BDD) alapját a tesztvezérelt fejlesztés adja, de más fejlesztési és tesztelési módszereket is felhasznál. A BDD során a fejlesztendő szotfver (elvárt) viselkedéséből indulnak ki, és a TDD-hez hasonlóan a _tests first_ technikát alkalmazza.
A program viselkedése axiómákkal leírható, amelyekből generálhatóak a tesztek, majd a teszteket figyelembe véve elkészíthető az implementáció.
(Viselkedést leíró axiomákat teszteljük végig)

### Gherkin
A Gherkin egy leíró nyelv, segítségével meghatározható a program viselkedése élő, beszélt nyelven. A Gherkin meghatározott szerkezetű, egyszerű angol szöveggel (illetve 60+ nyelven) írja le  a szoftver viselkedését meghatározó axiómákat. A nyelv úgy van megtervezve, hogy nem programozók által is könnyen érthető legyen - így a szoftver viselkesését a megrendelő is megfogalmazhatja, a teszteseteket megértheti - továbbá alkalmas a program dokumentálására is. De emellett elég struktúrált is ahhoz, hogy lehetővé tegye az üzleti elvárások tömör leírását. 

A Gherkin egy közös, könnyen érthető nyelvet biztosít a projekt különböző szereplői számára, amelyen a termék elvárt viselkedését megfogalmazhatják. 

Gherkin nyelven elkészített leírásokat .feature kiterjesztésű állományokba mentik, melyek egy-egy jellemző, funkcionalitás leírását tartalmazzák.

A "mondatok" kulcsszóval kezdődnek, amit bármilyen szöveg követhet a következő kulcsszóig.

A főbb kulcsszavak:
* **Feature**: a funcionalitás leírását vezeti be. A **Feature** kulcszó után, vele azonos  sorban a tulajdonság neve következik, majd egy opcionális leírás, a tulajdonság rövid magyarázata.
* **Scenario**: a viselkedés, ezzel együtt a teszteset megfogalmazása, majd meghatározása lépések sorozataként. Bármennyi tesztlépés megfogalmazható, de az átláthatóság és a kifejező erő megtartása miatt érdemes néhány lépésre korlátozni.
Szerkezete: (Adott kezdeti feltételek melett, amikor bekövetkezik egy esemény, akkor ez az elvárt eredmény)
   * **Given** kulcsszó, amit az előfeltételek, kezdeti összefüggések megfogalmazása követ. 
   * **When** kucsszó után egy esemény leírása következik
   * **Then** kulcszó vezeti be az elvárt eredmény leírását.
   * Amennyiben a lépések összetettek, **And** és **But** kulcsszavak használatával tovább részletezhetőek.
* Scanario Outline: sok esetben egy tesztet többször akarunk futtatni, különböző bemeneti értékekkel és különböző kimeneti eredményeket várva. Ez esetben használandó ez a kulcsszó. A tesztlépések megfogalmazásakor konkrét értékek helyett változókat használunk, melyeket **<>** jel jelöl.
* Examples: a Scenario Outline szakaszban használt változók számára ebben a részben adhatók meg konkrét értékek egy táblázat segítségével. A táblázat első sora a tesztlépések változóit tartalmazza, a következő sorok az egyes tesztesetekhez tartozó értékeiket.

A Gherkin nyelven tehát könnyen érthető formában, programozási nyelv használata nélkül leírható a program viselkedése, a tesztesetek természetes nyelven való megfogalmazása. 
Ezután kódra kell fordítani az így leírt tulajdonságokat, programozási nyelven kell leírni, hogy mit jelentenek a leírt mondatok. 
 
### Cucumber
A Cucumber egy tesztelési keretrendszer, mely lehetőséget ad viselkedés vezérelt fejlesztés illetve tesztelés alkalmazására és lehetővé teszi az automatikus funkcionális tesztelést. (?)
(Különböző nyelveket támogat, sok platform stb.)

(Ezt valahogy megfogalmazni:
Gherkinben viselkedés given-when-then lépések formájában -> Cucumberben ragasztó kód, amelyek futtatható kódként megvalósítják, definiálják ezeket a  lépéseket.
"Párosítás": annotáció + lépés leírása, Cu. reguláris kifejezést használ, az illeszkedő tesztesetek szerint fut az adott tesztlépés.
 Futtató: mely feature fileokat olvassa Cu., ami vezérli a hozzá "párosított" ragasztó kódot.)...

### Nem funkcionális tesztelés 

* nem a funkcionális követelmények ellenőrzése a cél
* egyéb, minőséget befolyásoló, számszerűsíthető jellemzők, követelmények vizsgálata
* helyes funkcionális működés mellett a program/rendszer teherbírásának, teljesítményének vizsgálata is szükséges

#### Teljesítmény teszt (Performance Testing)

* legelterjedtebb nem funkcionális teszt
* Többféle teljesítménnyel kapcsolatos elvárás fogalmazható meg=>típusok: mérnek valamit egy adott terhelés mellett: terheléses teszt, stresszteszt, kitartási teszt, csúcsteszt, stb.
tesztelés során azt szimulálják, hogyan működik a szoftver a valóságban, különböző körülmények fenállása esetén, körülmények között

##### Terheléses teszt (Load testing)

* hogyan viselkedik a rendszer a konkrét, várható/követelményként meghatározott terhelés mellett; 
* pl. webszerver mennyi kérést szolgál ki x idő alatt

* 1. Már létező funkcionális teszt felhasználása:
	* pl. funkcionális tesztek TestNG-vel, ezeket futtatjuk nagy számban
	* előny: nem kell új tesztet írni: funkcionális teszt=>terheléses teszt
	@invocationCount: hányszor kell futtatni a metódust
    @invocationTimeOut: az invocationCount értékének megfelelő számú futtatás összesített futási idejének maximuma, miliszekundumban megadva: ha ennél tovább tart, a teszt elbukik
    @threadPoolSize: hány szálon fusson az @invocationCount számú hívás. pl. webszerver több kérést kell párhuzamosan kiszolgáljon
   2. Gatling:
   * Direkt teljesítmény teszthez fejleszve
   * bonyi, de színes-szagos, könnyen használható teszt dokumentációt generál
   (olvasni)
   3. JMeter
   * terheléses tesztelésre és teljesítmény mérésére szolgáló nyílt forráskódú Java alkalmazás
   *  eredetileg web alkalmazások tesztelésére tervezték, de azóta bővült más teszt funkciókkal
##### Apache JMeter

* Nyílt forráskódú tesztelő eszköz, amelyet terheléses tesztelés végrehajtására és a  teljesítmény mérésére terveztek. Eredetileg webes alklamazások teszteléséhez készült, de a későbbiekben újabb tesztfunkciókkal bővült. 
* Tisztán Java nyelven írodott, platformfüggetlen
* alkalmazható funkcionális, terheléses, teljesítmény, regressziós stb. tesztek végrehajtására különböző alkalmazás/szerver/protokoll típusokon, mint:

  * HTTP, HTTPS
  * webszolgáltatások (webservices) protokolljai - SOAP
  * Adatbázis JDBC illesztőprogramokon keresztül
  * LDAP
  * JMS
  * e-mail protokollok: POP3, IMAP, SMTP
  * FTP szolgáltatás 
  
* futtatható parancssorból, de rendelkezik egy egyszerűen használható grafikus felülettel, nem szükséges programozni a tesztek írásához.
* A tesztterveket XML formátumban tárolja, így egy szövegszerkesztőben is létre hozhatunk teszttervet
* lehetővé tesz több szálon történő párhuzamos tesztelést
* felhasználható alkalmazások automatikus és funkcionális tesztelésére is.

##### Működése
A tesztelés során a rendszer valós viselkedését, működését szimuláljuk, eközben a JMeter rögzíti a választ, feldolgozza és statisztikát készít. 

A szimulációban egy felhasználókból álló csoport hívásokat küld egy szervernek/alkalmazásnak. A JMeter menti a szerver válaszait, összegyűjti az adatokat, amiből statisztikát készít. Ez a folyamat többször ismétlődhet, míg a szimuláció végetér, és a JMeter jelentést készít gráfok, táblák stb. formájában.

* ##### Teszt terv (Teszt Plan)

A teszt elkészítése során kell határozni, mit és hogyan akarunk tesztelni, milyen lépéseket kell végrehajtania a Jmeter-nek futása során. Ehhez létre kell hozni egy teszttervet (Test Plan), ami a futattandó teszteket tartalmazza.

A tesztterv kölönböző tesztelemekből épül fel:
* Thread Group: Az alkalmazást egyidejűleg futtató felhasználókat reprezentáló elem. A teljesítmény teszteknél fontos szempont, hogy mennyire jól tudja utánozni a való életbeli használatot, terhelést. Az ehhez szükséges paraméterek beállítására itt van lehetőség. 
   * Beállítható, hogy a JMeter a teszt futtatása során hány szálat használjon (tesztfelhasználók száma)
   * beállítható a felfutási idő értéke (ramp-up period), az az időtartam, amennyi idő alatt az összes tesztfelhasználó/szál belép a teszt futásába. Segítségével valósághűbbé tehető a tesztelés.
   * meghatározza az ismétlések számát.
   * a teszt futásának kezdte és vége meghatározható, így ütemezhető a tesztelés.

   A Thread Group a tesztterv kiindulási pontja, minden más elem ez alá kerül. 
 
A teszt folyamatát irányító vezérlő elemek: 
* Sampler: vezérlőelem, ami azt szimulálja, hogy mit csinál a felhasználó. Segítségével  a JMeter meghatározott kérést küld a szerver/alkalmazás felé. Főbb használható kérés típusok:
   * HTTP Request
   * FTP Request
   * JDBC Request
   * Java Request
   * SOAP/XML Request
   * RPC Requests
    
* Logikai verzélő elemek (Logic Controller): egy Thread Group-on belül szabályozza az alatta levő elemek végrehajtásának logikáját. 

* Listener: a Listener elemeken keresztül tekinthejtük meg a tesztfutás eredményét. A különböző elemek eltérő formában jelenítik meg az mért adatokból készült statisztikát. pl. táblázat, gráf, log file stb. 

(Legalább egy Thread Group, fentiek fába szerveződve, Thread Group alá)









## IV. Vizsgált eszközök összehasonlítása, elemzése. Konklúzió: adott feladatra melyik eszköz az ajánlott.
## V. Összefoglaló: nagyjából a bevezetés + eredmények
