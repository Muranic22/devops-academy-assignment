# Stage 1: Build (tu nainstalujeme dependencies, aby sme setrili miesto)
FROM python:3.11-slim as builder
WORKDIR /app
COPY requirements.txt .
RUN pip install --user -r requirements.txt

# Stage 2: Final (tu len skopirujeme co treba, aby bol image maly a bezpecny)
FROM python:3.11-slim
WORKDIR /app
# Skopirujeme nainstalovane kniznice z builder stage
COPY --from=builder /root/.local /root/.local
COPY . .

# Nastavenie cesty k nainstalovanym balickom
ENV PATH=/root/.local/bin:$PATH

EXPOSE 5000
CMD ["python", "app.py"]
