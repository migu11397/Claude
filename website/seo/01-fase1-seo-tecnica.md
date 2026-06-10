# FASE 1 — Limpieza SEO técnica (listo para aplicar)

> Todo lo de aquí es **para pegar/configurar a mano**. Cada bloque indica
> **dónde** se aplica. Los cambios marcados **🔴 DELICADO** (noindex y
> redirecciones) hazlos al final, de uno en uno y, si puedes, primero en staging.

---

## 1.1 Encabezados de la home

**Acción:** edita la home en Elementor.

- **H1 (uno solo):** `Enseña a tu bebé a comunicarse antes de hablar`
  - Pon este texto como el **único H1** de la página (HTML tag `H1` en el widget de título del hero).
  - El subtítulo del hero NO debe ser H1; déjalo como widget "Texto" o título con etiqueta `p`/`H2` pequeña.
- **"Comunicación accesible"** → debe ser **H2** (no un segundo H1). "Desde la infancia" → subtítulo (texto normal o `span`, no encabezado).
- Los párrafos largos de esa sección → **texto normal** (no encabezados).
- **"Beneficios de signar con bebés"** → **H2**. Cada beneficio ("Fomenta el vínculo afectivo", etc.) → **H3**.
- **"Nuestros cursos"** → **H2**. El título de cada curso → **H3**.
- **"Nuestros recursos"** → **H2**.
- **"¡Pregúntanos!" (FAQ)** → **H2**. Cada pregunta → **H3**.

> Regla general: **1 × H1**, luego **H2** para secciones, **H3** para subsecciones.
> Nada de encabezados vacíos ni párrafos marcados como H2.

**Cómo cambiar el tag en Elementor:** clic en el widget de título → pestaña
*Contenido* → campo **"HTML Tag"** → elige H1/H2/H3. (El tamaño visual no cambia
si ajustas el estilo; el tag es solo semántico para SEO.)

---

## 1.2 Metadatos por página (title + meta description + slug)

> Aplícalos en el plugin SEO (Yoast: caja "Yoast SEO" bajo el editor → "SEO" →
> *Título SEO* y *Meta descripción*. Rank Math: caja "Rank Math" → *Edit Snippet*).
> Títulos ≈ 55-60 caracteres; descripciones ≈ 150-160. **No** cambies un slug ya
> indexado sin poner una 301 (ver 1.5).

### Home `/`
- **Title:** `Signos para bebés y sistema bimodal | Lenguaje con Inés`
- **Meta description:** `Cursos online de signos para bebés y sistema bimodal para familias y profesionales. Acompaña el desarrollo del lenguaje con método claro y basado en evidencia.`
- **Slug:** `/` (no tocar)

### Sobre mí
- **H1 recomendado (visible):** `Inés Díez Sierra, especialista en comunicación temprana` *(puedes mantener el estilo "¿Quién soy?" como antetítulo no-H1).*
- **Title:** `Sobre Inés Díez Sierra | Lenguaje con Inés`
- **Meta description:** `Soy Inés, maestra de Audición y Lenguaje y Pedagogía Terapéutica con Máster en NEE. Acompaño a familias y profesionales en signos y sistema bimodal.`
- **Slug sugerido:** `/sobre-mi/` ⚠️ VERIFICAR el actual (si cambia, 301)

### Cursos (catálogo)
- **H1:** `Cursos de signos para bebés y sistema bimodal`
- **Title:** `Cursos de signos para bebés y sistema bimodal | Lenguaje con Inés`
- **Meta description:** `Descubre los cursos online de Lenguaje con Inés: signos para bebés para familias y sistema bimodal para profesionales. Empieza a comunicarte antes del habla.`
- **Slug objetivo:** `/cursos/` (canónica única — ver 1.4)

### Curso Familias Nivel 1
- **Title:** `Curso de signos para bebés para familias (Nivel 1) | Lenguaje con Inés`
- **Meta description:** `Aprende a comunicarte con tu bebé antes de que hable. Curso online de signos para bebés (con LSE) para familias: 53 clases, método práctico y respetuoso.`

### Curso Familias Nivel 2
- **Title:** `Curso de signos para bebés para familias (Nivel 2) | Lenguaje con Inés`
- **Meta description:** `Amplía el vocabulario de signos con tu bebé y acompaña su desarrollo del lenguaje. Nivel 2 del curso de signos para bebés de Lenguaje con Inés.`

