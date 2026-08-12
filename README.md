# Brasería El Tango — web

Sitio de una sola página (`index.html`) para el restaurante Brasería El Tango.

## Reemplazar las fotos

Todas las imágenes están en `/images` con nombres fijos y de marcador de posición.
Sustituye cada archivo por tu foto real **manteniendo el mismo nombre** (o cambia el `src` en `index.html` si prefieres otros nombres):

| Archivo | Dónde se usa | Tamaño recomendado |
|---|---|---|
| `images/hero-bg.webp` | Fondo de la portada | 1920×1080 (horizontal, oscura o se puede oscurecer) |
| `images/historia.webp` | Sección "Nuestra historia" | 900×1125 (vertical, retrato) |
| `images/ambiente-parrilla.webp` | Bloque grande de "Ambiente" | 900×1000 |
| `images/ambiente-sala.webp` | Bloque "Sala principal" | 700×480 |
| `images/ambiente-barra.webp` | Bloque "Barra de vinos" | 700×480 |
| `images/ambiente-terraza.webp` | Bloque "Terraza" | 700×480 |
| `images/ambiente-sobremesa.webp` | Bloque "Sobremesa" | 700×480 |
| `images/og-image.webp` | Vista previa al compartir el enlace (WhatsApp, redes) | 1200×630 |

Formato `.webp` (ligero y rápido para web, < 300 KB cada una ideal). Puedes convertir cualquier foto a `.webp` en [squoosh.app](https://squoosh.app) o con `cwebp foto.jpg -o foto.webp`.

> Nota: algunas apps de mensajería (WhatsApp, iMessage) todavía no generan vista previa de enlaces con `.webp` como `og:image`. Si ves que la vista previa al compartir el link no aparece, cambia solo `images/og-image.webp` a `.jpg` y actualiza esa línea en el `<head>` de `index.html`.

## Datos a revisar en `index.html`

- Número de WhatsApp: busca `34600000000` (aparece dos veces) y cámbialo por el real.
- Dirección: `Carrer del Tango, 12 · Barcelona`.
- Horario y teléfono en la sección de reservas.
- Precios y platos de la carta (`<section id="carta">`).

## Subir a GitHub

```bash
cd braseria-el-tango
git init
git add .
git commit -m "Sitio Brasería El Tango"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/braseria-el-tango.git
git push -u origin main
```

## Desplegar en Cloudflare Pages

1. Entra en el dashboard de Cloudflare Pages → **Create a project** → **Connect to Git**.
2. Selecciona el repo `braseria-el-tango`.
3. Build settings: no necesita build (es HTML estático) → framework preset **None**, build command vacío, output directory `/`.
4. Deploy. La web quedará en algo como `braseria-el-tango.pages.dev`.
