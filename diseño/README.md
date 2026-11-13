# Aura Farmers · Diseño de la interfaz (P1)

Web de minijuegos con humor sobre el «farmeo de aura». Cada jugador tiene un personaje y una moneda, el aura, que gana jugando y gasta en mejorar su personaje.

## Mapa de navegación

```
index.html (Bienvenida)
   │  «Entrar con Google»
   ▼
apodo.html (Primer acceso)
   │  «Empezar a farmear»
   ▼
lobby.html (Lobby) ◄──────────────┐
   │                              │
   ├── menú ──► tienda.html       │  (el menú está en todas las
   ├── menú ──► personaje.html    │   pantallas salvo las dos primeras
   └── menú ──► configuracion.html┘   y siempre lleva al resto)

configuracion.html
   ├── «Cerrar sesión»     ──► index.html
   └── «Borrar mi cuenta»  ──► index.html
```

| Desde | Va a |
|---|---|
| index.html | apodo.html |
| apodo.html | lobby.html |
| lobby.html | tienda.html, personaje.html, configuracion.html |
| tienda.html | lobby.html, personaje.html, configuracion.html |
| personaje.html | lobby.html, tienda.html, configuracion.html |
| configuracion.html | lobby.html, tienda.html, personaje.html, index.html |

## Comparación con Tailwind (fase 3)

Pantalla rehecha: `tienda-tailwind.html` (Tailwind 4 desde CDN, sin `estilos.css`).

**¿Qué ha sido más rápido?**
_Escribe aquí tu experiencia: cuánto tardaste con cada método, qué te frenó..._

**¿Qué HTML se lee mejor?**
_Compara una tarjeta de `tienda.html` (clases BEM) con la de `tienda-tailwind.html` (clases de utilidad)..._

**¿Qué haríais si hubiera que cambiar el color principal en todas las pantallas?**
_Pista para pensar: en `estilos.css` hay una variable en `:root`; en el HTML con Tailwind, mira dónde están definidos los colores y cuántos archivos habría que tocar..._

## Sass (fase 4)

- Los estilos están en `scss/`, repartidos en parciales (`_variables`, `_mixins`, `_tema`, `_base`, `_logo`, `_barra`, `_menu`, `_contenido`, `_tarjetas`, `_botones`, `_formularios`, `_avisos`, `_personaje`, `_portada`) y reunidos con `@use` en `estilos.scss`.
- Live Sass Compiler genera `css/estilos.css` (configuración en `.vscode/settings.json`). **No se edita a mano.**
- **Variables**: paletas `$oscuro` y `$claro`, fuentes, radio y puntos de corte en `_variables.scss`.
- **Anidamiento**: el BEM se escribe con `&__elemento` y `&--modificador`.
- **Mixin**: `boton($fondo, $texto)` lo usan todos los botones; `desde($ancho)` para las media queries.
- **Tema alternativo**: el tema oscuro es el de origen y el claro se activa con `@media (prefers-color-scheme: light)`, que solo cambia las variables de color de `:root`.

## Validación del CSS (fase 4)

_Pendiente: pasar `css/estilos.css` por el validador del W3C, guardar la captura en `img/validacion.png` y enlazarla aquí con `![Validación del CSS](img/validacion.png)`._


_Pendiente: captura en `img/validacion.png`._
