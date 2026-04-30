Module 3: LLM & RAG Integrity (LR-M 1.0) / 3. modul: LLM és RAG Integritás

3.1 PII & Sensitive Data Filter / PII és érzékeny adat szűrő
• EN: Real-time scanning for Personally Identifiable Information (PII) to prevent data exfiltration to external or unauthorized logs.
• HU: Személyes adatok (PII) valós idejű szűrése az adatszivárgás megelőzésére a külső vagy nem jogosult naplófájlok irányába.
• Trigger: Regex + NER (Named Entity Recognition) check.

3.2 Semantic Consistency (RAG Guard) / Szemantikai konzisztencia
• EN: Validates the logical distance between the user query and the retrieved context from the vector database.
• HU: Validálja a logikai távolságot a felhasználói kérdés és a vektor-adatbázisból lehívott kontextus között.
• Anomaly Detection: If Cosine_Similarity < 0.7 THEN Raise Anomaly (Context Mismatch).

3.3 Prompt Injection Defense / Prompt Injection védelem
• EN: Detects adversarial patterns designed to bypass system instructions (e.g., "Ignore previous instructions").
• HU: Detektálja az ellenséges mintázatokat, amelyek a rendszerutasítások megkerülésére irányulnak (pl. „Hagyd figyelmen kívül a korábbi utasításokat”).