### Pack Familias Niveles 1 y 2
- **Title:** `Pack curso de signos para bebés Niveles 1 y 2 | Lenguaje con Inés`
- **Meta description:** `Los dos niveles del curso de signos para bebés para familias en un solo pack. Aprende paso a paso a comunicarte con tu bebé antes del habla.`

### Curso Profesionales (Sistema bimodal)
- **Title:** `Curso de sistema bimodal para profesionales | Lenguaje con Inés`
- **Meta description:** `Formación en sistema bimodal y signos para profesionales de educación infantil, atención temprana y logopedia. 30 h, casos prácticos y aplicación en el aula.`

### Blog
- **Title:** `Blog sobre signos para bebés y desarrollo del lenguaje | Lenguaje con Inés`
- **Meta description:** `Artículos sobre signos para bebés, sistema bimodal, comunicación temprana y desarrollo del lenguaje infantil, con enfoque práctico y basado en evidencia.`

### Recursos / Tienda (productos de pago)
- **Title:** `Materiales y tarjetas de signos para descargar | Lenguaje con Inés`
- **Meta description:** `Tarjetas de signos para imprimir y materiales descargables para empezar a signar con tu bebé en casa: colores, animales, granja y bosque.`
- **Nota:** ver Fase 3 — conviene renombrar este apartado a "Materiales/Tienda" y reservar "Recursos gratis" para captación.

### Contacto
- **H1 recomendado:** `Contacto` *(puedes mantener "¡Queremos escucharte!" como subtítulo).*
- **Title:** `Contacto | Lenguaje con Inés`
- **Meta description:** `¿Tienes dudas sobre los cursos de signos para bebés o sistema bimodal? Escríbenos y te ayudamos a elegir el camino adecuado para ti.`
- **Recomendación:** marcar **noindex** si solo es un formulario sin contenido útil para Google (opcional; no es urgente).

---

## 1.3 🔴 Noindex + exclusión del sitemap (DELICADO)

**Objetivo:** que no posicionen en Google las páginas técnicas, SIN romper
checkout ni acceso de alumnos. **No se borra nada**, solo se marca noindex y se
saca del sitemap.

### Páginas a marcar `noindex`
- `sample-page` (página de ejemplo de WordPress)
- `carrito` / `cart`
- `finalizar-compra` / `checkout`
- `pago` (si existe como página)
- `mi-cuenta` / `my-account`
- `lista-de-deseos` / `wishlist`
- `cuenta-del-usuario`
- `student-public-account`
- `instructor-public-account`
- páginas técnicas del LMS (perfiles, "continuar", áreas privadas)
- páginas de login / recuperar contraseña

> ⚠️ **NO** marques noindex la página **catálogo de cursos** (`/cursos/`) ni las
> **fichas de curso** que quieras vender ni los **productos** que sí quieras
> posicionar. Solo lo técnico/privado.

### Cómo hacerlo

**Si es Yoast SEO:**
- Por página: editar página → caja Yoast → pestaña **"Avanzado"** → *"¿Permitir
  que los motores de búsqueda muestren esta página en los resultados?"* → **No**.
  Esto añade `noindex` y, en Yoast, **también la excluye del sitemap**.
- WooCommerce: Yoast suele excluir carrito/checkout/cuenta automáticamente; aun
  así verifícalo.

**Si es Rank Math:**
- Por página: editar → caja Rank Math → pestaña **"Advanced"** → *Robots Meta* →
  marca **"No Index"**. Rank Math también las saca del sitemap al ponerlas noindex.
- O en *Rank Math → Titles & Meta* puedes definir reglas por tipo de contenido.

**Verificación:** tras aplicarlo, abre la URL de la página, "ver código fuente"
y busca `<meta name="robots" content="noindex` — debe aparecer. Y comprueba que
**ya no** esté en el sitemap (ver 1.5).

---

## 1.4 🔴 Canibalización del catálogo de cursos

**Objetivo:** **una sola URL** de catálogo de cursos como canónica.

1. Decide la URL canónica. Recomendada: **`/cursos/`** (limpia y clara). Si tu
   página de catálogo actual ya es `/cursos/`, perfecto.
