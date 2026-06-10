# FASE 3 — Lead magnets y captación (listo para aplicar)

> Objetivo: que la web **convierta tráfico frío en leads**, no solo en visitas.
> Hoy el menú "Recursos" lleva a **productos de pago** y no hay ningún recurso
> gratuito visible. Esto lo arreglamos aquí.

---

## 3.1 Página de recursos gratuitos `/recursos-gratis/`

**Acción:** crea (o verifica si ya existe) una página con slug **`/recursos-gratis/`**.

⚠️ VERIFICAR primero si ya existen estas páginas (búscalas en Páginas y en el navegador):
- `/tarjetas-gratis/`
- `/masterclass-bimodal/`
- alguna landing de descarga ya creada

Si existen, **úsalas y enlázalas**; no dupliques. Si no existen, crea
`/recursos-gratis/` como página "hub" que agrupe todos los gratuitos.

### Contenido sugerido de `/recursos-gratis/`
- **H1:** `Recursos gratis para empezar a signar con tu bebé`
- **Title:** `Recursos gratis de signos para bebés | Lenguaje con Inés`
- **Meta description:** `Descarga gratis tarjetas de signos para bebés y accede a la masterclass de sistema bimodal. Recursos para familias y profesionales para empezar hoy.`
- **Intro:** `Empieza hoy mismo. Aquí tienes recursos gratuitos para familias y profesionales: descárgalos y comienza a comunicarte antes del habla.`
- **Dos bloques (familia / profesional):**
  - **Para familias:** `Tarjetas de signos para bebés (gratis)` → CTA `Descargar tarjetas gratis`
  - **Para profesionales:** `Masterclass gratuita de sistema bimodal` → CTA `Acceder a la masterclass`
- **Captura de email:** lo ideal es que la descarga pida el email (formulario de
  tu plugin de newsletter/formularios) para convertir la visita en **lead**.
  ⚠️ VERIFICAR qué herramienta de email usas (Mailchimp, MailerLite, Brevo, etc.).

Bloque Gutenberg base (pegable):

```html
<!-- wp:heading {"level":1} -->
<h1 class="wp-block-heading">Recursos gratis para empezar a signar con tu bebé</h1>
<!-- /wp:heading -->
<!-- wp:paragraph -->
<p>Empieza hoy mismo. Aquí tienes recursos gratuitos para familias y profesionales: descárgalos y comienza a comunicarte antes del habla.</p>
<!-- /wp:paragraph -->
<!-- wp:columns -->
<div class="wp-block-columns">
  <!-- wp:column {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"2rem"}}}} -->
  <div class="wp-block-column has-background" style="background-color:#dde9f1;padding:2rem">
    <!-- wp:heading {"level":2} --><h2 class="wp-block-heading">Para familias</h2><!-- /wp:heading -->
    <!-- wp:paragraph --><p>Tus primeras tarjetas de signos para bebés, listas para imprimir y usar en casa.</p><!-- /wp:paragraph -->
    <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#ffbd59","text":"#0d3d5d"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-text-color has-background wp-element-button" style="color:#0d3d5d;background-color:#ffbd59" href="#">Descargar tarjetas gratis</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
  </div>
  <!-- /wp:column -->
  <!-- wp:column {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"2rem"}}}} -->
  <div class="wp-block-column has-background" style="background-color:#dde9f1;padding:2rem">
    <!-- wp:heading {"level":2} --><h2 class="wp-block-heading">Para profesionales</h2><!-- /wp:heading -->
    <!-- wp:paragraph --><p>Masterclass gratuita sobre sistema bimodal aplicado al aula y la intervención.</p><!-- /wp:paragraph -->
    <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#1f6f8b"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-background wp-element-button" style="background-color:#1f6f8b" href="#">Acceder a la masterclass</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
  </div>
  <!-- /wp:column -->
</div>
<!-- /wp:columns -->
```

---

## 3.2 Reorganización del menú (importante)

**Problema actual:** "RECURSOS" → tienda de pago. Confunde a quien busca algo gratis.

**Propuesta de menú:**

`INICIO · CURSOS · RECURSOS GRATIS · MATERIALES · SOBRE MÍ · BLOG · CONTACTO` 🛒

