# 3D Inventory - Asztali Alkalmazás

## Leírás

A **3D Inventory** egy hatékony asztali alkalmazás 3D modellek gyűjteményének fa-szerkezetes menedzseléséhez. Az alkalmazás segít rendszerezni, nyomon követni és katalogizálni a modelleidet hierarchikus kategóriák (ágak) alatt.

## Fő Funkciók

### 📁 Hierarchikus Szervezés
- **Fa-szerkezet**: Szabad szervezés ágak és kategóriák alá
- **Metaadatok az ágakhoz**: Ikon, leírás, estatisztikák
- **Gyűjtemény metrikák**: Meglevő vs. hiányzó modellek aránya, átlagos értékelések

### 📦 Modellek Kezelése
- **Saját és hiányzó modellek**: Felveheted a meglévő és még beszerzendő modelleket
- **Gazdag metaadatok**: 
  - 📸 Fényképek (Drag-and-drop támogatás)
  - ⭐ Értékelés (1-5 csillag)
  - 📝 Jegyzetek és leírások
  - 🔗 URL-ek (forrásanyagok, webshop linkek)
  - 💰 Ár
  - 🏷️ Címkék (tag-ek)
  - 📂 Fájl lokáció

### 🔍 Keresés és Szűrés
- Szöveges keresés a modellek között
- Keresés tag alapján
- Fejlett szűrési lehetőségek (ár, értékelés, állapot, stb.)

### 🏷️ Címkék Kezelése
- Központosított tag-kezelő felület
- Új címkék létrehozása, szerkesztése, törlése

### 📋 Szervezési Funkciók
- Ágak és modellek mozgatása az ágak között
- Elemek törlése

## Technológia Stack

- **Frontend**: React
- **Desktop Framework**: Electron
- **Adatbázis**: SQLite (helyi tárolás)
- **Fejlesztés**: TypeScript

## Felhasználói Felület

### Alapnézet (Böngészés)
- **Bal oldal**: TreeView a hierarchia böngészéséhez
- **Jobb oldal**: Kiválasztott elem metaadatai és szerkesztési opciók

### Keresési Nézet
- **Bal oldal**: Egyszerű lista a keresési eredményekből
- **Jobb oldal**: Kiválasztott elem részletei

## Telepítés

```bash
cd 3DInventory-app
npm install
npm run build
npm run dev
```

## Projekt Szerkezete
```
3DInventory/
├── 3DInventory-app/        # Electron alkalmazás
│   ├── src/
│   │   ├── main/           # Electron main process
│   │   ├── preload/        # Preload scripts
│   │   └── renderer/       # React frontend
│   └── package.json
├── Wiki/                   # Dokumentáció
│   ├── Architecture/       # Architektúra dokumentáció
│   ├── Features/           # Funkció és felhasználói történet dokumentáció
|   └── UI/                 # UI prototípusok és leírók
└── 3DInventory_PRD.md      # Termékkívánalmak
```
