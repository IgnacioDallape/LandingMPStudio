# MP STUDIO — Estrategia SEO & páginas satélite

Centro de **Electrólisis Percutánea Intratisular (EPI)** y fisioterapia invasiva en Mendoza.
Objetivo: posicionar fuerte en Google para EPI/fisioterapia invasiva (Mendoza + zonas + nacional) y convertir a **consulta por WhatsApp**.

---

## 1. SEO on-page de la landing principal (ya implementado en `index.html`)

| Elemento | Valor |
|---|---|
| **Title** | `Electrólisis Percutánea Intratisular en Mendoza \| EPI \| MP STUDIO` |
| **Meta description** | `Electrólisis Percutánea Intratisular (EPI) en Mendoza: fisioterapia invasiva para tendinopatías y lesiones deportivas, con evaluación ecográfica, neuromodulación y punción seca. Atención en Maipú, Luján de Cuyo, Godoy Cruz y todo el Gran Mendoza. Consultá por WhatsApp.` |
| **H1 (único)** | Electrólisis Percutánea Intratisular en Mendoza |
| **H2** | Dolor que no mejora… · Electrólisis Percutánea Intratisular (EPI) en Mendoza · Lesiones que se pueden tratar · Servicios de MP STUDIO · Zonas de atención en Mendoza · Recuperación real… · Preguntas frecuentes · CTA final |
| **H3** | ¿Qué es la EPI? · ¿Para qué sirve? · ¿Por qué es diferente? · ¿Cuándo consultar? · cada servicio · cada FAQ |
| **Schema** | `MedicalBusiness` (con `areaServed` por zona + `hasOfferCatalog`) y `FAQPage` (10 preguntas) |
| **Extra** | Open Graph, Twitter Card, canonical, geo-tags (AR-M), `lang="es-AR"`, `robots index,follow` |

**Pendiente de cargar antes de publicar** (marcado en el código con comentarios):
1. `WHATSAPP` real en el `<script>` (hoy es placeholder `5492610000000`).
2. `telephone` y, si hay local, `address.streetAddress` en el schema `MedicalBusiness`.
3. Dominio real en `canonical` / `og:url` (hoy `https://www.mpstudio.com.ar/`).
4. Imagen `og-image.jpg` (1200×630) en la raíz para que se vea bien al compartir.

---

## 2. Mapa de palabras clave

**Principales (landing home):**
Electrólisis Percutánea Intratisular · Electrólisis Percutánea Intratisular en Mendoza · EPI Mendoza · tratamiento EPI Mendoza · fisioterapia invasiva Mendoza · rehabilitación deportiva Mendoza.

**Secundarias:** evaluación ecográfica Mendoza · neuromodulación Mendoza · punción seca Mendoza · readaptación deportiva Mendoza · tendinopatías · dolor crónico.

**Locales (páginas satélite por zona):** EPI Maipú · EPI Luján de Cuyo · fisioterapia invasiva Godoy Cruz · rehabilitación deportiva Ciudad de Mendoza · punción seca Guaymallén · neuromodulación Las Heras · evaluación ecográfica San Martín · fisioterapia avanzada Palmira.

**Nacionales (contenido / blog):** Electrólisis Percutánea Intratisular en Argentina · tratamiento EPI Argentina · fisioterapia invasiva en Argentina · rehabilitación deportiva avanzada Argentina.

---

## 3. Arquitectura del sitio

```
/                         → Landing principal (EPI Mendoza)            [keyword: EPI Mendoza]
/epi-mendoza/             → (opcional) hub EPI ampliado
ZONAS (SEO local):
/epi-maipu/               → Electrólisis Percutánea Intratisular en Maipú
/epi-lujan-de-cuyo/       → EPI en Luján de Cuyo
/epi-godoy-cruz/          → Fisioterapia invasiva / EPI en Godoy Cruz
/epi-ciudad-de-mendoza/   → EPI en Ciudad de Mendoza
SERVICIOS (SEO temático):
/fisioterapia-invasiva-mendoza/
/puncion-seca-mendoza/
/neuromodulacion-mendoza/
/evaluacion-ecografica-mendoza/
/readaptacion-deportiva-mendoza/
```

