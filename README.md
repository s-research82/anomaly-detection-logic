# anomaly-detection-logic
Logikai és strukturális integritás-ellenőrző modell komplex rendszerekhez.
# Anomália-detekciós Modell (AD-M 1.0)

## Absztrakt
A modell célja a rejtett rendszerszintű kockázatok (hibák, csalások, logikai ellentmondások) azonosítása az input adatok és a felelősségi körök aszimmetriája alapján.

## Logikai Architektúra (Algoritmus)
A rendszer az alábbi feltételrendszert vizsgálja minden csomópontnál:

1. **Integritás-ellenőrzés (IC):**
   - Ha `Döntési Jogkör < Büntetőjogi Felelősség`, akkor `Rendszerhiba = TRUE`.
   - Magyarázat: A felelősség delegálása kontroll nélkül minden esetben anomáliát jelez.

2. **Átláthatósági Együttható (TC):**
   - Ha `Input Információ < Várt Kimenet`, akkor `Kockázati Szint = MAGAS`.
   - Magyarázat: A hiányos adatszolgáltatás mellett elvárt eredmények predikciós hibát vagy manipulációt rejtenek.

3. **Végrehajtási Sebesség Teszt (ET):**
   - Ha a szereplő `Válaszidő > Küszöbérték` ÉS `Zajszint = MAGAS`, akkor `Megbízhatóság = 0`.

## Alkalmazási Területek
- Szervezeti átvilágítás (Due Diligence).
- Szerződéses logikai hibák feltárása.
- Hálózati integritás vizsgálata.

---
*Módszertan: Deduktív elemzés és sztochasztikus kockázatbecslés.*
