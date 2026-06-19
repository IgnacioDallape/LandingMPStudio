# MP STUDIO — Landing EPI Mendoza

Landing page de **MP STUDIO**, centro de **Electrólisis Percutánea Intratisular (EPI)**
y fisioterapia invasiva en Mendoza. Optimizada para SEO (local + nacional) y orientada
a conversión por **WhatsApp**.

Es un sitio **estático** (un solo `index.html`, sin build), así que se despliega en
cualquier hosting en segundos.

## Archivos
- `index.html` — la landing completa (HTML + CSS + JS inline, schema SEO incluido).
- `favicon.svg` — ícono con el logo MP.
- `og-image.png` — imagen 1200×630 para previews al compartir (generada desde `og-image.svg`).
- `og-image.svg` — fuente editable de la OG image.
- `robots.txt` — permite crawl + apunta al sitemap.
- `sitemap.xml` — URLs del sitio (home + satélites comentadas hasta que existan).
- `ESTRATEGIA-SEO.md` — keywords, arquitectura y specs de las páginas satélite.

## Ver en local
Abrí `index.html` en el navegador, o serví la carpeta:
```bash
npx serve .
```

## Estado SEO

**Ya resuelto:**
- WhatsApp `+54 9 261 213 0504` cargado (editá `var WHATSAPP` al final de `index.html` si cambia).
- Dominio `https://landing-mp-studio.vercel.app/` en canonical, OG, robots, sitemap y schema.
- Dirección (Gral. Paz 8222, Luján de Cuyo, Mendoza) y teléfono en el schema `MedicalBusiness` + footer (NAP).
- `og-image.png` (1200×630) generada.
- Schema del profesional (`Person` Marcos Porretta) + `robots.txt` + `sitemap.xml`.
- Fuentes cargadas async (mejor LCP/Core Web Vitals).

**Pendiente (necesita datos reales):**
1. **Nº de matrícula** de Marcos Porretta → agregar `hasCredential`/`identifier` al `Person` y mostrarlo en la sección "Profesional".
2. **Confirmar el título exacto** (ej. "Lic. en Kinesiología y Fisioterapia") en el `jobTitle` del schema y la sección.
3. **Coordenadas exactas** del pin de Google Maps → reemplazar `geo.position`/`ICBM` y `GeoCoordinates` (hoy es el centro aprox. de Luján de Cuyo; ver `TODO` en el `<head>`).
4. **Redes sociales** (Instagram/Facebook) → agregar `"sameAs": [...]` al schema `MedicalBusiness`.
5. **Off-code:** Google Business Profile (NAP idéntico) + Google Search Console (subir el sitemap).

## Deploy
- **Vercel / Netlify:** importá el repo (framework: *Other / static*) → deploy.
- **GitHub Pages:** Settings → Pages → Branch `main` / root.

## Subir a un repo nuevo
```bash
git remote add origin https://github.com/TU-USUARIO/mp-studio-landing.git
git push -u origin main
```
(El repo ya está inicializado con un commit inicial.)
