# Content Studio

Plataforma para organizar y crear contenido de Instagram, YouTube y Stories (BMEDIA).

- Vistas: Board, Lista, Calendario y Dashboard
- Pilares de contenido, etiquetas y propiedades personalizadas
- Comentarios en tareas, importacion desde Asana
- Temas: claro, oscuro y Marca
- Login por usuario con Supabase (cada usuario ve solo sus datos)
- Instalable en el celular (PWA)

## Estructura

| Archivo | Que es |
|---|---|
| `index.html` | La app completa |
| `config.js` | URL y clave publica del proyecto Supabase "Content Studio" |
| `sw.js` | Service worker (funciona offline) |
| `manifest.json`, `icon-*.png` | Datos para instalar la app |

Es un sitio estatico: no necesita build. En Vercel elige "Other" como framework y deja vacio el comando de build.

La clave de `config.js` es la clave publica (publishable) de Supabase; esta pensada para ir en el navegador. Los datos estan protegidos con Row Level Security en la tabla `content_studio`.
