Module 2: Transparency Coefficient (TC) / 2. modul: Transzparencia-együttható

2.1 Definition / Definíció
TC = (Available_Relevant_Data / Required_Total_Data) * 100

2.2 Thresholds / Küszöbértékek
• TC = 100%: High Confidence Analysis. / Magas megbízhatóságú elemzés.
• 75% <= TC < 100%: Conditional Analysis (Limitations must be flagged). / Feltételes elemzés (a korlátokat jelezni kell).
• TC < 75%: Systemic Blind Spot. / Rendszerszintű vakfolt.
• TC < 50%: Critical Failure. Analysis Discarded. / Kritikus hiba. Elemzés elvetve.

2.3 Noise Detection / Zaj-detekció
• If the volume of irrelevant data (Noise) > relevant data, the TC is automatically penalized by a factor of 0.5.
• Ha az irreleváns adatok (Zaj) mennyisége meghaladja a releváns adatokét, a TC értéke automatikusan 0,5-ös szorzóval csökken.
