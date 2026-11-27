# Modules plan

Plan kitu modułowego **Cyberpunk Sci-Fi Slum Habitation Block**: siatka, lista 24 modułów, przydział i reference board dla każdego modułu.

Pliki:

- [`Modules_plan.drawio`](Modules_plan.drawio): jeden duży board ze wszystkimi 24 modułami, w 4 kolumnach (jedna kolumna na osobę). Otwierasz w [app.diagrams.net](https://app.diagrams.net) przez *File > Open from > Device*.
- [`Modules_plan.pdf`](Modules_plan.pdf): podgląd, który GitHub pokazuje od razu po kliknięciu (strona = moduł, w kolejności numerów).

Przy każdym module: wymiary, materiały, osoba, opis, zdjęcia referencyjne z czerwonymi ramkami (numer ramki = pozycja w legendzie pod zdjęciem) i pusta ramka na screenshot blockoutu.

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

| # | Moduł | Wymiary (m) | Materiały | Osoba | Strona PDF |
|---|---|---|---|---|---|
| 01 | Wall_Solid | 2 x 0,2 x 3 | beton z plamami, tynk | Dawid | 1 |
| 02 | Wall_Half | 1 x 0,2 x 3 | beton z plamami, tynk | Dawid | 2 |
| 03 | Wall_Window* | 2 x 0,2 x 3, okno 1 x 1,5 | beton, rama metalowa, szkło | Dawid | 3 |
| 04 | Wall_Door* | 2 x 0,2 x 3, drzwi 1 x 2,2 | beton, blacha drzwi, naklejki | Dawid | 4 |
| 05 | Wall_Shopfront* | 2 x 0,5 x 3 | metal, szkło, roleta | Dawid | 5 |
| 06 | Corner_Pillar | 0,5 x 0,5 x 3 | beton, rury | Dawid | 6 |
| 07 | Floor_Slab | 2 x 2 x 0,2 | beton | Maria | 7 |
| 08 | Floor_Ledge | 2 x 0,5 x 0,2 | beton z odpryskami | Maja | 8 |
| 09 | Foundation_Plinth | 2 x 0,5 x 0,5 | beton, brud | Maja | 9 |
| 10 | Roof_Parapet | 2 x 0,2 x 1 | beton, blacha | Maja | 10 |
| 11 | Roof_Corrugated* | 2 x 2, spadek 0,5 | blacha falista, rdza | Maja | 11 |
| 12 | Awning* | 2 x 1 | blacha falista, wsporniki | Maja | 12 |
| 13 | Balcony* | 2 x 1 x 1 | beton, barierka stalowa | Maria | 13 |
| 14 | Railing | 2 x 0,1 x 1 | stal, rdza | Maria | 14 |
| 15 | Stairs_Metal* | 1 x 3 x 3 | stal, kratka | Maria | 15 |
| 16 | Addon_Box* | 2 x 2 x 3 | blacha, deski, panele | Maria | 16 |
| 17 | Rooftop_Equipment* | 1 x 1 x 1,5 | blacha, rdza | Maja | 17 |
| 18 | Utility_Pole* | 0,5 x 0,5 x 8 | beton, transformator, kable | Zuza | 18 |
| 19 | Neon_Vertical* | 0,5 x 0,2 x 2 | metal, neon (emissive) | Zuza | 19 |
| 20 | Neon_Horizontal | 2 x 0,2 x 0,5 | metal, neon (emissive) | Zuza | 20 |
| 21 | AC_Unit | 0,5 x 0,5 x 0,5 | blacha, kratka | Zuza | 21 |
| 22 | Cables_Pipes | 2 x 0,2 x 3 | guma, metal | Zuza | 22 |
| 23 | Vending_Machine* | 1 x 0,5 x 2 | metal, plastik, emissive | Zuza | 23 |
| 24 | Props_Barrels | 0,5 x 0,5 x 1 | metal, plastik, rdza | Maria | 24 |

Podsumowanie: Dawid 01 do 06 · Maja 08 do 12 + 17 · Maria 07, 13 do 16, 24 · Zuza 18 do 23. Pełny przydział w [przydzial_modulow.txt](przydzial_modulow.txt).

## Brakujące referencje

- 15 Stairs_Metal: zewnętrzne schody metalowe (stopnie z kratki, poręcz). Dozbiera Maria.
- 09 Foundation_Plinth: cokół / fundament budynku z bliska. Dozbiera Maja.

## Co robi każda osoba

1. Blockout swoich 6 modułów w Blenderze na siatce 0,5 m, obrys zgodny z tabelą.
2. Screenshot każdego modułu.
3. Pobierz najnowszy `Modules_plan.drawio` (pull), otwórz w app.diagrams.net, wklej screenshoty w ramki „Screenshot blockoutu” w swojej kolumnie, zapisz i od razu wypchnij.
4. Plik jest jeden dla wszystkich i git nie połączy dwóch wersji `.drawio`, więc edytujemy **po kolei**: zanim zaczniesz, napisz na grupie, że masz plik; po pushu daj znać, że jest wolny.
5. Na koniec (jedna osoba): *File > Export as > PDF* i nadpisz `Modules_plan.pdf`, żeby podgląd na GitHubie miał screenshoty.
