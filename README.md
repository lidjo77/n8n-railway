# n8n på Railway (från `lidjo77/n8n-railway`)

Detta repo är en färdig setup för att köra n8n (automationsplattform) direkt på [Railway](https://railway.app) med Docker.

---

## 🚀 Steg-för-steg: Deploya n8n via Railway

### 1. Klona detta repo eller koppla det direkt till Railway

Du kan använda Railway-knappen “Deploy from GitHub Repo” och välja:

```
https://github.com/lidjo77/n8n-railway
```

---

### 2. Railway kommer automatiskt upptäcka `Dockerfile`

Gå till **Settings → Build & Deploy → Builder**  
Välj: `Dockerfile` om det inte redan är valt.

---

### 3. Lägg till miljövariabler (Environment Variables)

| Key                     | Value (exempel)                                      |
|------------------------|------------------------------------------------------|
| `N8N_BASIC_AUTH_USER`   | `admin`                                              |
| `N8N_BASIC_AUTH_PASSWORD` | `superhemligt123`                                 |
| `N8N_HOST`              | `0.0.0.0`                                            |
| `N8N_PORT`              | `5678`                                               |
| `N8N_PROTOCOL`          | `https`                                              |
| `WEBHOOK_URL`           | `https://<din-railway-url>.up.railway.app/`         |
| `NODE_ENV`              | `production`                                         |

---

### 4. Starta appen

Railway bygger nu din n8n-instans. När det är klart får du en URL:  
T.ex. `https://n8n-railway-production.up.railway.app`

Gå till sidan och logga in med de uppgifter du satte i miljövariablerna.

---

### 🧠 Tips

- Du kan ändra port, host och lösenord via miljövariabler
- Alla flöden sparas i Railway-containern – om du vill ha permanent lagring, använd en extern databas som PostgreSQL
