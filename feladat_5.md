Authentikálás

Az ügyfél bemegy az üzletbe és vásárol bizonyos termékeket. Miután az ügyfél bevásárolt és a kasszához ér, a kasszakezelő bejelentkezik az alkalmazás felületén, ahol az alkalmazás autentikálja a felhasználót (aki jelen esetben a kasszás, ő fogja berögzíteni a számlát).
Az autentikáció kliens és szerver oldalon is megtörténik, szerver oldalon természetesen adatbázisból jönnek az adatok, a jelszó hash-kódolva van. Azáltal, hogy sikeresen bejelentkezett a kasszás, az alkalmazás tovább engedi őt a felületre. Ha nem sikerült autentikálnia magát, akkor a rendszer hibaüzenetet küldd arról, hogy melyik megadott adat helytelen.

Számla rögzítés

Miután a kasszás sikeresen bejelentkezett, az alkalmazás különböző szerepköröket különböztet meg, köztük a kasszás, vagy számla rögzítőt is. A kasszásnak lehetősége van a felületen új számlát kiállítani, amit aztán pdf formájában, céges számlaként ki tud nyomtatni. A számlát a rendszer leellenőrzi, köztük a dátum helyességét, amikorra a számla lett írva, az számlára írt összeget és a számla tételek szummáját. Ha mindent rendben talál, a számla kiállítódik, ha nem akkor megerősítést kér a kasszástól, hogy biztosan így szeretné e a számlát.

Számla jóváhagyás

Ezen a felületen a könyvelő, vagy az admin (aki legtöbb esetben pénzügyi háttérrel rendelkezne, vagy pénzügyi segítséget tud kapni) ellenőrizheti a számlákat, amiket a kasszás kiállított, itt lehetne őket sztornózni, esetleg a túlfizetéseket rendezni. Ha mindent rendben talál, akkor a számlát egy gomb segítségével jóvá tudja hagyni, illetve hibás rögzítésként is tudja jelölni őket, ha a számlán hibát talál.

Könyvelés

A könyvelő az autentikáció után egy, a számlázástól elválasztott, de ugyanazokkal a számlákkal kapcsolatban álló felületen találja magát, ahol egy a könyveléshez átláthatóbb módon megjelenítődnek a számlák és lehetőség van kettős könyvelés szerint rendezi is azokat. A felület színekekkel és üzenetekkel jelezné, hogy a beépített logika szerint, rendben vannak e a számítások, illetve gépiesen számított mezők is lennének, mint például a bruttó-nettó-áfa.

Fiókkezelés

Admin kezelőfelület a fiókok karbantartásához, meghatalmazásokhoz bizonyos műveletekre. Egy felhasználóbarát felületen lehetne itt listázni a rendszerben lévő összes fiókot, és lista szerűen rendezni azokat. Egy-egy felhasználóhoz tartozó "módosít" gombra kattintva, egy lenyíló ablakban lehetőség van az engedélyeket megadni a fiók számára. 

Számla kiküldés

A rendszer azon kívül, hogy a számlát megengedi kinyomtatni, elsősorban digitális számlákat használna. A kasszás által kiállított számla kiküldésre kerül a számlázott ügyfélnek, ha az ő e-mail címe már benne szerepel a rendszerben, vagy megadja azt. Ez úgy történik, hogy a  számla iktatása után a rendszer automatikusan kiküldi azt egy előre formázott sablon szerint. Természetesen egy kérést küld a frontend a backend számára, hogy küldje el a pdf-et a megadott e-mail címre. 