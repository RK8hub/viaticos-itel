# Solicitud de viático

Astro estático. `npm install` · `npm run dev` · `npm run build`.

## Despliegue (GitHub Pages + Cloudflare)

1. Subí el proyecto a un repo de GitHub (rama `main`), incluyendo `package-lock.json`.
2. Repo → Settings → Pages → Source: **GitHub Actions**.
3. Cada push a `main` despliega solo (`.github/workflows/deploy.yml`).
4. Dominio propio: en Settings → Pages → Custom domain escribí tu subdominio (ej. `viatico.rk8.dev`).
5. Cloudflare → DNS → agregar registro: `CNAME`, nombre `viatico`, destino `RK8hub.github.io`, proxy **solo DNS** (nube gris) hasta que GitHub emita el certificado.
6. En Settings → Pages activá **Enforce HTTPS**. Después podés prender el proxy (nube naranja) con SSL/TLS en modo **Full**.
