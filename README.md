# Portafolio — Randy Leandro Cabrera

Portafolio personal: desarrollador backend y full-stack. Sitio estático de un solo archivo, sin dependencias ni build.

**En vivo:** https://randycabrera.vercel.app

## Stack

HTML + CSS + JavaScript puro. Sin framework, sin `node_modules`, sin paso de compilación — se sirve tal cual.

## Estructura

```
index.html          Todo el sitio (estilos, marcado y lógica)
assets/
  ├── *.jpg         Imágenes de portada de cada proyecto
  ├── avatar.svg    Monograma del hero
  ├── favicon.svg   Icono de pestaña
  └── og.jpg        Previsualización para redes sociales
```

## Desarrollo local

```bash
python3 -m http.server 8000
# abrir http://localhost:8000
```

## Cómo editar el contenido

Todo el contenido vive en dos arreglos al final de `index.html`:

- **`SKILLS`** — cada objeto es una tarjeta de habilidad (`name`, `pct`, `desc`, `color`, `cat`).
- **`PROJECTS`** — cada objeto es una tarjeta de proyecto. Los campos que más se editan:
  - `image` — ruta a la portada en `assets/`
  - `title`, `desc`, `longDesc` — textos de la tarjeta y del modal
  - `howItWorks`, `concepts`, `tags` — listas del modal
  - `cat` — filtro al que pertenece (`fullstack`, `web`, `csharp`)
  - `cls: 'span2'` — hace que la tarjeta ocupe dos columnas

Para agregar un proyecto, copia un objeto de `PROJECTS`, cámbiale el `id` y añade su imagen a `assets/`.

## Foto del hero

El hero usa `assets/foto.jpg` (256×256). Para cambiarla, sustituye ese archivo por otra
imagen cuadrada; se recorta en círculo, así que conviene que la cara quede centrada.

Se incluye también `assets/avatar.svg`, un monograma "RC" como alternativa sin foto:
basta cambiar el `src` del `<img class="hero-avatar">` en `index.html`.

## Despliegue

Cualquier hosting estático. En Vercel se detecta solo — sin configuración.

> Si el dominio final no es `randycabrera.vercel.app`, actualiza las etiquetas
> `og:url`, `og:image` y `canonical` en el `<head>` para que la previsualización
> en redes sociales funcione.

## Imágenes

Fotografías de [StockSnap.io](https://stocksnap.io) bajo licencia **CC0** (dominio público, uso libre sin atribución). Ver [`CREDITS.md`](CREDITS.md).
