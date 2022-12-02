# Pénzügyi alkalmazás

A feladat egy olyan felhőalapú pénzügyi web-alkalmazás készítése a megrendelő számára, ami kiterjedten a céges számlákat kezelni képes. A szoftverrel képesek leszünk bejövő és kimenő számlákat rögzíteni, a számlákra fizetési tételeket írni, majd könyvelni azt és a fizetést elősegíteni. Mindezen pontokat jól szervezetten, minden lépésnél külön szerepköröket alkalmazva meghatározhatjuk, hogy melyik személy milyen lépésre jogosult (pl.: ki a könyvelő).  

## Ötletelés:
```
Varga Péter:
```

Tekintve az idő szűkösségét, tökeredjünk valami egyszerű projektre.
Nekem a következők a javaslataim nagyvonalakba a funkciókra és a szerepkörökre nézve:

Szerepkörök:
- Ügyfél vagy felhasználó simán. 
- Eladó vagy számlázó, aki a számlákat létrehozza, a tételeket rögzíti.
- Könyvelő vagy számlakezelő.
- Adminisztrátor

Én nagyjából ennyi szerepkörrel megelégednék, bár lehet, hogy a könyvelőt is kihagynám :)

Funkciók: 
- Bejelentkezés: Ez minden szerepkörnek kötelező lenne, kivéve az ügyfelet.
- Ügyfél nézet: Az email-ben kapott linkre kattintva ez jelenne meg az ügyfél részére.
Bejelentkezés nélkül elérhető lenne a számára, és itt tudná megtekinteni az online számláját, és letölteni azt.
- Számlák létrehozása, tételek rögzítése, számla mentése / kiállítása.
Ez lenne az eladói szerepkörhöz rendelve, ő tudna létrehozni számlákat, és rögzíteni rá az eladott tételeket, majd menteni, azaz kiállítani azt a vásárló részére, aki erről email értesítést kap.
Nyilván itt lehetne még beleálmodni dolgokat, hogy csak addig módosíthassa a számlát amíg nincs lezárva stb... de szerintem ez csak tovább bonyolít mindent.
- Számlák kezelése, beküldése: Ez lenne mondjuk a könyvelői szerepkörhöz rendelve.
Ő tudná felvenni a beérkező számlákat, és lekönyvelni azokat a meglévő kimennőekkel együtt. (jelentsen ez bármit is ?)
- Adminisztrátori szerepkör: Ő lenne az aki el tudja végezni az esetleges módosításokat a számlákon, törölni tudja azokat (de persze csak logikailag, fizikálisan semmi nem tünne el a felhőből). Ő tudna létrehozni és törölni felhasználókat a fenti két szerepkörnek megfelelően.
```
Balog Olivér:
```
Teams-es megbeszélésből kivágva:

> Olivér:
> 
> Ez kb. egymás után egy folyamat, amihez tartoznak szerepkörök, valahogy így,
> legyen mondjuk csak a fizetendő számkákkal foglalkozva (tehát mi nem számlázunk):
> Kapunk egy fizika számlát mondjuk egy bármilyen boltban a cégünk nevére. 
> Ezt a számlát fogjuk és a szoftverünk segítségével a számla iktató egyszerűen beírja a számla adatait
> (pl. ki számlázta, kinek a nevére, beolvassa a számlát pdf-ként, stb..).
> 
> A pénzügyi rögzítő az annyi lenne, hogy a pénzügyi adatokat, 
> tehát a pénznemet (lehet esetleg külföldi számla),a számlán lévő tételeket
> (ugye, egy számlán lehet több tétel, mint mondjuk, listázva a termékeket és az árukat, amit a boltban vettünk),
> nagyjából így jó is neki.
> 
> Számla jóváhagyó ellenőrzi, átnézi az összes adatot, nagyobb cég esetén leosztja a cég részlegei között 
> (mondjuk egy nagy cég, aminek van egy IT részlege és van egy Pénzügyi részlege).
> 
> A könyvelő egyértelmű, valahogyan úgy nézne ki, hogyha a számlát jóváhagyta, 
> akkor a könyvelő a könyvelői felületen azt látja és lekönyveli 
> (szerintem nem lesz szükségünk arra a feladathoz, hogy tudjuk, hogyan kell könyvelni).
>
>> Péter:
>> 
>> A számla iktató tehát az lenne aki kézhez kapja a fizikai számlát,
>> (legyen ez papír vagy akár online számla) és ezen számla adatait veszi fel,
>> illetve csatolja a számlát pdf-ként. Ez világos.
>> 
>> A pénzügyi rögzítő (ezt annyira nem értem): Ő kapja meg az iktató által készített számlát,
>> és az ezen lévő tételeket viszi fel külön valahova?
>> 
>> Aztán a jóváhagyó megkapja az értesítést, hogy új tételeket rögzítettek az adott számlához, 
>> és neki jóvá kell hagynia? Ezt a leosztást annyira nem értem? Miért kell leosztani ezeket?
>>
>>> Olivér:
>>> 
>>> Igen, jól érted. Ez egy folyamat, olyan sorrendben, ahogy leírtam. 
>>> Először az iktató csinálja a dolgát, ameddig tudja a jogosultságával. 
>>> Ugyanezt a "számlát" megtudja nyitni a pénzügyi rögzítő, csak ő neki már más dolgokhoz lesz joga nyúlni.
>>> És így tovább a többinél is.
>>> 
>>> A jóváhagyó egyébként lehet akár annyi is, hogy csak jóváhagyja és engedélyezi a számlát. Legyen ez a mi adminunk.


