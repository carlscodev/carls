# carls

Página y descargas de **carls**, el agente de código que corre en tu máquina.

- `index.html` — la página (HTML autocontenido, sin dependencias externas)
- `version.json` — el feed que consulta la app de escritorio para avisar de una versión nueva
- `assets/` — capturas reales de la app

Los binarios viven en [Releases](https://github.com/carlscodev/carls/releases). No se publica código
fuente: sólo programas compilados.

## Servir en local

```bash
python -m http.server 8099 --directory .
```

## Actualizar una versión

1. Subir los binarios al release `vX.Y.Z` de este repositorio.
2. Actualizar `version.json` (`version`, `url`, `notes`) y los enlaces de descarga del `index.html`.
3. La app de escritorio compara su versión con `version.json` y muestra el aviso; no se actualiza sola.

## Publicación

GitHub Pages, rama `main`, raíz del repositorio. `.nojekyll` evita que Pages procese los archivos.
