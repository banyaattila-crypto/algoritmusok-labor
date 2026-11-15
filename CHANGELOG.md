# Változásnapló (Changelog)

A projekt a [Semantic Versioning](https://semver.org/) elveit követi.

---

## [v0.4.0] — I. Rész (Alapok) lezárva

### Hozzáadva
- **4. fejezet (Oszd meg és uralkodj — Rekurziók és Mester-tétel):**
  - Interaktív Mester-tétel kalkulátor és élő SVG rekurziós fa generátor $T(n) = aT(n/b) + f(n)$ alakú rekurzív egyenletekhez.
  - A Mester-tétel mindhárom esetének, a kritikus kitevőnek ($\log_b a$), a polinomiális különbségnek ($\varepsilon$) és a regularitási feltételnek ($a f(n/b) \le c f(n)$) valós idejű verifikációja.
  - Előre definiált algoritmus-presetek: *Bináris keresés*, *Merge Sort*, *Strassen-mátrixszorzás* és kiegyensúlyozatlan rekurziók.
  - A helyettesítéses módszer (matematikai indukció) és a rekurziós fa mértani soros összegzésének részletes levezetése.
- **Dokumentáció:**
  - Hozzáadva a `README.md` és a `CHANGELOG.md` fájl a GitHub publikáláshoz.

---

## [v0.3.0] — Aszimptotikus jelölések és függvények növekedése

### Hozzáadva
- **3. fejezet (Függvények növekedése — 3.1 és 3.2):**
  - Interaktív *Aszimptotikus Szendvics-labor* ($O, \Omega, \Theta$) állítható $c_1, c_2$ konstansokkal, $n_0$ küszöbértékkel és élő SVG függvénydiagrammal.
  - Szigorú aszimptotikus jelölések ($o, \omega$) határérték-teszttel ($\lim_{n \to \infty} f(n)/g(n)$) és a CLRS standard növekedési hierarchiájával.

---

## [v0.2.0] — Oszd meg és uralkodj (`MERGE` és `MERGE-SORT`)

### Hozzáadva
- **2.3. fejezet (Algoritmusok tervezése):**
  - Determinisztikus `MERGE(A, p, q, r)` lépésenkénti debugger az $L$ és $R$ segédtömbök végére helyezett $\infty$ őrszem (sentinel) elemekkel és élő ciklusinvariáns-ellenőrzéssel.
  - Interaktív `MERGE-SORT(A, p, r)` szimulátor dinamikusan kirajzolódó SVG rekurziós fával és szintenkénti költségösszegzéssel ($\Theta(n \lg n)$).

---

## [v0.1.0] — Alaparchitektúra, MIT Press arculat és 1.1–2.2. fejezetek

### Hozzáadva
- **Alkalmazás-architektúra és arculat:**
  - Külső függőségektől mentes (`Zero-Dependency`) HTML5/CSS3/ES6+ motor, MIT Press ihletésű tipográfiai dizájn világos és sötét témával.
  - Dedikált nyitóoldal (könyvborító nézet, élő komplexitás-előnézet, I–VIII. részes tanulási térkép) és `localStorage` alapú haladásmentés.
  - Egységes 9 részes (A–I) pedagógiai tanulási keretrendszer.
- **Kidolgozott kezdő egységek:**
  - **1.1. fejezet:** Algoritmusok fogalma, permutáció- és rendezettség-ellenőrző, $n!$ vs. $n^2$ vs. $n \lg n$ diagram.
  - **1.2. fejezet:** Az algoritmusok mint technológia (*Hardver vs. Algoritmus* szimulátor).
  - **2.1. fejezet:** `INSERTION-SORT` determinisztikus debugger 1-alapú pszeudokóddal és élő ciklusinvariáns-ellenőrzővel.
  - **2.2. fejezet:** RAM-modell és az `INSERTION-SORT` soronkénti ($c_1 \dots c_8$) utasításköltség-táblázata.