# Mejoras SEO Lenguaje con Inés — Fases 0 a 3

Paquete **listo para aplicar a mano** en el WordPress de `lenguajeconines.com`.
Cubre **Fase 0 (inspección) + Fase 1 (SEO técnica) + Fase 2 (home) + Fase 3
(lead magnets)**. Las Fases 4-10 (páginas pilar, landings de curso, schema,
enlazado interno completo, footer, verificación) quedan para una segunda tanda.

## ⚠️ Por qué "a mano" y no automático
La conexión MCP detecta tu sitio como **WordPress autoalojado con Jetpack SIN
plan de pago**, así que **todas** las operaciones de leer/escribir contenido,
ajustes y tema están bloqueadas (error "requires a paid Jetpack plan"). Por eso
no he tocado tu web: te entrego todo redactado y estructurado para que lo pegues.
Si en algún momento activas un plan Jetpack de pago + las *abilities* en
`wordpress.com/me/mcp`, puedo aplicarlo yo directamente.

## Archivos
| Archivo | Contenido |
|---|---|
| `00-informe-fase0-inspeccion.md` | Diagnóstico de la web actual + tareas priorizadas |
| `01-fase1-seo-tecnica.md` | Headings, metadatos, noindex, redirecciones, sitemap, alt text |
| `02-fase2-home.md` | Copy y bloques de la home (texto + Gutenberg) |
| `03-fase3-lead-magnets.md` | Página de recursos gratis, menú y CTAs |

---

## RESUMEN EJECUTIVO

Tu web **ya tiene una base sólida** (hero, beneficios, cursos, FAQ, blog con
varios posts, página Sobre mí completa). Los problemas que más frenan el SEO y la
conversión, por orden de urgencia:

1. **H1 de la home** es una pregunta sin keyword → cambiar a *"Enseña a tu bebé a
   comunicarse antes de hablar"*.
2. **Páginas técnicas indexables** (carrito, checkout, cuenta, lista de deseos,
   perfiles del LMS, sample-page) → noindex + fuera del sitemap.
3. **Probable canibalización** del catálogo de cursos (varias URLs) → una sola
   `/cursos/` + 301.
4. **Falta de captación**: el menú "Recursos" lleva a pago y no hay lead magnet
   gratuito visible → crear/enlazar `/recursos-gratis/` y reordenar menú.
5. **Home sin segmentación** familia/profesional, sin bloque de autoridad de Inés
   y sin lead magnet → añadir esos bloques.
6. **Páginas de curso = plantilla de aula del LMS**, no landings de venta (se
   aborda en Fase 5, segunda tanda).

---

## ORDEN RECOMENDADO PARA APLICAR

1. **Antes de nada:** confirma producción vs staging y haz copia de seguridad.
2. **Fase 1 no destructiva:** headings de la home + metadatos de todas las
   páginas + alt text. (Riesgo bajo.)
3. **Fase 2:** mejorar home (hero, segmentación, autoridad, lead magnet, FAQ).
4. **Fase 3:** página `/recursos-gratis/`, menú y CTAs.
5. **Fase 1 delicada (al final, una a una):** noindex de técnicas → verificar →
   redirecciones 301 → verificar → sitemap → reenviar en Search Console.
6. **Verificación final:** checkout, carrito, login y acceso a cursos OK; sitemap
   carga; móvil usable.

---

## INFORME (estructura del entregable)

- **1. Resumen ejecutivo** → arriba.
- **2. Cambios realizados** → *Ninguno sobre la web* (sin acceso de escritura).
  Entregado: paquete documental completo Fases 0-3 (4 archivos).
- **3. Cambios no realizados y motivo** → todo lo "ejecutable" sobre WordPress,
  porque el plan Jetpack del sitio no permite operaciones MCP de contenido. Queda
  preparado para pegar o para que lo aplique yo con acceso.
- **4. Páginas a modificar** → Home, Sobre mí, Cursos, fichas de curso, Blog,
  Tienda/Recursos, Contacto, + nueva `/recursos-gratis/`.
- **5. Redirecciones a crear** → ver `01-fase1` §1.5 (duplicados de catálogo → `/cursos/`).
- **6. Páginas a poner en noindex** → ver `01-fase1` §1.3 (técnicas/privadas).
- **7. Cambios en sitemap** → excluir noindex; mantener páginas/cursos/posts/productos a posicionar.
- **8. Mejoras de headings** → ver `01-fase1` §1.1 y `02-fase2`.
- **9. Mejoras de metadatos** → ver `01-fase1` §1.2.
- **10. Mejoras de enlaces internos** → ver `03-fase3` §3.3-3.4 (más a fondo en Fase 7).
- **11. Mejoras de conversión** → ver `02-fase2` (segmentación, autoridad, lead magnet, CTAs).
- **12. Riesgos / pendientes** → confirmar producción/staging; verificar plugin
  SEO, theme/child theme, LMS y slugs reales; las **⚠️ VERIFICAR** del informe.
- **13. Próximos pasos** → segunda tanda: Fase 4 (pilares `/signos-para-bebes/`
  y `/sistema-bimodal/`), Fase 5 (landings de curso), Fases 6-9 (blog, enlazado,
  schema, conversión/footer), Fase 10 (verificación). Y, si te interesa que lo
  aplique yo: activar plan Jetpack + abilities MCP.

---

## RECORDATORIO DE SEGURIDAD
- No borres páginas ni productos: solo noindex donde corresponda.
- No toques checkout, carrito, cuenta, login ni acceso a cursos.
- Aplica primero en staging si existe; copia de seguridad si vas a producción.
- Cambios delicados (noindex/301) de uno en uno, verificando cada paso.
