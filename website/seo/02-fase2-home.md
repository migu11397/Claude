# FASE 2 — Home orientada a SEO y conversión (copy listo para pegar)

> Objetivo: que en los primeros segundos un visitante que llega **frío desde
> Google** entienda qué es Lenguaje con Inés, para quién es, qué problema
> resuelve, por qué confiar en Inés y qué camino elegir (familia o profesional).
>
> Tu home ya tiene una buena base (hero, beneficios, cursos, FAQ). Aquí tienes
> los **textos exactos** + qué **bloques nuevos** añadir y en qué **orden**.
> Cada bloque trae versión en **texto plano** (para Elementor) y, cuando es útil,
> **bloque Gutenberg** (pegable en el editor de código `Añadir bloque → HTML
> personalizado` o en una página Gutenberg). Usa la paleta y tipografías de marca.

## Orden recomendado de la home
1. Hero (mejorar)
2. **Segmentación Familia / Profesional** (NUEVO)
3. Comunicación accesible (mantener, como apoyo)
4. **Autoridad de Inés** (NUEVO en home)
5. Beneficios (mantener)
6. **Lead magnet gratuito** (NUEVO)
7. Nuestros cursos (mantener, mejorar textos)
8. **"Por qué Lenguaje con Inés"** (NUEVO, opcional)
9. Testimonios (estructura preparada, sin inventar)
10. FAQ (mantener)
11. CTA final + enlaces

---

## 1) HERO (mejorar el actual)

- **H1:** `Enseña a tu bebé a comunicarse antes de hablar`
- **Subtítulo:** `Cursos online de signos para bebés y sistema bimodal para familias y profesionales que quieren acompañar el desarrollo del lenguaje con herramientas claras, respetuosas y basadas en evidencia.`
- **CTA principal:** `Ver cursos` → `/cursos/`
- **CTA secundario:** `Descargar recurso gratuito` → `/recursos-gratis/` (o `/tarjetas-gratis/` ⚠️ VERIFICAR URL real)

> Mantén la foto actual del hero. Solo cambia el texto del título a H1 y ajusta
> los botones.

---

## 2) SEGMENTACIÓN FAMILIA / PROFESIONAL (NUEVO)

Texto plano:

- **Título de sección (H2):** `¿Por dónde quieres empezar?`
- **Tarjeta 1 — Título (H3):** `Soy familia`
  - Texto: `Quiero ayudar a mi bebé o peque a comunicarse mejor antes de que pueda hablar.`
  - CTA: `Ver cursos para familias` → `/cursos/` (o ficha familias)
- **Tarjeta 2 — Título (H3):** `Soy profesional`
  - Texto: `Quiero incorporar signos y sistema bimodal en el aula, la intervención o la atención temprana.`
  - CTA: `Ver curso para profesionales` → ficha del curso de profesionales

Bloque Gutenberg (pegable):

```html
<!-- wp:heading {"level":2} -->
<h2 class="wp-block-heading">¿Por dónde quieres empezar?</h2>
<!-- /wp:heading -->

<!-- wp:columns -->
<div class="wp-block-columns">
  <!-- wp:column {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"2rem"}}}} -->
  <div class="wp-block-column has-background" style="background-color:#dde9f1;padding:2rem">
    <!-- wp:heading {"level":3} --><h3 class="wp-block-heading">Soy familia</h3><!-- /wp:heading -->
    <!-- wp:paragraph --><p>Quiero ayudar a mi bebé o peque a comunicarse mejor antes de que pueda hablar.</p><!-- /wp:paragraph -->
    <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#1f6f8b"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-background wp-element-button" style="background-color:#1f6f8b" href="/cursos/">Ver cursos para familias</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
  </div>
  <!-- /wp:column -->
  <!-- wp:column {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"2rem"}}}} -->
  <div class="wp-block-column has-background" style="background-color:#dde9f1;padding:2rem">
    <!-- wp:heading {"level":3} --><h3 class="wp-block-heading">Soy profesional</h3><!-- /wp:heading -->
    <!-- wp:paragraph --><p>Quiero incorporar signos y sistema bimodal en el aula, la intervención o la atención temprana.</p><!-- /wp:paragraph -->
    <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#1f6f8b"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-background wp-element-button" style="background-color:#1f6f8b" href="/cursos/sistema-bimodal-profesionales/">Ver curso para profesionales</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
  </div>
  <!-- /wp:column -->
</div>
<!-- /wp:columns -->
```

