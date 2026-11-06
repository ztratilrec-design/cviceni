# Cvičení

Webová aplikace pro zapisování a sledování denního cvičení (kliky, sedy-lehy, dřepy, shyby) přímo v sešitu Excelu – se zachováním všech vzorců, souhrnů a formátování.

**Aplikace:** https://ztratilrec-design.github.io/cviceni/

> **Důležité:** Aplikace pracuje pouze se **sešitem Excelu v předepsaném formátu** (listy po rocích, sloupce Pokuta / Hotovo / Zbývá pro 4 cviky, denní cíle v záhlaví). Sešit **není součástí** tohoto repozitáře – aplikace je určena pro **osobní použití**.

---

## Jak to funguje

Každý den má pro každý cvik **cíl**. Co nesplníte, přechází do dalšího dne (**z minula**) a navíc se k tomu připočte **pokuta** 10 % (zaokrouhleno nahoru):

**Zbývá = cíl + z minula + pokuta − hotovo** (při nule se zobrazí ✓)

Dluh se přenáší i mezi roky (listy 2026 → 2027 → …).

---

## Otevření a ukládání sešitu

Podporovaný formát: **.xlsx** (Excel 2007 a novější). Aplikace mění jen zapsané hodnoty a přepočítané výsledky – vše ostatní v souboru zůstává beze změny.

| Způsob | Otevření | Ukládání |
|---|---|---|
| **OneDrive** (doporučeno, počítač i telefon) | ⚙ → *Připojit OneDrive* (osobní účet Microsoft), pak výběr sešitu ve složkách nebo vložením odkazu | **Uložit** zapíše přímo do sešitu v OneDrive |
| **Místní soubor – Chrome / Edge na počítači** | *Otevřít…* nebo přetažení souboru do okna | **Uložit** zapíše přímo do stejného souboru (např. v synchronizované složce OneDrive) |
| **Místní soubor – ostatní prohlížeče / telefon** | *Otevřít…* | **Uložit kopii** stáhne aktualizovaný sešit |

Ikona ☁ vedle názvu souboru ukazuje, zda je sešit připojený k OneDrive (přeškrtnutý mrak = místní soubor).

### Synchronizace

- **Neuložené záznamy** se zobrazí žlutě a v pilulce vedle názvu souboru (např. *2 neuloženo*). Zůstávají v prohlížeči, dokud je neuložíte – nic se neztratí ani po zavření aplikace.
- **Autosave** (⚙) ukládá automaticky krátce po každé změně. Po uložení pilulka ukáže *✓ Uloženo 14:32*.
- **Změny odjinud** (Excel, jiné zařízení): při návratu do aplikace se sešit z OneDrive (nebo připojený místní soubor) automaticky načte znovu. Ručně lze obnovit **tažením dolů** na začátku stránky nebo tlačítkem *Načíst*.
- **Souběžné úpravy:** pokud se sešit mezitím změnil jinde, vaše záznamy se **sloučí do nejnovější verze** a uloží znovu.
- Při otevření jiného souboru s neuloženými záznamy se aplikace zeptá, zda je **ponechat**, nebo **zahodit**.
- Bez připojení k internetu aplikace funguje dál; uložit do OneDrive lze po obnovení připojení.

### Instalace jako aplikace

⚙ → **Nainstalovat aplikaci** (nebo v Chrome / Edge: ⋮ → *Nainstalovat aplikaci* / *Přidat na plochu*). Aplikace se pak spouští z plochy jako samostatné okno.

---

## Ovládání

- **Klávesnice:** v poli pro zadání hodnoty **Enter** přeskočí na další cvik (u posledního zavře klávesnici). **Esc** zavře nabídku ⚙.
- **Dotyk:** **přejetí doleva / doprava** přepíná karty Den → Historie → Statistiky. **Tažení dolů** na začátku stránky načte nejnovější verzi sešitu.
- **Tip:** podržením (nebo najetím myší) na pilulku, grafy a značky se zobrazí vysvětlivky.

---

## Karta Den

Zápis hodnot pro vybraný den.

- **Navigace:** ‹ / › předchozí a další den, výběr data, **Dnes** návrat na dnešek. Vedle je název dne a počet splněných cviků (*Splněno 2 ze 4*).
- **Karta cviku** ukazuje:
  - rozpis **zbývající dávky = cíl + z min. + pokuta** a velké číslo, kolik ještě zbývá (✓ po splnění),
  - pole **Hotovo** s tlačítky **− / +**,
  - **progress bar** – kolik z dnešní dávky je hotovo; **svislá značka** v barvě cviku ukazuje **minimum** (cíl + pokuta), při jehož splnění dluh dál neroste.
- **Rychlá tlačítka:**
  - **+10 / +25** (u shybů **+5 / +10**) – přičte k hodnotě,
  - **Min** – doplní hodnotu na minimum (cíl + pokuta),
  - **Rest** – doplní vše, co zbývá (včetně dluhu z minula).
- Budoucí dny zobrazují jen denní cíl.

---

## Karta Historie

Měsíční tabulka v barvách původního listu: datum, den v týdnu a pro každý cvik **Pokuta / Hotovo / Zbývá** (s datovým pruhem), poslední sloupec ✓ = splněny všechny čtyři cviky. Dole je **součet za měsíc**, dnešní řádek je zvýrazněný.

- **Navigace:** ‹ / › předchozí a další měsíc, výběr měsíce, **Dnes** návrat na aktuální měsíc.
- **Kliknutí na řádek** otevře daný den v kartě **Den**; kliknutí na hodnotu cviku navíc rovnou nastaví kurzor do jeho pole.

---

## Karta Statistiky

- **Filtry** (zůstávají nahoře při posouvání): *Posledních 7 dní*, *Tento měsíc*, *Celé období*, nebo výběr **roku** a **měsíce**. Všechny údaje níže se počítají za zvolené období.
- **Trend** – klouzavý průměr (7denní, u dlouhých období 4týdenní) v % denního cíle, s malým grafem a šipkou ▲/▼ za poslední týden.
- **Celkově za období** – perfektní dny, aktuální a nejdelší série, dny se záznamem, opakování celkem a „cena pokut“.
- **Podle cviku** – průměr za den, splněné dny, pokuty, nejlepší den a zbývající dluh ke konci období.
- **Grafy** *Hotovo za den* a *Zbývá* – po najetí / dotyku ukazují hodnoty pro konkrétní den.
- **Po měsících** – přehled za rok; **kliknutím na měsíc** se nastaví jako filtr.
- **Kalendář** – barva dne podle počtu splněných cviků; **kliknutím na den** se otevře v kartě **Den**.

---

## Nastavení (⚙)

OneDrive (připojit / vybrat jiný sešit / odpojit), **Autosave**, **Tmavé schéma**, **Přidat do .xlsx další rok** (nový list navazující na předchozí rok), **Nainstalovat aplikaci** a **Ochrana soukromí**.

---

## Soukromí

Aplikace nemá vlastní server ani sledování; data zůstávají ve vašem sešitu a v prohlížeči. Podrobnosti: [Ochrana soukromí](https://ztratilrec-design.github.io/cviceni/soukromi.html).

## Soubory v repozitáři

| Soubor | Účel |
|---|---|
| `index.html` | celá aplikace (jeden soubor, včetně knihovny JSZip) |
| `manifest.webmanifest`, `icons/` | instalace jako aplikace, ikony |
| `sw.js` | offline režim (při připojení se vždy načte nejnovější verze) |
| `soukromi.html` | prohlášení o ochraně soukromí |
