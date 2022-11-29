# Pénzügyi alkalmazás

A feladat egy olyan felhőalapú pénzügyi web-alkalmazás készítése a megrendelő számára, ami kiterjedten a céges számlákat kezelni képes. A szoftverrel képesek leszünk bejövő és kimenő számlákat rögzíteni, a számlákra fizetési tételeket írni, majd könyvelni azt és a fizetést elősegíteni. Mindezen pontokat jól szervezetten, minden lépésnél külön szerepköröket alkalmazva meghatározhatjuk, hogy melyik személy milyen lépésre jogosult (pl.: ki a könyvelő).  

## Ötletelés:
> Varga Péter:

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


## Feladatok:

1. A szoftver által támogatandó tevékenység/funkcionalitás szabad szöveges leírása: 4P
2. Táblázatos rendszerezés (struktúrált szöveg): 4P
3. Használati eset diagram: 4P
4. Aktorok részletes leírása: 3P
5. Használati esetek részletes szöveges ismertetése: 4P
6. Tevékenység diagramok az egyes használati esetekhez: 4P
7. Állapotgép diagramok: 4P
8. Kontextus diagram: 3P
9. Szakarchitektúra diagram: 3P
10. Projektterv MS Projektben: 6P
11. Projekt kockázatok elemzése (halszálka, kockázat értékelés + Pareto, kockázat tervezés (stratégia), SWOT): 5P
12. Az adatbázis egyed-kapcsolat (ER) modellje és az ennek alapján készült relációs vagy Entity Framework modell: 6P
13. A beadott dokumentáció külalakja: 1P
14. A teljes dokumentációs anyag egységességének, összhangjának, és az esetleg megoldott pluszfeladatoknak az értékelése: 2P
15. Felületterv elkészítése: 3P
16. Feladat feltöltés határidőre: 4P

Összesen tehát 60P lehet, szerintem ezt kár eröltetni :)

Ki és Mit szeretne csinálni?
Szerintem mindenki válasszon ki magának olyan dolgokat amikre azt tudja mondani, hogy ennyi idő alatt meg tudja csinálni.
Amiben nem biztos, hogy vállalná / meg tudná csinálni oda tegyen kérdőjelet, és majd ha mindenki felcsipkedte a feladatokat, akkor megbeszéljük, hogy mi legyen azokkal.
- Balog Olivér:
- Deszpod László:
- Molnár Gergő:
- Varga Péter: 1, 2, 3(?), 4(?)