> En Elementor: usa una sección de 2 columnas con fondo `#dde9f1`, cada una con
> Título (H3) + Texto + Botón.

---

## 3) COMUNICACIÓN ACCESIBLE (mantener)
Mantén el texto actual; solo asegúrate de que el título es **H2** (ver Fase 1).
Es buen contenido de apoyo y refuerzo de confianza/evidencia.

---

## 4) AUTORIDAD DE INÉS (NUEVO en home)

- **Título (H2):** `Quién te acompaña`
- **Foto:** usa la foto de Inés que ya está en la biblioteca (la de Sobre mí).
- **Texto:**
  > `Soy Inés, maestra de Audición y Lenguaje y Pedagogía Terapéutica, con Máster en Necesidades Educativas Especiales. Acompaño a familias y profesionales en el uso de signos, comunicación temprana y sistema bimodal para favorecer el desarrollo del lenguaje infantil.`
- **Credenciales (lista):**
  - Maestra de Audición y Lenguaje
  - Maestra de Pedagogía Terapéutica
  - Máster en Necesidades Educativas Especiales
  - Especialista en comunicación temprana
  - Experiencia con familias, centros y contexto bilingüe en Dinamarca
- **CTA:** `Conoce mi historia` → `/sobre-mi/`

---

## 5) BENEFICIOS (mantener)
Mantén los 6 beneficios actuales. Solo revisa headings (sección = H2, cada
beneficio = H3) según Fase 1.

---

## 6) LEAD MAGNET GRATUITO (NUEVO — clave para captación)

- **Título (H2):** `Empieza hoy, gratis`
- **Texto:** `Descarga gratis tus primeras tarjetas de signos para bebés y empieza a comunicarte con tu peque desde casa.`
- **CTA:** `Descargar tarjetas gratis` → `/recursos-gratis/` o `/tarjetas-gratis/` ⚠️ VERIFICAR URL real

Bloque Gutenberg (pegable):

```html
<!-- wp:group {"style":{"color":{"background":"#91d4d9"},"spacing":{"padding":{"all":"2.5rem"}}},"layout":{"type":"constrained"}} -->
<div class="wp-block-group has-background" style="background-color:#91d4d9;padding:2.5rem">
  <!-- wp:heading {"level":2,"textAlign":"center"} --><h2 class="wp-block-heading has-text-align-center">Empieza hoy, gratis</h2><!-- /wp:heading -->
  <!-- wp:paragraph {"align":"center"} --><p class="has-text-align-center">Descarga gratis tus primeras tarjetas de signos para bebés y empieza a comunicarte con tu peque desde casa.</p><!-- /wp:paragraph -->
  <!-- wp:buttons {"layout":{"type":"flex","justifyContent":"center"}} --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#ffbd59","text":"#0d3d5d"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-text-color has-background wp-element-button" style="color:#0d3d5d;background-color:#ffbd59" href="/recursos-gratis/">Descargar tarjetas gratis</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
</div>
<!-- /wp:group -->
```

> ⚠️ Si aún no existe la página `/recursos-gratis/` ni `/tarjetas-gratis/`, mira
> la Fase 3: ahí se explica cómo dejarla lista.

---

## 7) NUESTROS CURSOS (mantener, afinar textos)

Mantén las 4 tarjetas. Recomendación: que cada tarjeta deje claro **público +
beneficio + precio + CTA**. Textos sugeridos:

- **Familias Nivel 1** — *Para familias · 60 €*
  `Tus primeros signos para comunicarte con tu bebé antes de que hable.`
  CTA: `Ver curso`
