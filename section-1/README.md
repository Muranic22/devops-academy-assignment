# Section 1: Task B - Dockerize Python App

## Popis
Dockerizacia Flask aplikacie pomocou multi-stage buildu pre minimalizaciu velkosti image.

## Subory
- app.py: Zdrojovy kod aplikacie
- requirements.txt: Python dependencies (Flask)
- Dockerfile: Multi-stage build (builder + runner stage)
- docker-compose.yml: Definicia sluzby a mapovanie portov

## Spustenie
```bash
docker-compose up --build