**Reglas de oro para no canibalizar:**
- Cada satélite tiene **un H1 único** con su keyword exacta.
- Contenido **diferente** (no copiar/pegar la home): párrafos propios sobre la zona/servicio.
- Cada satélite **enlaza a la home** (texto ancla “Electrólisis Percutánea Intratisular en Mendoza”) y la home enlaza a los satélites (footer/sección zonas).
- Misma plantilla visual (reusar `index.html` como base), distinto copy + meta + schema.

---

## 4. Páginas satélite (specs SEO)

> Plantilla común: Hero (H1 + sub + CTA WhatsApp) → ¿Qué es? → Beneficios/lesiones → Por qué MP STUDIO → mini-FAQ (3-4, con `FAQPage`) → CTA. Schema `MedicalBusiness` con `areaServed` = la zona. Internal link a `/`.

### 4.1 `/epi-maipu/` — Electrólisis Percutánea Intratisular en Maipú
- **Intención:** local, transaccional (paciente de Maipú buscando EPI cerca).
- **Title:** `Electrólisis Percutánea Intratisular en Maipú | EPI | MP STUDIO`
- **Meta:** `¿Buscás Electrólisis Percutánea Intratisular (EPI) en Maipú, Mendoza? En MP STUDIO tratamos tendinopatías y lesiones deportivas con fisioterapia invasiva ecoguiada. Consultá por WhatsApp.`
- **H1:** Electrólisis Percutánea Intratisular en Maipú
- **H2:** ¿Qué es la EPI? · Lesiones que tratamos en Maipú · Por qué elegir MP STUDIO · Preguntas frecuentes · Pedí tu turno
- **Keywords:** EPI Maipú, electrólisis percutánea Maipú, fisioterapia invasiva Maipú, tendinitis Maipú.

### 4.2 `/epi-lujan-de-cuyo/` — EPI en Luján de Cuyo
- **Title:** `EPI en Luján de Cuyo | Electrólisis Percutánea Intratisular | MP STUDIO`
- **Meta:** `Electrólisis Percutánea Intratisular (EPI) para pacientes de Luján de Cuyo. Fisioterapia invasiva ecoguiada para tendinopatías y lesiones deportivas en MP STUDIO, Mendoza.`
- **H1:** Electrólisis Percutánea Intratisular en Luján de Cuyo
- **Keywords:** EPI Luján de Cuyo, fisioterapia invasiva Luján de Cuyo, rehabilitación deportiva Luján de Cuyo.

### 4.3 `/epi-godoy-cruz/` — Fisioterapia invasiva / EPI en Godoy Cruz
- **Title:** `Fisioterapia Invasiva y EPI en Godoy Cruz | MP STUDIO`
- **Meta:** `Fisioterapia invasiva y Electrólisis Percutánea Intratisular (EPI) para pacientes de Godoy Cruz. Tratamiento de tendinopatías y lesiones deportivas con evaluación ecográfica.`
- **H1:** Fisioterapia invasiva y EPI en Godoy Cruz
- **Keywords:** fisioterapia invasiva Godoy Cruz, EPI Godoy Cruz, punción seca Godoy Cruz.

### 4.4 `/epi-ciudad-de-mendoza/` — EPI en Ciudad de Mendoza
- **Title:** `EPI en Ciudad de Mendoza | Electrólisis Percutánea Intratisular | MP STUDIO`
- **Meta:** `Electrólisis Percutánea Intratisular (EPI) en Ciudad de Mendoza. Rehabilitación deportiva avanzada y fisioterapia invasiva ecoguiada en MP STUDIO.`
- **H1:** Electrólisis Percutánea Intratisular en Ciudad de Mendoza
- **Keywords:** EPI Ciudad de Mendoza, rehabilitación deportiva Ciudad de Mendoza.

### 4.5 `/fisioterapia-invasiva-mendoza/` — Fisioterapia invasiva en Mendoza
- **Intención:** informacional + transaccional (categoría amplia).
- **Title:** `Fisioterapia Invasiva en Mendoza | EPI y Punción Seca | MP STUDIO`
- **Meta:** `Fisioterapia invasiva en Mendoza: Electrólisis Percutánea Intratisular (EPI), punción seca y neuromodulación guiadas por ecografía para lesiones tendinosas y deportivas.`
- **H1:** Fisioterapia invasiva en Mendoza
- **H2:** Qué es la fisioterapia invasiva · Técnicas (EPI, punción seca, neuromodulación) · Lesiones · FAQ.