- **Familias Nivel 2** — *Para familias · 60 €*
  `Amplía vocabulario y acompaña el siguiente paso del lenguaje de tu peque.`
  CTA: `Ver curso`
- **Pack Familias 1 y 2** — *Para familias · 100 €*
  `Los dos niveles juntos, con todo el recorrido paso a paso.`
  CTA: `Ver pack`
- **Profesionales (Sistema bimodal)** — *Para profesionales · 150 €*
  `Incorpora signos y sistema bimodal en el aula, la atención temprana o la logopedia.`
  CTA: `Ver curso`

---

## 8) POR QUÉ LENGUAJE CON INÉS (NUEVO, opcional pero recomendado)

- **Título (H2):** `Por qué Lenguaje con Inés`
- Puntos (lista con icono):
  - Enfoque **basado en evidencia**
  - Signos tomados de la **Lengua de Signos Española (LSE)**
  - **Apoyo al lenguaje oral** (no lo sustituye)
  - **Experiencia profesional** real (AL, PT, NEE)
  - Método **práctico** y aplicable desde el primer día
  - Para **familias y profesionales**
  - **Comunicación respetuosa** con el ritmo del bebé

---

## 9) TESTIMONIOS (estructura preparada — NO inventar)

> No inventes testimonios. Deja la sección lista y rellénala cuando tengas
> reseñas reales (las fichas de curso ya muestran ★★★★★, así que probablemente
> tengas valoraciones que reutilizar con permiso).

- **Título (H2):** `Lo que dicen las familias y profesionales`
- Marcador interno (no publicar tal cual): `[PENDIENTE: añadir 3 testimonios reales con nombre/rol y, si es posible, foto]`

---

## 10) FAQ (mantener y ampliar)

Tu FAQ ya existe. Mantenla como **H2** con cada pregunta en **H3**. Añade, si
encajan, estas orientadas a objeciones SEO/venta:

- **¿Los signos retrasan el habla?** → `No. La evidencia indica que los signos acompañan y favorecen el lenguaje oral; los bebés pueden signar antes porque la motricidad de las manos madura antes que el habla.`
- **¿Desde qué edad se puede empezar?** → `Se puede empezar pronto, adaptando los signos a cada etapa. Nunca es tarde si tu peque aún está desarrollando el lenguaje.`
- **¿Sirve si mi bebé ya dice algunas palabras?** → `Sí. Los signos siguen siendo un apoyo útil para la comprensión y la expresión incluso cuando ya aparecen las primeras palabras.`
- **¿Es lengua de signos o sistema bimodal?** → `Trabajo con signos tomados de la LSE como apoyo a la comunicación; el sistema bimodal combina habla y signo a la vez.`
- **¿Es para familias o también para profesionales?** → `Para ambos: hay cursos para familias y un curso de sistema bimodal para profesionales.`

> Estas preguntas reales habilitan **FAQPage schema** más adelante (Fase 8).

---

## 11) CTA FINAL + enlaces internos

Cierra la home con un bloque de llamada a la acción y enlaces a lo importante
(refuerza el enlazado interno de la Fase 7):

- **Título (H2):** `¿Empezamos?`
- Botones: `Ver cursos` (`/cursos/`) · `Descargar tarjetas gratis` (`/recursos-gratis/`)
- Enlaces de texto: `signos para bebés` (futura pilar `/signos-para-bebes/`),
  `sistema bimodal` (futura pilar `/sistema-bimodal/`), `Sobre mí` (`/sobre-mi/`).

---

## Verificación Fase 2
- [ ] H1 único y nuevo en el hero.
- [ ] Bloque de segmentación visible "arriba" (above the fold o justo debajo).
- [ ] Bloque de autoridad con foto + credenciales.
- [ ] Lead magnet gratuito visible y enlazado.
- [ ] Tarjetas de curso con público + beneficio + precio + CTA.
- [ ] FAQ con preguntas reales.
- [ ] Móvil: comprobar que las columnas se apilan bien y los botones se tocan fácil.
