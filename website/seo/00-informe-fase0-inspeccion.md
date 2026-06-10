# FASE 0 — Inspección inicial (Lenguaje con Inés)

> **Cómo se ha hecho esta inspección.** No ha sido posible inspeccionar la
> instalación por dentro: la conexión MCP con `lenguajeconines.com` la detecta
> como un sitio **WordPress autoalojado conectado vía Jetpack SIN plan de pago**,
> por lo que **todas** las operaciones de lectura/escritura de contenido,
> ajustes, plugins y tema devuelven el error *"This action requires a paid
> Jetpack plan"*. Además, el sitio responde `403 Forbidden` a peticiones
> externas (firewall/WAF), así que tampoco se puede leer el HTML público.
>
> Esta inspección se ha hecho **a partir de las capturas reales de la web**
> guardadas en `/website/*.png` más el contexto de marca. Lo que está marcado
> con **⚠️ VERIFICAR** es algo que NO he podido confirmar y que debes comprobar
> en tu panel de WordPress antes de actuar.

---

## 0.1 Producción vs. staging (responde antes de aplicar nada)

Tu asesor lo pidió y es lo correcto: **antes de aplicar redirecciones, noindex
masivos o cambios de plantilla, confirma si trabajas sobre producción o sobre
un staging.** Recomendación:

- Si tienes **staging**, aplica primero ahí las Fases 1 (técnica) y prueba.
- Si **no** tienes staging y vas directo a producción:
  - Haz **copia de seguridad completa** (BD + archivos) antes de empezar.
  - Aplica los cambios **no destructivos** primero (metadatos, headings, textos).
  - Deja para el final, y de uno en uno, los **delicados**: redirecciones 301 y
    noindex. Verifica cada uno antes del siguiente.

---

## 0.2 Qué se ha detectado

| Elemento | Detección | Confianza |
|---|---|---|
| **Dominio** | `lenguajeconines.com` | Alta |
| **Tipo de instalación** | WordPress autoalojado + Jetpack (sin plan de pago) | Alta |
| **WooCommerce** | **Activo** — hay carrito en el menú, productos "Tarjetas para signar" con "Añadir al carrito" y precios | Alta |
| **LMS** | **Muy probablemente MasterStudy LMS** (StylemixThemes). Señales: páginas de curso con currículo lateral, progreso %, "lista de deseos", "Continuar"; y la auditoría menciona slugs `student-public-account` e `instructor-public-account`, característicos de MasterStudy | Media-alta ⚠️ VERIFICAR |
| **Builder** | **Elementor** como builder principal de la home y páginas (secciones tipo Elementor). La auditoría menciona `courses-archive-elementor` y `courses-archive-gutenberg`, así que conviven plantillas Elementor + Gutenberg | Media ⚠️ VERIFICAR |
| **Plugin SEO** | **No confirmable visualmente.** Es Yoast o Rank Math (la auditoría habla de sitemap y noindex). Las instrucciones de la Fase 1 cubren **ambos** | ⚠️ VERIFICAR |
| **Theme / child theme** | No confirmable. Probable theme compatible con MasterStudy/Stylemix. **Comprueba que exista child theme** antes de tocar `functions.php` | ⚠️ VERIFICAR |
| **Tipografías** | Títulos: *Lilita One* · Texto: *Open Sans* | Alta |
| **Paleta** | `#0d3d5d` (azul oscuro), `#1f6f8b` (azul medio), `#91d4d9` (turquesa), `#b5d2dd` / `#dde9f1` (fondos claros), `#ffbd59` (amarillo), `#737373` (gris texto) | Alta |

### Custom post types probables
- `stm-courses` (cursos LMS) y sus lecciones/cuestionarios (MasterStudy). ⚠️ VERIFICAR
- `product` (WooCommerce) → las "Tarjetas para signar".
- `post` (blog) y `page` (páginas).

---

## 0.3 Estructura actual observada

### Menú principal
`INICIO · CURSOS · RECURSOS · SOBRE MÍ · BLOG · CONTACTO` + 🛒 carrito + saludo "Hola, Inés" (sesión iniciada).

> ⚠️ **Problema clave de captación:** el menú **"RECURSOS" lleva a productos de
> pago** (tienda de tarjetas), no a recursos gratuitos. No hay ningún lead
> magnet gratuito visible en el menú. (Se corrige en Fase 3.)

### Home (`/`) — bloques actuales, en orden
1. **Hero** — H1 actual: *"¿Sabías que tu bebé puede comunicarse contigo antes de hablar?"* + subtítulo + CTAs **"Quiero saber más"** y **"Explora nuestros cursos"** + foto.
2. **"Comunicación accesible / desde la infancia"** — bloque de texto largo (varios párrafos sobre signos, LSE, evidencia). ⚠️ Verificar nivel de encabezado (parece H2 grande, posible segundo "H1" visual).
3. **"Beneficios de signar con bebés"** — 6 beneficios con icono de estrella.
4. **"Nuestros cursos"** — 4 tarjetas (ver tabla de cursos abajo).
5. **"Nuestros recursos"** — 4 productos de pago (tarjetas) + "Ver tienda".
6. **FAQ "¡Pregúntanos!"** — preguntas: edad para empezar / y si mi bebé no hace signos / puedo usar signos si mi hijo ya habla / para quién son los signos.

