# Historial de versiones del demo

Cada entrada describe qué cambió, por qué, y la fecha. Lo más reciente arriba.

---

## v1.5 · 2026-05-21

**Fix layout wizard plan activo + nombre plan.**

- Badge "ACTIVO" se montaba encima del título "PLAN CONTRATADO". Ahora el badge va en una barra superior dedicada al lado del eyebrow, sin solaparse
- Plan del wizard renombrado de "Más vendido" → "**Plan Pro**" (más limpio y directo)
- El nombre "Mejor opción" se reserva para el plan Platinum en la página de precios pre-pago (no aplica al wizard porque ahí el usuario ya pagó)

---

## v1.4 · 2026-05-21

**Pulido + lógica de wizard corregida.**

### Quitado
- **Buscador ⌘K del topbar global**: distraía sin aportar valor en esta versión del demo. (El atajo Ctrl+K sigue funcionando si alguien lo usa, pero el botón visible se eliminó)

### Wizard step 2 · rediseñado con lógica real de negocio
- **Antes**: pedía elegir entre Free / Pro / Platinum con precios (incorrecto: el usuario ya pagó antes de entrar al wizard)
- **Ahora**: muestra "Tu plan está activo" + card grande con borde azul + badge "ACTIVO" verde arriba derecha + nombre del plan + precio + próximo cobro + lista de features con check verde + botones "Cambiar de plan" y "Descargar factura"
- Se eliminó el toggle Mensual/Anual del wizard (también pertenece a la página de precios pre-pago)

### Nombres y precios actualizados (para landing page futura, no wizard)
- Free → **Gratis**
- Pro → **Más vendido** · $2,900/mes
- Platinum → **Mejor opción** · $3,700/mes
- Quitado el badge "MÁS POPULAR" del medio (la jerarquía ahora la marca el nombre)

### Cache-bust agresivo
- URL del demo ahora incluye `?b=v13-<timestamp>` para esquivar el cache CDN de Fastly de GitHub Pages
- Headers no-cache en meta tags

---

## v1.3 · 2026-05-21

**Hero LMS rediseñado completo + sin ratings + banda de marcas.**

### Quitado
- **Ratings y estrellitas de los cursos**: comparar doctores entre sí por estrellas perjudica al que ranquea bajo, y eso no es justo. Reemplazado por "24 lecciones · 8h 42m" (información útil, no comparativa)
- **Bestseller rojo Netflix**: cambiado a "DESTACADO" en azul brand. Más neutral, no jerarquiza doctores
- Estrellitas del hero stats bar (era "4.9★ RATING PROMEDIO" → ahora "4K PRODUCCIÓN")

### Hero LMS · split nuevo
- **Izquierda**: texto premium grande (52px) "Aprende de los mejores odontólogos del mundo", subtítulo, meta en una línea, 2 CTAs grandes ("Ver catálogo completo" gradient azul + "Para clínicas" outlined)
- **Derecha**: poster de anuncio editable real (4:3), con imagen de fondo, etiqueta "ESPACIO PATROCINADO · EDITABLE" arriba izquierda, marca del patrocinador (ej. 3M ESPE) arriba derecha, título overlay grande abajo con CTA. Click → toast "Espacio publicitario editable". Hover → lift + shadow
- Quitado el background-image full-bleed del hero (cubría todo y se veía pesado). Ahora hero es claro con gradient sutil radial brand+purple y el poster con la foto va a la derecha

### Banda de marcas patrocinadoras (nuevo)
- Entre el hero y los carruseles, una banda con label "CON EL RESPALDO DE" + 7 marcas dentales (3M ESPE, Ivoclar, Straumann, Henry Schein, GC Dental, Dentsply Sirona, Nobel Biocare)
- Estilo grayscale por defecto, color al hover (efecto Apple/Vercel)
- Llena el espacio vacío entre hero y cursos

---

## v1.2 · 2026-05-21

**Rediseño Academia + Home estilo Netflix premium.**

### Academia (LMS)
- **Hero**: ya no es un "trailer" con play. Ahora es un **banner publicitario tipo poster Netflix** con imagen de fondo real (Unsplash), etiqueta "Patrocinado por marca" (ej. 3M ESPE), título grande estilo cinematográfico, meta info en una línea horizontal y dos CTAs ("Ver tráiler" + "Más información") al estilo Netflix originals. La label "ANUNCIO DESTACADO · EDITABLE" arriba a la derecha deja claro que es un espacio publicitario editable
- **Stats bar** ahora va flotando bajo el hero (no embebido dentro)
- **Carruseles full-bleed**: van de borde a borde de la pantalla (no contenidos en una caja). Eliminado el `mask-image` con degradado en los costados que se veía cortado y barato
- **Thumbnails de cursos**: ya no son gradients morados planos. Ahora son **fotos reales dentales/clínicas (Unsplash)** distintas por curso, con el título overlay en blanco sobre la imagen (estilo Netflix card)
- Tag "BESTSELLER" cambió a rojo Netflix (`#e50914`) para más contraste
- Cards más limpias: sin línea de título debajo, el título está sobre la foto

