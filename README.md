# Cvičení

Webová aplikace pro zapisování a sledování denního cvičení (kliky, sedy-lehy, dřepy, shyby) v sešitu Excelu **Cvičení_20xx.xlsx** – se zachováním všech vzorců, souhrnů a formátování sešitu.

**Aplikace:** https://ztratilrec-design.github.io/cviceni/

- **Den** – zápis hodnot pro vybraný den, co zbývá (cíl + z minula + pokuta).
- **Historie** – měsíční tabulka v barvách původního listu.
- **Statistiky** – období (7 dní, měsíc, rok, celé období), série, grafy, kalendář.
- **⚙ Nastavení** – OneDrive, Autosave, tmavé schéma, přidání dalšího roku do sešitu, ochrana soukromí.

Sešit lze otevřít ze zařízení, nebo (po přihlášení účtem Microsoft) přímo z OneDrive – aplikace pak ukládá zpět do OneDrive.
Aplikaci lze nainstalovat jako app (Chrome → ⋮ → Nainstalovat aplikaci) a funguje i offline.

[Ochrana soukromí](https://ztratilrec-design.github.io/cviceni/soukromi.html) – aplikace nemá vlastní server ani sledování; data zůstávají ve vašem sešitu.

## Soubory

| Soubor | Účel |
|---|---|
| `index.html` | celá aplikace (jeden soubor, včetně knihovny JSZip) |
| `manifest.webmanifest`, `icons/` | instalace jako aplikace, ikony |
| `sw.js` | offline režim (aplikace se při připojení vždy načte v nejnovější verzi) |
| `soukromi.html` | prohlášení o ochraně soukromí |
