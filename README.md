# CLRS Algoritmus Labor

> Interaktív, vizuális és matematikailag precíz algoritmustanuló laboratórium Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest és Clifford Stein ***Algoritmusok*** (*Introduction to Algorithms*) című alapműve alapján.

![Verzió](https://img.shields.io/badge/verzió-v0.4.0-b45309)
![Állapot](https://img.shields.io/badge/I._Rész_(1–4._fejezet)-Kész-047857)
![Architektúra](https://img.shields.io/badge/Zero--Dependency-HTML5%20%2F%20ES6%2B%20%2F%20SVG-1e3a8a)
![Licenc](https://img.shields.io/badge/licenc-MIT-slate)

---

## A projekt célja

A **CLRS Algoritmus Labor** nem egy statikus összefoglaló vagy előre rögzített animációgyűjtemény, hanem egy **determinisztikus végrehajtási motorra épülő interaktív digitális tankönyv és laboratórium**. A tananyag szigorúan a könyv eredeti fejezetsorrendjét és jelöléseit (1-alapú tömbindexelés $A[1..n]$, CLRS pszeudokód-konvenciók) követi az alapoktól indulva.

Minden tanulási egység egységes, **9 lépcsős pedagógiai felépítést (A–I)** követ:
1. **A. Bevezetés és motiváció** — A probléma kontextusa és gyakorlati jelentősége.
2. **B. Szükséges előismeretek** — Jelölések, fogalmak és matematikai alapok.
3. **C. Intuitív magyarázat** — Hétköznapi analógiák a formális leírás előtt.
4. **D. Interaktív algoritmus-laboratórium** — Élő, léptethető végrehajtás saját bemenetekkel.
5. **E. Az algoritmus pontos leírása** — CLRS pszeudokód és elő-/utófeltételek.
6. **F. Matematikai háttér és levezetés** — Ciklusinvariánsok, rekurziók és bizonyítások.
7. **G. Hatékonyság és komplexitás** — Legjobb, átlagos és legrosszabb eset elemzése.
8. **H. Interaktív gyakorlás** — Ellenőrzött feladatok azonnali, magyarázó visszajelzéssel.
9. **I. Összefoglalás** — Kulcsfogalmak és átvezetés a következő fejezetre.

---

## Jelenlegi tartalom (`v0.4.0` — I. Rész: Alapok lezárva)

A `v0.4.0` mérföldkő a könyv teljes **I. Részét (1–4. fejezet)** dolgozza fel teljes interaktivitással:

* **Nyitóoldal (Könyvborító és Tanulási Térkép):**
  * Élő interaktív időkomplexitás-összehasonlító widget ($n \lg n$, $n^2$, $n^3$, $2^n$).
  * A könyv teljes **I–VIII. Részének (35 fejezet)** áttekinthető tanulási útvonala.
  * Helyi haladásmentés (`localStorage`) és világos / sötét téma váltó.
* **1.1. fejezet — Algoritmusok:**
  * A rendezési probléma formális definíciója (bemeneti példány vs. permutációs kimenet).
  * Interaktív permutáció- és rendezettség-ellenőrző, valamint $n!$ vs. $n^2$ vs. $n \lg n$ növekedési grafikon.
* **1.2. fejezet — Az algoritmusok mint technológia:**
  * A CLRS klasszikus *Hardver vs. Algoritmus* versenyszimulátora ($10^{10}$ műv/mp-es gép $c_1 n^2$-tel vs. $10^7$ műv/mp-es gép $c_2 n \lg n$-nel) állítható paraméterekkel és log-log diagrammal.
* **2.1. fejezet — Beszúró rendezés (`INSERTION-SORT`):**
  * Determinisztikus lépésenkénti debugger saját tömbbevitellel, szinkronizált 1-alapú pszeudokóddal, élő változófigyelővel ($j, i, \text{key}$) és valós idejű **ciklusinvariáns-ellenőrzővel** (Inicializálás, Fenntartás, Befejezés).
* **2.2. fejezet — Algoritmusok elemzése:**
  * A RAM-modell bemutatása és az `INSERTION-SORT` soronkénti ($c_1 \dots c_8$) utasításköltség-táblázata legjobb ($\Theta(n)$), átlagos és legrosszabb ($\Theta(n^2)$) esetre.
* **2.3. fejezet — Algoritmusok tervezése (Oszd meg és uralkodj):**
  * **1. Labor (`MERGE`):** Lépésenkénti összefésülés az $L[n_1+1]=\infty$ és $R[n_2+1]=\infty$ őrszem (sentinel) elemekkel.
  * **2. Labor (`MERGE-SORT`):** Élő SVG rekurziós fa ($\lg n + 1$ szint) saját bemenettel és szintenkénti költségösszegzéssel ($\Theta(n \lg n)$).
* **3. fejezet — Függvények növekedése ($O, \Omega, \Theta, o, \omega$):**
  * Interaktív *Aszimptotikus Szendvics-labor* állítható $c_1, c_2$ konstansokkal és $n_0$ küszöbértékkel, határérték-teszttel és növekedési hierarchiával.
* **4. fejezet — Oszd meg és uralkodj (Rekurziók és Mester-tétel):**
  * Interaktív **Mester-tétel és Rekurziós Fa Laboratórium** $T(n) = aT(n/b) + f(n)$ egyenletekhez mindhárom eset és a regularitási feltétel vizuális ellenőrzésével, valamint a helyettesítéses módszer levezetésével.

---

## Technológiai felépítés és futtatás

Az alkalmazás szándékosan **külső függőségektől és build-folyamattól mentes** (`Zero-Dependency` egyfájlos architektúra: szabványos HTML5 + CSS3 + ES6+ JavaScript + natív SVG), így bármilyen böngészőben azonnal, offline is futtatható.

### Helyi futtatás
```bash
git clone https://github.com/banyaattila-crypto/algoritmusok-labor.git
cd algoritmusok-labor
# Nyisd meg az index.html fájlt bármely modern böngészőben
```

### Publikálás GitHub Pages-en
1. A repository **Settings → Pages** menüpontjában állítsd a *Source* értéket **Deploy from a branch** opcióra (`main` branch, `/ (root)` mappa).
2. Mentés után az alkalmazás elérhetővé válik a `https://banyaattila-crypto.github.io/algoritmusok-labor/` címen.

---

## Tervezett ütemterv (Roadmap)

- [x] **v0.1.0 – v0.4.0:** I. Rész — Alapok (1–4. fejezet: Bevezetés, Insertion Sort, Merge Sort, Aszimptotikus jelölések, Rekurziók és Mester-tétel)
- [ ] **v0.5.0:** II. Rész — Kupacrendezés (`HEAPSORT`, `MAX-HEAPIFY`, `BUILD-MAX-HEAP`, prioritási sorok — 6. fejezet)
- [ ] **v0.6.0:** II. Rész — Gyorsrendezés (`QUICKSORT`, `PARTITION`, véletlenített változat — 7. fejezet) és lineáris idejű rendezések (8. fejezet)
- [ ] **v0.7.0:** III. Rész — Elemi adatszerkezetek, Hash-táblák, Bináris keresőfák és Piros-fekete fák (10–13. fejezet)
- [ ] **v0.8.0:** IV. Rész — Dinamikus programozás és Mohó algoritmusok (15–16. fejezet)
- [ ] **v0.9.0:** VI. Rész — Gráfalgoritmusok (BFS, DFS, Kruskal, Prim, Dijkstra, Bellman-Ford — 22–24. fejezet)

---

## Bibliográfiai hivatkozás

* Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C.: *Introduction to Algorithms* (MIT Press). Magyar kiadás: *Algoritmusok* / *Új algoritmusok* (Műszaki Könyvkiadó).
* Az alkalmazásban szereplő magyarázatok, interaktív szimulációk és vizualizációk önálló pedagógiai feldolgozások.