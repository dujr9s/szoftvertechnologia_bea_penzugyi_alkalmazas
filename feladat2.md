# Táblázatos rendszerezés (struktúrált szöveg)

Az alábbi táblázatban a megvalósítandó funkciók strukturált leírása látható, az aktorokhoz rendelve.
A projekthez fűződően a következő aktorok jelennek meg (mellettük a táblázatos jelölés):
- Ügyfél: Ü
- Eladó / Szervizes: E
- Könyvelő: K
- Admin: A

| Ki?        | Milyen gyakran? | Mit?                                                     | Megjegyzés                            |
| ---------- | --------------- | -------------------------------------------------------- | ------------------------------------- |
| E, K, A    | 1               | Bejelentkezés.                                           | Felhasználónév, Jelszó                |
| Ü, E, K, A | 0..n            | **Számlák megtekintése**                                 |                                       |
| Ü          | 0..n            | &ensp; Linkre kattintás.                                 | Email-be kapott link                  |
| E, K, A	   | 1..n	           | &ensp; Számlák keresése.                                 | Meglévő számlák közt                  |
| E, K, A	   | 1..n	           | &ensp; Számla megnyitása.                                |                                       |
| Ü, E, K, A | 0..n	           | **Számlák letöltése**                                    | PDF letöltés                          |
| Ü          | 0..n            | &ensp; Letöltés linkre kattintás.                        |                                       |
| E, K, A    | 0..n            | &ensp; Számlák keresése.                                 |                                       |
| E, K, A    | 0..n            | &ensp; Letöltés gombra kattintás.                        |                                       |
| E          | 1..n            | **Új számla kiállítása**                                 |                                       |
| E          | 1..n            | &ensp; Alap adatok felvitele.                            | Név, cím, email                       |
| E          | 1..n            | &ensp; Javítási tételek rögzítése árral, garanciaidővel. |                                       |
| E          | 1..n            | &ensp; Számla zárása.                                    | Automatikus kiküldés                  |
| K          | 1..n            | **Számlák könyvelése**                                   |                                       |
| K          | 1..n            | &ensp; Könyvelési feladatok elvégzése.                   |                                       |
| K          | 1..n            | &ensp; Könyvelt státusz bejegyzése.                      |                                       |
| A          | 1               | **Felhasználókezelés**                                   |                                       |
| A          | 1               | &ensp; *Új felhasználó hozzáadása.*                      |                                       |
| A          | 1               | &ensp;&ensp; Adatbevitel.                                | Név, Beosztás, Felhasználónév, Jelszó |
| A          | 1               | &ensp;&ensp; Szerepkör, jogosultság beállítása.	        | Eladó vagy Könyvelő, esetleg Admin    |
| A          | 1               | &ensp; *Felhasználó módosítása.*                         |                                       |
| A          | 1               | &ensp;&ensp; Felhasználó kijelölése.                     |                                       |
| A          | 1               | &ensp;&ensp; Adatmódosítás, mentés.                      |                                       |
| A          | 1               | &ensp; *Felhasználó törlése.*                            | Csak logikai                          |
| A          | 1               | &ensp;&ensp; Felhasználó kijelölése.                     |                                       |
| A          | 1               | &ensp;&ensp; Törlés.                                     |                                       |
