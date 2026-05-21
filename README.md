# Cenident · Demo de revisión privado

Demo HTML del producto Cenident para revisión y aprobación de diseño antes de codificar la versión final.

## Acceso

**URL:** [https://kenedytorcatt.github.io/cenident-demo/](https://kenedytorcatt.github.io/cenident-demo/)

**Clave:** se entrega por WhatsApp al revisor autorizado.

> Este sitio no se indexa en buscadores (`noindex` + `robots.txt`). Solo accede quien tenga el link + la clave.

## Qué probar

El demo tiene 4 vistas internas (navegan sin recargar):

| Vista | Qué incluye |
|---|---|
| **Inicio** | Hero + 3 cards a las pantallas + recorrido sugerido + 6 preguntas de evaluación |
| **Wizard** | Onboarding 8 pasos: clínica, plan SaaS, sucursales, equipo, sillones, servicios + precios, métodos de pago |
| **App** | App principal: 5 roles, timeline 8 pasos, odontograma 32 piezas, kanban drag&drop, 3D rotable, chat de equipo |
| **Academia** | Catálogo LMS estilo Netflix con carruseles auto-scroll |

## Cómo dar feedback

3 formas, la que prefieras:

1. **Botón "Enviar feedback"** dentro del demo (abajo-derecha) → copia tu opinión al portapapeles para pegar en WhatsApp
2. **GitHub Issues** → [Crear feedback aquí](https://github.com/kenedytorcatt/cenident-demo/issues/new/choose) (queda registrado y se asigna a quien corresponda)
3. **WhatsApp directo** al equipo

## Historial de versiones

Cada cambio queda anotado en [CHANGELOG.md](CHANGELOG.md) con fecha y motivo. Las versiones anteriores quedan en los releases del repo.

## Notas

- Esto es un **mockup navegable**, no es el producto final. Algunas interacciones son visuales (botones que no hacen nada todavía).
- El producto real se construirá en Next.js + Go + PostgreSQL una vez aprobado el diseño.
- Light mode por defecto, dark mode disponible con el switch arriba.
- Funciona 100% sin internet (excepto el modelo 3D que carga de Sketchfab).
