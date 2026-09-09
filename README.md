# Portafolio · rauuwww.github.io

Sitio personal de Raúl R. Yllescas con los proyectos más relevantes de
[github.com/Rauuwww](https://github.com/Rauuwww). Publicado con GitHub Pages en
**https://rauuwww.github.io**.

## Qué contiene

- `index.html`: toda la página (HTML, CSS y JavaScript en un solo archivo, sin frameworks ni build).
- `assets/img/`: capturas de los proyectos en formato WebP.
- `.nojekyll`: le dice a GitHub Pages que sirva los archivos tal cual.

La página está en español e inglés. Un botón ES/EN en la cabecera cambia el idioma, lo recuerda
en el navegador y también se puede forzar con `?lang=en` en la URL.

## Cómo editar

**Textos.** Cada texto aparece dos veces, uno con clase `es` y otro con clase `en`:

```html
<span class="es">Repositorio</span><span class="en">Repository</span>
```

Edita los dos. Si un texto solo debe aparecer en un idioma, deja solo ese span.

**Añadir un proyecto.** Copia un bloque `<article class="project" id="...">` dentro de la sección
`#proyectos` y cambia:

1. `.media`: una captura (`<div class="shot browser"><img ...></div>`) o un esquema de arquitectura
   (`<div class="arch">` con nodos `.node` y flechas `.arrow`).
2. `h3`, `.client` y el párrafo de descripción.
3. La lista `ul.did` con lo que construiste (3 o 4 puntos).
4. La ficha `dl.sheet` con Stack y Evidencia (commits, periodo, pruebas, documentación).
5. Los enlaces en `.links`.

Para proyectos secundarios, añade un `<article>` en la sección `#otros`.

**Capturas.** Convierte a WebP para que pesen poco, por ejemplo con ffmpeg:

```
ffmpeg -i captura.png -vf scale=1400:-1 -quality 82 assets/img/nombre.webp
```

**Colores y tipografía.** Están en las variables de `:root` al inicio del `<style>`. El tema oscuro
se activa solo según la preferencia del sistema.

## Publicar

```
git add -A
git commit -m "Actualiza portafolio"
git push
```

GitHub Pages publica la rama `main` en uno o dos minutos.