2. ⚠️ VERIFICAR cuáles de estas existen realmente (búscalas en Páginas y en el
   navegador):
   - `/nuestros-cursos/`
   - `/pagina-de-cursos/`
   - `/courses-archive-elementor/`
   - `/courses-archive-gutenberg/`
   - el archivo por defecto del LMS (p. ej. `/courses/`)
3. Para cada duplicada que **no** sea la canónica:
   - Si **no la necesita el LMS internamente** → **301 → `/cursos/`** (ver 1.5).
   - Si el LMS **la necesita** para funcionar → **no la borres**; ponla
     **noindex** + **canonical apuntando a `/cursos/`** (en Yoast/Rank Math,
     campo "URL canónica" en la pestaña Avanzado/Advanced).

> Importante: antes de redirigir el archivo nativo del LMS, comprueba que
> `/cursos/` muestra todos los cursos correctamente, para no dejar a nadie sin
> catálogo funcional.

---

## 1.5 🔴 Redirecciones 301 (lista a crear)

**Plugin recomendado:** "Redirection" (gratuito) o el módulo de redirecciones de
Rank Math (*Rank Math → Redirections*). Yoast Premium también las tiene.

**Redirecciones propuestas** (ajusta orígenes a los que existan de verdad):

| Origen (301) | Destino |
|---|---|
| `/nuestros-cursos/` | `/cursos/` |
| `/pagina-de-cursos/` | `/cursos/` |
| `/courses-archive-elementor/` | `/cursos/` |
| `/courses-archive-gutenberg/` | `/cursos/` |
| `/courses/` *(archivo LMS, solo si no es necesario)* | `/cursos/` |

**Verificación:** abre cada origen en el navegador en incógnito → debe llevar a
`/cursos/` con código 301 (puedes comprobarlo con una extensión "Redirect Path"
o en *Inspeccionar → Network*).

> ⚠️ No crees redirecciones "en cadena" (A→B→C). Apunta todo directo a `/cursos/`.

---

## 1.6 Sitemap

1. Asegúrate de que el sitemap **incluye**: home, páginas principales, `/cursos/`,
   fichas de curso a posicionar, posts del blog, productos a posicionar y (cuando
   existan) las páginas pilar.
2. **Excluye** todo lo marcado noindex en 1.3 (al ponerlas noindex, Yoast/Rank
   Math las quitan solas; verifícalo).
3. Comprueba que el sitemap sigue accesible:
   - Yoast: `https://lenguajeconines.com/sitemap_index.xml`
   - Rank Math: `https://lenguajeconines.com/sitemap_index.xml`
4. (Recomendado) Reenvía el sitemap en **Google Search Console** tras los cambios.

---

## 1.7 Imágenes — alt text

**Acción:** en *Medios* (o al editar cada imagen en Elementor), rellena el campo
**"Texto alternativo"**. Natural y descriptivo, sin keyword stuffing.

Ejemplos por imagen típica:
- Hero home → `bebé y madre comunicándose con signos antes de hablar`
- Foto de Inés → `Inés Díez Sierra, especialista en comunicación temprana y lenguaje infantil`
- Tarjeta curso familias → `curso de signos para bebés para familias de Lenguaje con Inés`
- Tarjeta curso profesionales → `curso de sistema bimodal para profesionales de educación infantil`
- Producto tarjetas → `tarjetas de signos para bebés para imprimir y usar en casa`
- Bloque beneficios → `bebé usando signos para comunicarse antes de hablar`

> Regla: describe lo que se ve + contexto de marca cuando aporte. Una frase por
> imagen. No repitas la misma keyword en todas.

---

## 1.8 Checklist de verificación de la Fase 1
- [ ] Home tiene **un solo H1** y es el nuevo.
- [ ] Jerarquía H2/H3 correcta en home.
- [ ] Title + meta description en todas las páginas de 1.2.
- [ ] Páginas técnicas en **noindex** (verificado en código fuente).
- [ ] Esas páginas **fuera del sitemap**.
- [ ] Catálogo de cursos con **una sola URL**; duplicados con 301 o canonical.
- [ ] Redirecciones 301 probadas en incógnito.
- [ ] Sitemap accesible y correcto.
- [ ] Alt text en imágenes principales.
- [ ] **Checkout, carrito, login y acceso a cursos siguen funcionando.**