### Home
- **Hero rediseñado tipo Netflix**: imagen de fondo de impacto + degradado lateral oscuro + texto a la izquierda (ya no centrado)
- Eyebrow ahora con backdrop-blur sobre la imagen
- Stats con glassmorphism sobre la imagen
- Cards de Inicio (Wizard / App / LMS) ahora con **imágenes Unsplash de fondo** + gradient azul/morado por categoría + icono glass flotante abajo-derecha

### Curvas / border-radius
- Reducido el border-radius global de cards, modales, botones (era 14-18px → ahora 8-10px). Se veía "infantil/redondeado" como observado. Ahora más cuadrado tipo Apple/Linear
- Botones: 9px → 6px
- Cards: 14px → 10px
- Modales: 16px → 10px
- Cat-chips: 999px → 6px

---

## v1.1 · 2026-05-21

**Pulido de detalles del wizard.**

### Arreglado
- **Hero gradient del wizard**: ya no se ve cortado. Texto e icono ahora están centrados verticalmente, padding consistente, gradient con más profundidad (3 capas radial + degradado base más rico)
- **Toggle Mensual / Anual**: el badge "−16%" ya no se sale del botón. Padding ajustado, sombras más limpias, gradient azul en el botón activo
- **Badge "POPULAR"**: ya no se ve cortado por encima de la card. Movido al centro superior del plan Pro, con sombra azul más fuerte e inner highlight, cambiado el texto a "MÁS POPULAR" para claridad. Las cards ahora tienen `overflow: visible` con un elemento separado para el glow

---

## v1.0 · 2026-05-21

**Primera versión navegable consolidada.**

### Nuevo
- 1 solo archivo HTML con 4 vistas internas navegables sin recargar
- Vista **Inicio**: hero + 3 cards (Wizard / App / Academia) + recorrido sugerido + 6 preguntas de evaluación + FAB de feedback
- Vista **Wizard**: onboarding 8 pasos · clínica / plan SaaS / sucursales / equipo / sillones / servicios + precios / métodos de pago / listo
  - Cada paso tiene visual hero gradient azul/púrpura premium
  - Cards de planes con check animado al seleccionar
  - Toggle mensual / anual con badge "−16%"
  - Servicios con precios editables en vivo
- Vista **App**: app principal de la clínica
  - 5 roles (Recepción / Asistente / Odontólogo / Admin / Paciente)
  - Timeline horizontal de 8 pasos bloqueables
  - Odontograma anatómico FDI con 32 piezas y 5 superficies
  - Modal con modelo 3D real rotable
  - Kanban drag & drop con 4 columnas (Ideal / Aceptado / Ejecución / Rechazado)
  - Cálculo en vivo del plan: subtotal + IVA del país + 40% hoy
  - Chat lateral de equipo
- Vista **Academia**: LMS estilo Netflix
  - Hero trailer 16:9 cinemático
  - 3 carruseles auto-scroll con pause al pasar mouse
  - 8 cursos demo con instructores, ratings, precios
- Topbar global persistente: nav 4 botones + ⌘K búsqueda + selector país 7 (MX/PE/CO/CL/AR/ES/US) que recalcula moneda + IVA en vivo + dark/light toggle
- FAB de feedback que copia al portapapeles para pegar en WhatsApp
- Tonalidad de copy en **español latino neutro / mexicano** (no argentino)

### Decisiones de diseño cerradas
- Tipografía: Geist Sans + Geist Mono (cero italic, cero serif)
- Color brand: azul eléctrico `#3b6cff` light · `#5b6ff5` dark
- Light mode por defecto, dark visible
- Drag & drop con Sortable.js (estilo Trello, no HTML5 nativo)
- 3D dental: Sketchfab embed (en producción será modelo brandeado propio)

### Pendiente para versión Next.js (no aplica al demo)
- Chat lateral con WebSocket real
- Contenido distinto por rol (datos filtrados desde backend)
- Videos tutoriales reales (botones "?" abren ahora un placeholder)
- Persistencia del wizard al cambiar paso
- Recálculo real del toggle mensual / anual
- Pantallas adicionales: Agenda multi-doctor · Cobros · Reportes · ERP · Panel LMS del doctor productor
