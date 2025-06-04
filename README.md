# OpenWebUI Docker Setup

Questa repository contiene un setup di **[Open WebUI](https://github.com/open-webui/open-webui)**, con supporto per **Ollama**.

⚠️ _Questa repo **non contiene il progetto originale di Open WebUI** ma solo il `docker-compose.yaml` configurato e un file `.env.example`._

## Cosa contiene questa repo

- `docker-compose.yaml` già configurato per far partire Open WebUI e Ollama.
- `.env.example` da usare come base per il tuo `.env` personale.

---

## ✅ Prerequisiti

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)
---

## 🚀 Come iniziare

1. **Clona questa repo**

```bash
git clone https://github.com/rosy1a/OpenWebui_D.git
cd OpenWebui_D
```
2. **Copia e modifica il file `.env.example`**
```bash
cp .env.example .env  # poi apri .env e modificalo
```
3. **Avvia i container**
```bash
docker compose up -d
```

4. **🧠 Modelli AI in Ollama**
  Dopo aver avviato i container con `docker compose up -d` il container di Ollama sarà attivo, ma non conterrà alcun **modello preinstallato.**
  Per scaricare un modello (ad esempio LLaMA 3.2), esegui:
```bash
docker exec -it ollama ollama pull llama3.2
```
  Sostituisci llama3 con il nome di qualsiasi altro modello supportato da Ollama che desideri usare. Puoi consultare i modelli disponibili sulla pagina ufficiale di **[Ollama](https://ollama.com/library).**
   
6. **Accedi all'interfaccia**
   
   Apri il tuo browser e digita:
   
   ``` http://localhost:3000``` _(o la porta che hai impostato nel .env)_

## 🧱 Struttura dei servizi

- **ollama**: container che ospita i modelli LLM (es. LLaMA)
- **open-webui**: interfaccia utente web, basata sul progetto [open-webui](https://github.com/open-webui/open-webui)

---

---

### 👥 Partecipanti al progetto

Queste persone hanno collaborato allo sviluppo e alla configurazione del progetto:

- [@albertoarola](https://github.com/albertoarola)
- [@rosy1a](https://github.com/rosy1a)
- [@Camrotez](https://github.com/Camrotez)
- [@Dondo-98](https://github.com/Dondo-98)
- [@Francesco17-tr](https://github.com/Francesco17-tr)




## 📝 Note

- Questo progetto **non modifica il codice originale** di Open WebUI.
- Se vuoi personalizzare o contribuire al progetto principale, usa direttamente la loro repo ufficiale:  
  👉 [https://github.com/open-webui/open-webui](https://github.com/open-webui/open-webui)
- Le immagini Docker utilizzate sono:
  - `ghcr.io/open-webui/open-webui`
  - `ollama/ollama`
