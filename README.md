# Calzada Research Group website

Sitio web del Calzada Research Group (Department of Geography and Environmental Studies, New Mexico State University), hecho con [Quarto](https://quarto.org/) y publicado en GitHub Pages.

## Cómo editar sin programar (panel de administración)

1. Entra a <https://app.pagescms.org> e inicia sesión con tu cuenta de GitHub.
2. Elige este repositorio. En el menú verás:
   - **News & talks**: noticias y charlas. Una entrada por noticia, con categoría, foto opcional y texto.
   - **Publications**: pega el BibTeX (de Google Scholar, Zotero o la revista). El tipo (artículo, capítulo, reporte…) sale del BibTeX; el menú *Type* lo cambia si hace falta.
   - **Research projects**: proyectos con foto o color de tarjeta.
   - **People**: integrantes, vacantes y exalumnos, con foto.
   - **Page text: …**: todos los textos de cada página (títulos, introducciones, secciones, números de la portada).
3. Presiona **Save**. El sitio se vuelve a publicar solo en uno o dos minutos.

Las fotos se suben desde el mismo panel y quedan en `assets/img/`.

## Dónde vive cada cosa

| Qué | Archivo |
|---|---|
| Textos de la portada | `data/home.yml` |
| Textos de las demás páginas | `data/pages/*.yml` |
| Proyectos de investigación | `data/research.yml` |
| Equipo y vacantes | `data/people.yml` |
| Publicaciones (BibTeX o campos) | `data/publications.yml` |
| Noticias y charlas | `news/*.qmd` |
| Colores y tipografía | `assets/lab.scss`, `assets/extra.css` |
| Diseño de cada sección | `_templates/*.ejs` |

## Vista previa local

```bash
quarto preview
```

## Publicación

Cada cambio en `main` ejecuta `.github/workflows/publish.yml`, que renderiza el sitio y lo publica en GitHub Pages. Una sola vez hay que ir a **Settings → Pages** y elegir **Source: GitHub Actions**.
