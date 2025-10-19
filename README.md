# webCapilla — IE Capilla del Rosario

<!-- Badges -->

- ![CI](https://img.shields.io/github/actions/workflow/status/MarlonMedellin/webCapilla/.github/workflows/ci.yml?branch=main&label=CI&logo=github)
- ![Pages](https://img.shields.io/github/actions/workflow/status/MarlonMedellin/webCapilla/.github/workflows/pages.yml?branch=main&label=Pages&logo=github)
- ![Latest Commit](https://img.shields.io/github/commit-activity/m/MarlonMedellin/webCapilla)
- ![License](https://img.shields.io/github/license/MarlonMedellin/webCapilla)

Estado: en desarrollo

Repositorio para el sitio institucional de la Institución Educativa Capilla del Rosario (Medellín).

Este proyecto contiene la versión estática del sitio web: la página principal y recursos asociados. El objetivo es ofrecer información institucional (matrículas, cupos, jornadas, proyectos, circulares y contacto) para la comunidad educativa.

## Contenido principal del repositorio

- `index.html` — Página principal del sitio (sitio estático responsable de la mayor parte del contenido visible).
- `head_snippet.txt` — Fragmento HTML/CSS/metadata usado en el head (meta tags, estilos y enlaces a fuentes/CDN).
- `Agentes/ajustes.md` — Instrucciones y tareas de ajuste para actualizar la web (guía interna).
- `Agentes/contenido.md` — Plantilla de contenidos (texto base para las secciones que se publicarán).
- `README.md` — Este archivo.

Si tienes más carpetas (por ejemplo `assets/` o `public/`) aparecerán en el árbol del proyecto y contendrán estilos, scripts o imágenes.

## Cómo probar / ver el sitio localmente

El sitio es estático. Para una vista rápida basta con abrir `index.html` en un navegador. Para un servidor local (mejor para rutas relativas y pruebas):

PowerShell (Windows):

```powershell
# 1) Servir desde la carpeta del proyecto (puede requerir Python instalado)
python -m http.server 8000

# 2) Abrir en el navegador
Start-Process "http://localhost:8000/index.html"
```

Alternativas:

- Usar la extensión Live Server de Visual Studio Code.
- Cualquier servidor estático (http-server de npm, páginas GitHub Pages, etc.).

## Dónde editar el contenido

- Contenido y estructura principal: editar `index.html`.
- Fragmentos reutilizables (meta tags, estilos iniciales): `head_snippet.txt`.
- Notas de mantenimiento, ajustes y listas de tareas: `Agentes/ajustes.md`.
- Textos que deben completarse o sustituirse por el equipo: `Agentes/contenido.md`.

Para cambios de contenido frecuentes, lo ideal es mantener textos en archivos Markdown dentro de `Agentes/` y, si se desea, crear un pequeño script que los incluya en `index.html` durante una etapa de build.

## Estructura sugerida (basada en el proyecto actual)

- Banner / Hero
- Horizonte institucional (misión, visión, principios)
- Proceso de matrícula (nuevos / antiguos)
- Cupos / Publicación de aceptados
- Jornadas y niveles
- Proyectos institucionales
- Novedades / Circulares (PDFs)
- Contacto (teléfonos, correos y mapa)

Estas secciones ya aparecen en `index.html` y en los archivos dentro de `Agentes/` como bocetos o instrucciones.

## Contribuir

1. Haz fork del repositorio.
2. Crea una rama con un nombre descriptivo: `git checkout -b feature/mi-cambio`.
3. Haz commits claros y atómicos.
4. Envía un push y abre un Pull Request describiendo los cambios.

Buenas prácticas:

- Mantén los textos en `Agentes/` si son contenido que debe revisarse con el equipo editorial.
- Para assets (imágenes, PDFs) usa una carpeta `assets/` con subcarpetas `img/`, `docs/`, `css/`, `js/`.

## Notas operativas y tareas pendientes

- Revisar y completar los textos en `Agentes/contenido.md` antes de publicar.
- Subir las circulares y documentos oficiales en `assets/docs/` y enlazarlos desde la sección de Circulares.
- Verificar y actualizar los datos de contacto (teléfonos y correos) en `index.html`.

## Contacto

Responsable del repo: Marlon Arcila

Si necesitas que yo (o el equipo) incorpore cambios concretos en el HTML o genere versiones para despliegue (GitHub Pages), indícame qué sección actualizar y lo hago.

---

_README reconstruido automáticamente a partir de la estructura y los archivos actuales del proyecto._
