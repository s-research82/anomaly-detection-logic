Module 4: Unified Anomaly Scoring Model (UASM 1.0) / 4. modul: Egységesített Anomália-pontozási Modell

4.1 Concept / Koncepció
The UASM 1.0 aggregates findings from all active modules to produce a single Total Anomaly Score (TAS). / Az UASM 1.0 összesíti az összes aktív modul eredményét, hogy létrehozzon egyetlen Összesített Anomália-pontszámot (TAS).

4.2 Calculation Formula / Számítási képlet
TAS = (w1 * IC) + (w2 * TC) + (w3 * LR)
Where / Ahol:
• w1 (0.2): Integrity Weight / Integritási súly
• w2 (0.3): Transparency Weight / Transzparencia súly
• w3 (0.5): Logic & RAG Weight / Logikai és RAG súly

4.3 Severity Levels / Súlyossági szintek
• TAS < 0.3: Normal Operation. / Normál működés.
• 0.3 <= TAS < 0.6: Suspicious Activity. Automated monitoring increased. / Gyanús tevékenység. Automatizált megfigyelés fokozva.
• 0.6 <= TAS < 0.8: High Risk. Human intervention required. / Magas kockázat. Emberi beavatkozás szükséges.
• TAS >= 0.8: Critical Breach. Immediate system lockdown. / Kritikus behatolás. Azonnali rendszerszintű lezárás.
