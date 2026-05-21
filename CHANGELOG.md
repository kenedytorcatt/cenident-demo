# Historial de versiones del demo

Cada entrada describe qué cambió, por qué, y la fecha. Lo más reciente arriba.

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