- **RECURSOS GRATIS** → `/recursos-gratis/` (captación / lead magnets).
- **MATERIALES** (o **TIENDA**) → la tienda actual de tarjetas de pago (lo que hoy es "Recursos").
- Mantén el resto igual.

> Si no quieres añadir dos entradas, como mínimo **renombra "Recursos" → "Tienda"
> / "Materiales"** y añade **"Recursos gratis"**. Lo esencial: que "gratis" y
> "pago" no se confundan.

**Cómo:** *Apariencia → Menús* (o el menú de Elementor si usas su header).

---

## 3.3 Enlazar los recursos gratis desde todas partes

Coloca enlaces a `/recursos-gratis/` (y, si existen, `/tarjetas-gratis/` y
`/masterclass-bimodal/`) en:

- ✅ **Home** — bloque lead magnet (Fase 2, punto 6).
- ✅ **Menú** — entrada "Recursos gratis".
- ✅ **Footer** — enlace "Recursos gratis" (ver Fase 9).
- ✅ **Cada post del blog** — CTA contextual (abajo).
- ✅ **Páginas de cursos** — enlace "¿Aún lo estás pensando? Descarga las tarjetas gratis".
- ✅ **Artículos relacionados** entre sí.

---

## 3.4 CTA contextuales por tipo de contenido

Pega estos bloques al final (o a mitad) de los posts, según el público.

**En posts de FAMILIAS** (p. ej. "¿Los signos retrasan el habla?", "Signos para bebés y desarrollo del lenguaje"):

```html
<!-- wp:group {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"1.5rem"}}},"layout":{"type":"constrained"}} -->
<div class="wp-block-group has-background" style="background-color:#dde9f1;padding:1.5rem">
  <!-- wp:paragraph --><p><strong>Descarga gratis tus primeras tarjetas de signos</strong> para empezar a comunicarte con tu bebé en casa.</p><!-- /wp:paragraph -->
  <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#ffbd59","text":"#0d3d5d"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-text-color has-background wp-element-button" style="color:#0d3d5d;background-color:#ffbd59" href="/recursos-gratis/">Descargar tarjetas gratis</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
</div>
<!-- /wp:group -->
```

**En posts de PROFESIONALES** (p. ej. "Qué es la comunicación bimodal…", "El sistema bimodal en el aula"):

```html
<!-- wp:group {"style":{"color":{"background":"#dde9f1"},"spacing":{"padding":{"all":"1.5rem"}}},"layout":{"type":"constrained"}} -->
<div class="wp-block-group has-background" style="background-color:#dde9f1;padding:1.5rem">
  <!-- wp:paragraph --><p><strong>Accede a la masterclass gratuita</strong> sobre sistema bimodal aplicado al aula y la intervención.</p><!-- /wp:paragraph -->
  <!-- wp:buttons --><div class="wp-block-buttons"><!-- wp:button {"style":{"color":{"background":"#1f6f8b"}}} --><div class="wp-block-button"><a class="wp-block-button__link has-background wp-element-button" style="background-color:#1f6f8b" href="/recursos-gratis/">Acceder a la masterclass</a></div><!-- /wp:button --></div><!-- /wp:buttons -->
</div>
<!-- /wp:group -->
```

### Mapeo de tus 4 posts actuales → CTA
| Post | Público | CTA a poner |
|---|---|---|
| ¿Los signos para bebés retrasan el habla? | Familias | Tarjetas gratis |
| Signos para bebés y desarrollo del lenguaje | Familias | Tarjetas gratis |
| Qué es la comunicación bimodal… | Profesionales | Masterclass bimodal |
| El sistema bimodal en el aula | Profesionales | Masterclass bimodal |

---

## 3.5 Verificación Fase 3
- [ ] Existe y carga `/recursos-gratis/` (o la equivalente real).
- [ ] El menú distingue claramente "Recursos gratis" de "Tienda/Materiales".
- [ ] El lead magnet de la home enlaza a la página correcta.
- [ ] Cada post tiene su CTA contextual.
- [ ] (Recomendado) La descarga capta el email en tu herramienta de newsletter.
