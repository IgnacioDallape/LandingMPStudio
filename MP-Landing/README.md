# MP STUDIO — Landing EPI Mendoza

Landing page de **MP STUDIO**, centro de **Electrólisis Percutánea Intratisular (EPI)**
y fisioterapia invasiva en Mendoza. Optimizada para SEO (local + nacional) y orientada
a conversión por **WhatsApp**.

Es un sitio **estático** (un solo `index.html`, sin build), así que se despliega en
cualquier hosting en segundos.

## Archivos
- `index.html` — la landing completa (HTML + CSS + JS inline, schema SEO incluido).
- `favicon.svg` — ícono con el logo MP.
- `ESTRATEGIA-SEO.md` — keywords, arquitectura y specs de las páginas satélite.

## Ver en local
Abrí `index.html` en el navegador, o serví la carpeta:
```bash
npx serve .
```

## ⚠️ Antes de publicar (completar)
1. **WhatsApp:** ya cargado (`+54 9 261 213 0504`). Si cambia, editá
   `var WHATSAPP = "5492612130504";` al final de `index.html`.
2. **Dominio:** reemplazá `https://www.mpstudio.com.ar/` en `<link canonical>`,
   `og:url` y el schema.
3. **Teléfono / dirección** en el bloque JSON-LD `MedicalBusiness`.
4. **`og-image.jpg`** (1200×630) en la raíz, para compartir el link en redes.

## Deploy
- **Vercel / Netlify:** importá el repo (framework: *Other / static*) → deploy.
- **GitHub Pages:** Settings → Pages → Branch `main` / root.

## Subir a un repo nuevo
```bash
git remote add origin https://github.com/TU-USUARIO/mp-studio-landing.git
git push -u origin main
```
(El repo ya está inicializado con un commit inicial.)
