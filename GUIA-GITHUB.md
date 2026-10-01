# Publicar en GitHub Pages — PolTaugourdeau/Porfolio-Page

## Qué fallaba
- GitHub Pages (Jekyll) **ignora carpetas y archivos que empiezan por `_`** → `_ds/styles.css` no se servía: sin estilos ni fuente Inter.
- Nombres con espacios (`Pol Taugourdeau Portfolio v2.dc.html`, `3ds Max.png`, `After Effects.png`).

## Qué se ha cambiado
- Estilos ahora en `ds/styles.css` y `ds/ds-bundle.js` (sin guion bajo) + archivo `.nojekyll`.
- Página principal renombrada a `portfolio.dc.html`; `index.html` redirige a ella.
- Inter cargada desde Google Fonts en el `<head>`.
- Iconos renombrados: `3ds-max.png`, `after-effects.png`. Todas las rutas son relativas (`uploads/imagenes/...`).

## Cómo subirlo
1. En el repo: borra todo lo que hay (o crea el repo nuevo).
2. Descarga este proyecto, descomprime y sube **el contenido** con GitHub Desktop (recomendado: así sube también `.nojekyll`, que es un archivo oculto).
3. Añade tú:
   - `models/car.zip` (FBX + carpetas UV_01…UV_09, texturas a 2K, < 100 MB)
   - `videos/reel.mp4` (< 100 MB)
   Respeta las minúsculas exactamente.
4. Settings → Pages → Deploy from a branch → `main` / `(root)`.
5. Web: `https://poltaugourdeau.github.io/Porfolio-Page/`

Si al cambiar algo no ves el cambio: Ctrl+F5 (la caché de Pages tarda ~1 min).
