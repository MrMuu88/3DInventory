# 1. A Program Célja

Egy asztali alkalmazás készítése, amellyel fa-struktúrába szervezve (hierarchikusan) nyomon követhető, hogy milyen 3D modellekkel (fájlokkal) rendelkezel. A cél a gyűjtemény vizuális és strukturált menedzselése.

---

# 2. Funkcionális Követelmények

## 2.1. Ágak / Kategóriák (Hierarchia)
Minden ághoz metaadatként a következőket lehessen hozzárendelni:
- Ikon
- Rövid leírás
- Új al-ág létrehozási opció

Az egyes ágak alatt lehessen látni:
- Hány modellfájl van meg, és mennyi hiányzik (százalékban kifejezve).
- Az alatta lévő modellek összesített, átlagos értékelését.

## 2.2. Modellek
Minden ághoz lehessen modellfájlokat rendelni, valamint **hiányzó modelleket** is felvenni (amelyekkel még nem rendelkezel).

Egy modellhez a következő metaadatokat lehessen csatolni:
- **Fényképek**: A képek hozzáadása Drag-and-Drop módon is lehetséges legyen.
- **Értékelés**: Csillagos (1-5) értékelés.
- **Leírás vagy jegyzet**: Szabad szöveges formátum.
- **URL-ek**: Források, webshop linkek.
- **Fájl lokáció**: Az MVP-ben a 3D modell megtekintésére elég egy "Tartalmazó mappa megnyitása" gomb (a rendszer beépített fájlkezelőjének segítségével).
- **Ár**
- **Tag-ek (Címkék)**

## 2.3. Kezelési és Szervezési Funkciók
- **Elemek mozgatása/törlése**: Al-ágakat és modelleket lehessen áthelyezni más ágak alá, vagy épp törölni. (*MVP-ben nem szükséges a drag-and-drop mozgatás a fában, elég egy menüből kiválasztani a cél ágat.*)
- **Tag-ek (címkék) központosított kezelése**: Új létrehozása, szerkesztése, törlése egy felületen.
- **Keresés és Szűrés**:
  - Lehessen keresni modellt szöveg vagy Tag alapján.
  - Lehessen kiterjedten szűrni a modelleket (pl. ár, értékelés, meglévő/hiányzó stb.).

---

# 3. UI / Layout (Felhasználói Felület)

## 3.1. Alapnézet (Böngészés)
- **Bal oldal**: TreeView (fa-nézet) a hierarchia böngészéséhez és az ágak / modellek eléréséhez.
- **Jobb oldal**: Ha a fában ki van választva egy elem (ág vagy modell), ezen az oldalon jelenjenek meg a hozzá tartozó metaadatok és szerkesztési opciók.

## 3.2. Keresési Nézet
- **Bal oldal**: Keresés vagy szűrés futtatása esetén a TreeView helyett egy **egyszerű lista** jelenjen meg a találatokkal.
- **Jobb oldal**: A listából kiválasztott elem részleteit (ugyanúgy, mint alapnézetben).

---

# 4. Technikai Követelmények

- **Keretrendszer**: Electron alapú vastagkliens asztali alkalmazás.
- **Frontend**: React.
- **Adatbázis**: Lokális SQLite adatbázis a metaadatok, hierarchia és fájl útvonalak stabil tárolására.


