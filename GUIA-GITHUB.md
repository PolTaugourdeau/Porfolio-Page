# Publicar el portfolio en GitHub Pages

## 1. Prepara tus archivos (en tu PC)
| Archivo | Dónde va | Notas |
|---|---|---|
| `car.zip` | `models/car.zip` | FBX/GLB + carpetas UV_01…UV_09. **Texturas a 2K** para que el zip pese < 100 MB |
| `reel.mp4` | `videos/reel.mp4` | < 100 MB (H.264, 1080p) |

**Reducir texturas a 2K:** en Substance Painter → Export Textures → Size: 2048. (O en Photoshop: Archivo → Automatizar → Lote, tamaño 2048.) El visor ya las baja a 2K, así que no pierdes calidad visible.

## 2. Crea el repositorio
1. Entra en github.com → **New repository** → nombre: `portfolio` → Public → Create.
2. Pulsa **uploading an existing file**.
3. Arrastra **todo el contenido** de la carpeta descargada (no la carpeta en sí): `index.html`, `Pol Taugourdeau Portfolio v2.dc.html`, `car-viewer.html`, `support.js`, `_ds/`, `uploads/`, `models/`, `videos/`.
   - Si arrastrar carpetas falla, usa **GitHub Desktop** (desktop.github.com): clona el repo, copia los archivos dentro, *Commit* y *Push*.
4. Commit changes.

## 3. Activa GitHub Pages
Settings → Pages → Source: **Deploy from a branch** → Branch: `main` / `(root)` → Save.
En 1–2 minutos tu web estará en: `https://TU-USUARIO.github.io/portfolio/`

## 4. Comprueba
- El reel se ve de fondo en la portada.
- "Click to explore in 3D" → sale *Loading F1 model…* → coche con texturas.
- Si el coche no carga: comprueba que el archivo se llama exactamente `models/car.zip` (minúsculas).

## Límites a tener en cuenta
- GitHub: máx. **100 MB por archivo**, recomendable < 1 GB el repo total. Git LFS **no** funciona con GitHub Pages.
- Si tu zip sigue pesando mucho: guarda el normal map en JPG calidad 90, o exporta el modelo como **.glb** con texturas incrustadas desde Blender (suele pesar menos).
