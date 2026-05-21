# Cenident · Demo de revisión privado

Demo HTML interactivo del producto Cenident para revisión y aprobación de diseño antes de codificar en Next.js + Go + PostgreSQL.

**Versión actual:** `v2.1-baseline` · primer demo funcional aprobado. Punto de partida formal sobre el cual se desarrollan los ajustes futuros.

## Acceso

**URL:** [https://kenedytorcatt.github.io/cenident-demo/](https://kenedytorcatt.github.io/cenident-demo/)

**Clave:** se entrega por WhatsApp al revisor autorizado.

> Este sitio no se indexa en buscadores (`noindex` + `robots.txt`). Solo accede quien tenga el link + la clave.

## Estructura del demo

### Web pública (sin login)

| Vista | Qué incluye |
|---|---|
| **Academia** (Inicio) | LMS estilo Netflix · hero con poster anuncio editable · banda de marcas patrocinadoras · 3 carruseles full-bleed auto-scroll con cursos |
| **Precios** | 3 planes (Gratis $0 / Pro $2,900 destacado / Platinum $3,700 con medalla "Mejor opción" dorada) + toggle Mensual/Anual + FAQ |
| **Nosotros** | Stats · Misión / Visión / Valores · equipo |
| **Contacto** | Formulario + sidebar con WhatsApp / Email / Oficina / Horarios |
| **Iniciar sesión** | Modal con email/password → entra al App |

### Vistas internas (post-login)

| Vista | Qué incluye |
|---|---|
| **Wizard de clínica** | 7 pasos: clínica → sucursales → equipo → sillones → servicios + precios → métodos de pago → ¡Listo! |
| **App principal** | Timeline de **8 pasos 100% funcionales**: Llegada · Anamnesis · Exploración (odontograma + 3D) · Plan tratamiento (kanban drag&drop) · Firma plan (WhatsApp) · Cobro (Stripe split) · Ejecución (sesiones) · Próxima cita |

### Para el revisor del demo

Arriba aparece un pill negro **"MODO DEMO"** con atajos para saltar a Wizard / App sin loguearse. En el producto real ese pill no existe.

## Cómo dar feedback

3 formas, la que prefieras:

1. **Botón "Enviar feedback"** dentro del demo (abajo-derecha) → copia tu opinión al portapapeles para pegar en WhatsApp
2. **GitHub Issues** → [Crear feedback aquí](https://github.com/kenedytorcatt/cenident-demo/issues/new/choose) (queda registrado, plantillas: No me gusta / Falta algo / No funciona / Me gusta)
3. **WhatsApp directo** al equipo

## Historial de versiones

Cada cambio queda anotado en [CHANGELOG.md](CHANGELOG.md) con fecha y motivo. Los **releases formales** del demo se publican en [Releases](https://github.com/kenedytorcatt/cenident-demo/releases) — el actual es [v2.1-baseline](https://github.com/kenedytorcatt/cenident-demo/releases/tag/v2.1-baseline).

## Stack técnico del demo

Solo HTML + CSS + JS vanilla. Sin frameworks pesados, sin servidor, sin base de datos.

- Tailwind CSS (CDN)
- Sortable.js (drag & drop estilo Trello)
- Sketchfab (modelo 3D dental real rotable)
- Geist Sans + Geist Mono
- Imágenes Unsplash reales (dentales / clínicas)

## Notas

- Light mode por defecto, dark mode disponible con el switch arriba
- 7 países con recálculo automático de moneda + IVA en vivo (MX / PE / CO / CL / AR / ES / US)
- Funciona offline (excepto Sketchfab 3D y carga inicial de imágenes Unsplash)
- El producto real se construirá en **Next.js 15 + Go + PostgreSQL** respetando exactamente la estructura visual y de flujos aprobada en este demo
