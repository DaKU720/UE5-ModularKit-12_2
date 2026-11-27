# Modules plan

Plan kitu modułowego **Cyberpunk Sci-Fi Slum Habitation Block**: siatka, lista 24 modułów, przydział i reference board dla każdego modułu.

Każdy moduł ma dwa pliki:

- `NN_<Moduł>.drawio`: edytowalny board (otwierasz w [app.diagrams.net](https://app.diagrams.net) przez *File > Open from > Device*),
- `NN_<Moduł>.pdf`: podgląd, który GitHub pokazuje od razu po kliknięciu.

Na boardzie: wymiary, materiały, osoba, opis modułu, zdjęcia referencyjne z czerwonymi ramkami (numer ramki = pozycja w legendzie pod zdjęciem) i pusta ramka na screenshot blockoutu.

## Siatka

| Parametr | Wartość |
|---|---|
| Krok siatki | 0,5 m (snapping UE5: 0,5; detale 0,1) |
| Moduł ściany | 2 m szer. x 3 m wys. |
| Kondygnacja | 3 m (2,8 m w świetle + 0,2 m stropu) |
| Pół-moduł | 1 m |
| Grubość ściany i stropu | 0,2 m (snapping 0,1) |
| Wysokości kondygnacji | 0, 3, 6, 9 m |
| Pivot | dolny lewy narożnik od strony fasady |
| Blender | Scale grid 0,5, eksport w metrach (Unit Scale 1.0) |

## Konwencje

- Nazwa meshu w UE5: `SM_<Moduł>`, np. `SM_Wall_Window`.
- Obrys modułu musi się zgadzać z wymiarami z tabeli, żeby moduły łączyły się na siatce bez szczelin.
- Elementy, które będą miały inny materiał (szkło, neon emissive), od razu jako osobna część meshu.

## Moduły i przydział

Trudne moduły oznaczone `*`. Każda osoba ma 6 modułów, w tym 3 trudne.

| # | Moduł | Wymiary (m) | Materiały | Osoba | Board |
|---|---|---|---|---|---|
| 01 | Wall_Solid | 2 x 0,2 x 3 | beton z plamami, tynk | Dawid | [pdf](01_Wall_Solid.pdf) |
| 02 | Wall_Half | 1 x 0,2 x 3 | beton z plamami, tynk | Dawid | [pdf](02_Wall_Half.pdf) |
| 03 | Wall_Window* | 2 x 0,2 x 3, okno 1 x 1,5 | beton, rama metalowa, szkło | Dawid | [pdf](03_Wall_Window.pdf) |
| 04 | Wall_Door* | 2 x 0,2 x 3, drzwi 1 x 2,2 | beton, blacha drzwi, naklejki | Dawid | [pdf](04_Wall_Door.pdf) |
| 05 | Wall_Shopfront* | 2 x 0,5 x 3 | metal, szkło, roleta | Dawid | [pdf](05_Wall_Shopfront.pdf) |
| 06 | Corner_Pillar | 0,5 x 0,5 x 3 | beton, rury | Dawid | [pdf](06_Corner_Pillar.pdf) |
| 07 | Floor_Slab | 2 x 2 x 0,2 | beton | Maria | [pdf](07_Floor_Slab.pdf) |
| 08 | Floor_Ledge | 2 x 0,5 x 0,2 | beton z odpryskami | Maja | [pdf](08_Floor_Ledge.pdf) |
| 09 | Foundation_Plinth | 2 x 0,5 x 0,5 | beton, brud | Maja | [pdf](09_Foundation_Plinth.pdf) |
| 10 | Roof_Parapet | 2 x 0,2 x 1 | beton, blacha | Maja | [pdf](10_Roof_Parapet.pdf) |
| 11 | Roof_Corrugated* | 2 x 2, spadek 0,5 | blacha falista, rdza | Maja | [pdf](11_Roof_Corrugated.pdf) |
| 12 | Awning* | 2 x 1 | blacha falista, wsporniki | Maja | [pdf](12_Awning.pdf) |
| 13 | Balcony* | 2 x 1 x 1 | beton, barierka stalowa | Maria | [pdf](13_Balcony.pdf) |
| 14 | Railing | 2 x 0,1 x 1 | stal, rdza | Maria | [pdf](14_Railing.pdf) |
| 15 | Stairs_Metal* | 1 x 3 x 3 | stal, kratka | Maria | [pdf](15_Stairs_Metal.pdf) |
| 16 | Addon_Box* | 2 x 2 x 3 | blacha, deski, panele | Maria | [pdf](16_Addon_Box.pdf) |
| 17 | Rooftop_Equipment* | 1 x 1 x 1,5 | blacha, rdza | Maja | [pdf](17_Rooftop_Equipment.pdf) |
| 18 | Utility_Pole* | 0,5 x 0,5 x 8 | beton, transformator, kable | Zuza | [pdf](18_Utility_Pole.pdf) |
| 19 | Neon_Vertical* | 0,5 x 0,2 x 2 | metal, neon (emissive) | Zuza | [pdf](19_Neon_Vertical.pdf) |
| 20 | Neon_Horizontal | 2 x 0,2 x 0,5 | metal, neon (emissive) | Zuza | [pdf](20_Neon_Horizontal.pdf) |
| 21 | AC_Unit | 0,5 x 0,5 x 0,5 | blacha, kratka | Zuza | [pdf](21_AC_Unit.pdf) |
| 22 | Cables_Pipes | 2 x 0,2 x 3 | guma, metal | Zuza | [pdf](22_Cables_Pipes.pdf) |
| 23 | Vending_Machine* | 1 x 0,5 x 2 | metal, plastik, emissive | Zuza | [pdf](23_Vending_Machine.pdf) |
| 24 | Props_Barrels | 0,5 x 0,5 x 1 | metal, plastik, rdza | Maria | [pdf](24_Props_Barrels.pdf) |

Podsumowanie: Dawid 01 do 06 · Maja 08 do 12 + 17 · Maria 07, 13 do 16, 24 · Zuza 18 do 23. Pełny przydział w [przydzial_modulow.txt](przydzial_modulow.txt).

## Brakujące referencje

- 15 Stairs_Metal: zewnętrzne schody metalowe (stopnie z kratki, poręcz). Dozbiera Maria.
- 09 Foundation_Plinth: cokół / fundament budynku z bliska. Dozbiera Maja.

## Co robi każda osoba

1. Blockout swoich 6 modułów w Blenderze na siatce 0,5 m, obrys zgodny z tabelą.
2. Screenshot każdego modułu.
3. Otwórz `NN_<Moduł>.drawio` w app.diagrams.net, wklej screenshot w ramkę „Screenshot blockoutu”, zapisz `.drawio`.
4. Eksport w tym samym folderze: *File > Export as > PDF* (nadpisz `NN_<Moduł>.pdf`, żeby podgląd na GitHubie był aktualny) i *File > Export as > PNG* jako `NN_<Moduł>.png`.
