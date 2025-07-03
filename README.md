# Twenty CRM — Self-Hosting with Coolify

This repository provides a **clean, production-ready `docker-compose.yml`** to deploy [Twenty CRM](https://github.com/FabianHertwig/twenty) on your own VPS using [Coolify](https://coolify.io).

---

## ✅ Overview

- Uses Docker Compose with correct `volumes` syntax — no more “Undefined array key” errors.
- Works with wildcard DNS and Coolify’s Traefik proxy for automatic SSL.
- Tested on a VPS with a real domain.

---

## ⚡ Quick Start

1. **Clone this repository**

2. Point your wildcard DNS `*.yourdomain.com` to your VPS IP.

3. In Coolify, create a **Docker Compose Empty** app.  
   - Paste the `docker-compose.yml` from this repo.

4. Add your required environment variables, for example:
   ```env
   PG_DATABASE_USER=postgres
   PG_DATABASE_PASSWORD=postgres
   REDIS_URL=redis://redis:6379
   STORAGE_TYPE=local
   APP_SECRET=your_super_secret_key
   SERVER_URL=https://crm.yourdomain.com