### 4.6 `/puncion-seca-mendoza/` — Punción seca en Mendoza
- **Title:** `Punción Seca en Mendoza | Puntos Gatillo y Contracturas | MP STUDIO`
- **Meta:** `Punción seca en Mendoza para puntos gatillo, contracturas y dolor muscular. Tratamiento de fisioterapia invasiva en MP STUDIO. Consultá por WhatsApp.`
- **H1:** Punción seca en Mendoza
- **Keywords:** punción seca Mendoza, puntos gatillo Mendoza, contracturas Mendoza, punción seca Guaymallén.

### 4.7 `/neuromodulacion-mendoza/` — Neuromodulación en Mendoza
- **Title:** `Neuromodulación en Mendoza | Manejo del Dolor | MP STUDIO`
- **Meta:** `Neuromodulación en Mendoza para modular el dolor y mejorar la función neuromuscular dentro de un plan de rehabilitación. MP STUDIO, fisioterapia avanzada.`
- **H1:** Neuromodulación en Mendoza
- **Keywords:** neuromodulación Mendoza, neuromodulación Las Heras, dolor crónico Mendoza.

### 4.8 `/evaluacion-ecografica-mendoza/` — Evaluación ecográfica en Mendoza
- **Title:** `Evaluación Ecográfica en Mendoza | Diagnóstico de Lesiones | MP STUDIO`
- **Meta:** `Evaluación ecográfica en Mendoza para valorar tendones, músculos y lesiones en tiempo real. Tratamientos más precisos y personalizados en MP STUDIO.`
- **H1:** Evaluación ecográfica en Mendoza
- **Keywords:** evaluación ecográfica Mendoza, ecografía musculoesquelética Mendoza, evaluación ecográfica San Martín.

### 4.9 `/readaptacion-deportiva-mendoza/` — Readaptación deportiva en Mendoza
- **Title:** `Readaptación Deportiva en Mendoza | Volver a Entrenar | MP STUDIO`
- **Meta:** `Readaptación deportiva en Mendoza: vuelta progresiva y segura al deporte tras una lesión. Fortalecimiento, control motor y prevención de recaídas en MP STUDIO.`
- **H1:** Readaptación deportiva en Mendoza
- **Keywords:** readaptación deportiva Mendoza, rehabilitación deportiva avanzada Argentina, volver a entrenar lesión.

---

## 5. SEO técnico (checklist de publicación)

- [ ] **Dominio + HTTPS** (ej. mpstudio.com.ar). Deploy en Vercel/Netlify (estático = rapidísimo, buen Core Web Vitals).
- [ ] **`robots.txt`** permitiendo todo + línea `Sitemap:`.
- [ ] **`sitemap.xml`** con la home + todas las satélite.
- [ ] **Google Business Profile (GBP)** “MP STUDIO” categoría Fisioterapeuta/Centro de rehabilitación, zona Mendoza → clave para el “local pack” del mapa. Coherencia **NAP** (Nombre, Dirección, Teléfono) entre GBP, web y schema.
- [ ] **Google Search Console** + enviar sitemap.
- [ ] **Reseñas Google** (sumar `aggregateRating` al schema cuando haya reseñas reales — no inventar).
- [ ] **`og-image.jpg`** 1200×630 con logo + “EPI en Mendoza”.
- [ ] **Velocidad/CWV:** la landing ya es 1 archivo, sin imágenes pesadas; si se agregan fotos, usar formato `webp` + `loading="lazy"`.
- [ ] **Alt text** descriptivo en toda imagen real que se agregue (ej. “Tratamiento de EPI ecoguiada en tendón rotuliano - MP STUDIO Mendoza”).
- [ ] **Contenido fresco:** blog/notas (“EPI vs infiltración”, “Tendinopatía rotuliana: tratamiento”) para keywords informacionales y enlazar a la home/satélite.

## 6. Cumplimiento (importante en salud)
- Evitar promesas absolutas: nada de “cura garantizada” ni “100% efectivo”.
- Usar siempre: “puede ayudar”, “se utiliza en”, “orientado a”, “según evaluación profesional”.
- Aclarar que la web es orientativa y no reemplaza la consulta (ya incluido en el footer y en la tarjeta de beneficios).