```
Deszpod László:
```
```
Molnár Gergő:
```

## Végleges feladat ismertetése nagyvonalakban:
~~A Projekt arról szólna, hogy tervezzünk egy felhős pénzügyi számlakezelő alkalmazást.
Az alkalmazás csak a bejövő számlákat kezelné, tehát mi nem állítunk ki számlát, hanem csak felvesszük azokat amiket kaptunk.
Pl.: A cég rendel valamit valahonnan, vesz valamit valami boltból, és erről számlát kap. Mi csak ezekkel foglalkozunk!~~

~~Az alábbiakban a szerepköröknél leírom a teljes folyamatot nagyjából:~~

~~Szerepkörök:~~
~~- Számla iktató: Ő az aki kézhez kapja a számlát (mindegy milyen módon, ez itt nem lesz lényeges).
Ezt a számlát fogja és rögzíti az alkalmazásban. Legyenek a rögzítendő adatok a következők: Ki állította ki a számlát?, Kinek a nevére?, esetleg valami belső megnevezés, és belső számla sorszám, és PDF-ként rögzíti a számlát a fenti ürlap mellé.~~
~~- Pénzügyi rögzítő: Ő figyeli a beérkezett számlákat. A számlán lévő tételeket külön rögzíti valahol (külön tábla) a számla sorszámához hozzárendelve.~~
~~- Számla jóváhagyó vagy Admin: Ő ellenőrzi a fentieket és jóváhagyja a számlát, vagy törli, módosítja, és ő kezeli a felhasználókat is.~~
~~- Könyvelő: A jóváhagyást követően ő fogja lekönyvelni a számlát.~~

***VÁLTOZÁS:***

Úgy alakult, hogy az 1. verziót csináljuk meg, amely röviden a következő lenne.
Tervezzünk egy felhős pénzügyi számlázó alkalmazást, amely lehetőséget nyújt arra, hogy a cégnél dolgozó eladók online számlát állíthassanak ki az ügyfelek részére.

Az alábbiakban a szerepköröknél leírom a teljes folyamatot nagyjából:

Szerepkörök:
- Az **ügyfél** bemegy az üzletbe (vagy webshop, de ez most mindegy), és vásárol.
- A pénztárhoz érve az **eladó** számlát készít a számára, amelyen rögzíti a megvásárolni kívánt tételeket.
- A **könyvelő** bizonyos időközönként ellenőrizné, lekönyvelné a rendszerben keletkezett új számlákat.
- Az **admin** az igényeknek megfelelően néha ellenőrzi a rendszer működését.
Neki van jogköre a fenti két felhasználó típus kezelésére is (törlés, módosítás, létrehozás).
- Csak, hogy körbeérjünk, az **ügyfél** a kapott email-es értesítés hatására, a linkre kattintva meg tudja nyitni a számláját,
és le tudja tölteni. Ehhez semmilyen bejelentkezésre nincs szüksége, **ellenben az összes többi felhasználó típussal akiknek igen**.

## Feladatok:

- [X] 1. A szoftver által támogatandó tevékenység/funkcionalitás szabad szöveges leírása: 4P
- [X] 2. Táblázatos rendszerezés (struktúrált szöveg): 4P
- [X] 3. Használati eset diagram: 4P
- [ ] 4. Aktorok részletes leírása: 3P
- [ ] 5. Használati esetek részletes szöveges ismertetése: 4P
- [ ] 6. Tevékenység diagramok az egyes használati esetekhez: 4P
- [ ] 7. Állapotgép diagramok: 4P
- [ ] 8. Kontextus diagram: 3P
- [ ] 9. Szakarchitektúra diagram: 3P
- [ ] 10. Projektterv MS Projektben: 6P
- [ ] 11. Projekt kockázatok elemzése (halszálka, kockázat értékelés + Pareto, kockázat tervezés (stratégia), SWOT): 5P
- [ ] 12. Az adatbázis egyed-kapcsolat (ER) modellje és az ennek alapján készült relációs vagy Entity Framework modell: 6P
- [ ] 13. A beadott dokumentáció külalakja: 1P
- [ ] 14. A teljes dokumentációs anyag egységességének, összhangjának, és az esetleg megoldott pluszfeladatoknak az értékelése: 2P
- [ ] 15. Felületterv elkészítése: 3P
- [ ] 16. Feladat feltöltés határidőre: 4P

Összesen tehát 60P lehet, szerintem ezt kár eröltetni :)

Ki és Mit szeretne csinálni?
Szerintem mindenki válasszon ki magának olyan dolgokat amikre azt tudja mondani, hogy ennyi idő alatt meg tudja csinálni.
Amiben nem biztos, hogy vállalná / meg tudná csinálni oda tegyen kérdőjelet, és majd ha mindenki felcsipkedte a feladatokat, akkor megbeszéljük, hogy mi legyen azokkal.
- Balog Olivér: 5, 10, 15
- Deszpod László: 6, 7, 8, 9
- Molnár Gergő: 11, 12, és a Dokumentum (a nagy Mű) megszerkesztése.
- Varga Péter: 1, 2, 3, 4
