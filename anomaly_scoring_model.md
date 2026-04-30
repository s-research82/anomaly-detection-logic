Module 4: Anomaly Scoring Model (AS-M 1.0) / 4. modul: Anomália-pontozó modell

4.1 Weighted Risk Formula / Súlyozott kockázati képlet
Total_Risk_Score (TRS) = (w1 * IC) + (w2 * TC_Penalty) + (w3 * LR_Anomaly)
Weights / Súlyok:
• w1 (Integrity): 0.25
• w2 (Transparency): 0.15
• w3 (AI/RAG Security): 0.60 (Critical priority / Kritikus prioritás)

4.2 Risk Categories / Kockázati kategóriák
• 0.0 - 0.2: Low Risk / Alacsony kockázat (Green / Zöld)
• 0.2 - 0.5: Medium Risk / Közepes kockázat - Investigation required / Kivizsgálás szükséges (Yellow / Sárga)
• 0.5 - 1.0: High Risk / Magas kockázat - Immediate Block / Azonnali blokkolás (Red / Piros)
4.3 Logic Gate: The "Zero Trust" Override

• EN: If any module returns a "CRITICAL" flag (e.g., direct PII leakage attempt), the TRS is automatically set to 1.0, regardless of other factors.
• HU: Ha bármelyik modul "KRITIKUS" jelzést ad (pl. közvetlen PII szivárogtatási kísérlet), a TRS értéke automatikusan 1.0 lesz, egyéb tényezőktől függetlenül.
