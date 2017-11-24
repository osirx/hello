# Házi feladat:
1. Markdown text-file formázás tutorial (remélem tetszeni fog)

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

### A) Teszttípusok: (Különféle típusok aszerint, hogy  milyen tulajdonságokat tesztel)

- Funkcionális teszt: a szoftver funkcionálisan helyes-e, azt csinálja-e, amit elvárunk tõle. Fekete doboz.

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
## IV. Vizsgált eszközök összehasonlítása, elemzése. Konklúzió: adott feladatra melyik eszköz az ajánlott.
## V. Összefoglaló: nagyjából a bevezetés + eredmények