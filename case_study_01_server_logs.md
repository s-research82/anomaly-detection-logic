Case Study 01: Log-Based Intrusion Detection / Esettanulmány 01: Naplófájl alapú behatolásjelzés

1. Dataset / Adathalmaz
• Source / Forrás: Web server access logs (Nginx). / Web szerver hozzáférési naplók (Nginx).
• Format / Formátum: Standard Combined Log Format. / Standard Kombinált Log Formátum.
• Scenario / Szituáció: Unexpected spike in 401 Unauthorized errors followed by a 200 OK from an unverified IP range. / Váratlan kiugrás a 401 Unauthorized hibaüzenetekben, amit egy 200 OK válasz követ egy nem hitelesített IP-tartományból.

2. Applying AD-M 1.0 Logic / Az AD-M 1.0 logika alkalmazása
Step 1: Integrity Check (IC) / 1. lépés: Integritás-ellenőrzés
• Input / Bemenet: Is the log file continuous? Are there gaps in the timestamp? / Folytonos-e a naplófájl? Vannak-e hézagok az időbélyegekben?
• Result / Eredmény: Timestamps are sequential. Integrity = TRUE. / Az időbélyegek szekvenciálisak. Integritás = IGAZ.

Step 2: Transparency Coefficient (TC) / 2. lépés: Transzparencia-együttható
• Check / Ellenőrzés: Do logs contain User-Agent and Request Payload hash? / Tartalmazzák-e a naplók a User-Agent-et és a kérés adatcsomag (Payload) hash-ét?
• Result / Eredmény: User-Agent is present, but Payload is missing. / A User-Agent jelen van, de a Payload hiányzik.
• TC Calculation / TC számítás: TC = 80%.
• Verdict / Ítélet: Conditional Analysis. The absence of payload data limits the depth of anomaly classification. / Feltételes elemzés. Az adatcsomag-adatok hiánya korlátozza az anomália-osztályozás mélységét.

Step 3: Anomaly Identification (The Logic) / 3. lépés: Anomália-azonosítás
• Pattern / Mintázat: 150 consecutive 401 errors from IP 192.x.x.x within 30 seconds. / 150 egymást követő 401-es hiba a 192.x.x.x IP-címről 30 másodpercen belül.
• Trigger / Aktiváló: If Frequency > Threshold AND Response = 401 THEN Risk = HIGH. / Ha a gyakoriság > küszöbérték ÉS a válasz = 401, AKKOR a kockázat = MAGAS.
• Detection / Detektálás: Bruteforce attempt followed by a successful bypass (200 OK) due to a session hijacking vulnerability. / Bruteforce (nyers erő) támadási kísérlet, amelyet egy sikeres megkerülés (200 OK) követett egy munkamenet-eltérítési (session hijacking) sebezhetőség miatt.

3. Conclusion / Konklúzió
The model successfully flagged the IP before the breach occurred. However, the TC = 80% limitation indicates that without payload analysis, the exact method of the bypass remains an assumption.
A modell sikeresen megjelölte az IP-címet a behatolás előtt. Azonban a TC = 80%-os korlát azt jelzi, hogy adatcsomag-elemzés nélkül a megkerülés pontos módja feltételezés marad.
