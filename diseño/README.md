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

_Pendiente: ¿qué ha sido más rápido?, ¿qué HTML se lee mejor?, ¿qué haríais si hubiera que cambiar el color principal en todas las pantallas?_

## Validación del CSS (fase 4)

_Pendiente: captura en `img/validacion.png`._