### Catálogo de cursos (página "Cursos")
Cabecera "NUESTROS CURSOS" + bloque de 3 ventajas + las 4 tarjetas de curso.

### Cursos (datos reales de las tarjetas)
| Curso | Público | Precio | Datos |
|---|---|---|---|
| **Familias Nivel 1** — Signos para bebés (con LSE) | Familias | **60 €** | 15 h estimadas · 53 clases · 1 asignación · Principiante · ★★★★★ |
| **Familias Nivel 2** — Signos para bebés (con LSE) | Familias | **60 €** | 13 h estimadas |
| **Familias Niveles 1 y 2 (pack)** | Familias | **100 €** | ★★★★★ |
| **Profesionales** — Sistema bimodal · signos para bebés (con LSE) | Profesionales | **150 €** | 30 h estimadas · 107 clases · 2 cuestionarios · Principiante |

### Páginas de curso (detalle)
Son **plantillas de reproductor del LMS** (currículo lateral con módulos
"Bienvenida / Módulo 1 - Marco teórico…", barra de progreso, "Continuar",
"Agregar a la lista de deseos", "Compartir"). **Funcionan como aula, no como
landing de venta** → es el punto débil comercial (se aborda en Fase 5).

### Sobre mí
H1 visual: *"¿Quién soy?"* / *"Inés Díez Sierra"*. Texto con credenciales
(Audición y Lenguaje, Pedagogía Terapéutica, Máster en NEE, asesora en signos,
LSE) + secciones "Mi propósito / Mi misión / Mis valores" + botón LinkedIn + vídeo.

### Blog (`/blog`)
Muestra **4 entradas** (sí se ven varias, no solo una):
1. *Cuando un niño no puede hablar, pero tiene mucho que decir: el sistema bimodal en el aula* — 4 jun 2026
2. *Qué es la comunicación bimodal y cómo puede apoyar el desarrollo del lenguaje infantil* — 20 abr 2026
3. *Signos para bebés y desarrollo del lenguaje: la importancia de los gestos antes de las primeras palabras* — 16 abr 2026
4. *¿Los signos para bebés retrasan el habla? Lo que realmente sabemos* — 13 abr 2026

> Nota: la auditoría decía "el blog solo muestra un post". En la captura se ven
> 4, así que **⚠️ VERIFICAR** si ya está resuelto o si hay otra vista (widget,
> home) que sí muestra solo uno.

### Contacto
H1 visual *"¡Queremos escucharte!"* + formulario (Nombre, Correo, Mensaje,
Teléfono opcional, Tipo de consulta, Enviar).

---

## 0.4 Hallazgos priorizados (lista de tareas antes de implementar)

**🔴 Urgente (Fase 1 — técnico):**
1. H1 de la home es una pregunta sin keyword. Cambiar a *"Enseña a tu bebé a comunicarse antes de hablar"*.
2. ⚠️ Verificar que haya **un solo H1** por página y jerarquía H2/H3 correcta (el bloque "Comunicación accesible" parece competir con el H1).
3. **Noindex + exclusión de sitemap** de páginas técnicas: carrito, finalizar-compra, pago, mi-cuenta, lista-de-deseos, student-public-account, instructor-public-account, sample-page, login.
4. **Canibalización de catálogo de cursos**: dejar una sola URL (`/cursos/`) y 301 desde duplicados (`/nuestros-cursos/`, `/pagina-de-cursos/`, `/courses-archive-elementor/`, `/courses-archive-gutenberg/`). ⚠️ VERIFICAR cuáles existen.
5. Meta title + meta description en todas las páginas principales.
6. Alt text en imágenes clave.

**🟠 Importante (Fase 2 — home/conversión):**
7. Bloque de **segmentación Familia / Profesional** (no existe).
8. Bloque de **autoridad de Inés con foto + credenciales** en la home (hoy solo en Sobre mí).
9. **Lead magnet gratuito visible** en la home (no existe).

**🟡 Captación (Fase 3):**
10. Renombrar/reordenar "Recursos" (que hoy va a la tienda de pago) y crear/enlazar **`/recursos-gratis/`**.
11. CTAs contextuales a recursos gratuitos en home, menú, footer y blog.

**🟢 Posterior (Fases 4-9, fuera de este entregable):** páginas pilar
`/signos-para-bebes/` y `/sistema-bimodal/`, convertir páginas de curso en
landings, schema, enlazado interno completo, footer.

---

## 0.5 Lo que NO se ha podido verificar (pendiente de acceso o de tu confirmación)
- Plugin SEO exacto (Yoast vs Rank Math) y su configuración de sitemap.
- Theme y existencia de child theme.
- LMS exacto y sus slugs reales de páginas técnicas.
- Slugs reales actuales de cada página (p. ej. si "Cursos" es `/cursos/` o `/nuestros-cursos/`).
- Qué URLs duplicadas de catálogo existen realmente.
- Estructura HTML real de encabezados (niveles H1/H2/H3).
- IDs de medios para asignar alt text.
- Footer (no hay captura).
