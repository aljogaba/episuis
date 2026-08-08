# EPISUIS — sitio estático V1

Sitio web ligero para EPISUIS, construido con HTML, CSS y JavaScript sin WordPress ni dependencias de compilación.

## Estructura

- `index.html` — inicio en español
- `consultoria.html` — consultoría en español
- `sobre.html` — EPISUIS / sobre la consultoría
- `contacto.html` — contacto
- `en/` — versión inglesa equivalente
- `assets/css/style.css` — sistema visual completo
- `assets/js/main.js` — navegación, animaciones y formulario
- `assets/images/identity/` — logo y favicon
- `assets/images/visuals/` — visuales vectoriales propios
- `robots.txt` y `sitemap.xml` — SEO técnico básico

## Publicación en GitHub Pages

1. Crear o usar un repositorio para EPISUIS.
2. Copiar el contenido de esta carpeta a la raíz del repositorio.
3. Commit + Push.
4. En GitHub: Settings → Pages → Deploy from a branch → `main` / root.
5. Revisar primero la URL de GitHub Pages antes de cambiar el dominio `episuis.com.mx`.

No se incluye `CNAME` todavía para evitar apuntar el dominio antes de validar el sitio.

## Formulario de contacto

El formulario está diseñado para captar un primer contacto institucional sin pedir información sanitaria confidencial. En esta V1, si no se configura un endpoint, el botón abre un correo dirigido a `episuis@gmail.com` con los campos ya acomodados.

Para producción conviene conectar un servicio de formularios estáticos (por ejemplo Formspree o equivalente). El código ya está preparado: basta con colocar el endpoint en el atributo `data-endpoint` de los formularios en `index.html`, `contacto.html`, `en/index.html` y `en/contact.html`.

Ejemplo:

```html
<form data-contact-form data-endpoint="https://formspree.io/f/XXXXXXXX">
```

## Identidad visual

Dirección: **red epidemiológica + laboratorio de soluciones**, con elementos de cartografía del riesgo.

Paleta base:

- Verde epidemiológico: `#0F3D36`
- Rosa EPISUIS: `#E6AAAA`
- Marrón profundo: `#662112`
- Grafito: `#4D4D4D`
- Fondo cálido: `#F6F3EE`
- Verde suave: `#E8EEE9`

Los SVG de `assets/images/visuals/` son propios del sitio y pueden editarse como texto.

## Idiomas e internacionalización

La raíz es español (`es-MX`) y `en/` contiene la versión inglesa. Se incluyen `canonical`, `hreflang` y sitemap bilingüe para mantener una base SEO internacional correcta.
