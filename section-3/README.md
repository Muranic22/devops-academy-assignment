# Section 3: Task A - Production went down (Incident Response)

## Postup riesenia incidentu

1. Verifikacia a Triage
- Potvrdenie vypadku (monitoring, status page, manualny test).
- Zistenie rozsahu (je to globalne alebo len konkretna lokalita/funkcia?).

2. Stabilizacia (Quick Fix)
- Ak bol tesne pred vypadkom nasadeny novy kod, okamzity ROLLBACK na poslednu stabilnu verziu.
- Restartovanie sluzieb/kontajnerov, ak ide o zahltenie pamate (OOM).

3. Investigacia (Root Cause Analysis)
- Kontrola logov (ELK, CloudWatch): hladanie chyb 5xx alebo fatal errorov.
- Kontrola infrastrukturnych metrik: CPU spike, plny disk, zahltenie DB spojeni.
- Kontrola externych zavisloasti: DNS, SSL certifikaty, vypadok cloud providera (AWS/Azure).

4. Trvala oprava a Post-mortem
- Nasadenie finalnej opravy po najdeni chyby.
- Spisanie reportu: Co sa stalo, preco sa to stalo a ako upravit monitoring/kod, aby sa to neopakovalo.
