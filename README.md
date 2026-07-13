# Asistente de accesibilidad web para personas con discapacidad visual mediante Inteligencia Artificial

Fuente en LaTeX de una memoria para optar al título de Ingeniero Civil en Informática de la Universidad Técnica Federico Santa María (UTFSM). Actualmente en desarrollo.

## Sobre la memoria

Los lectores de pantalla tradicionales (como JAWS o NVDA) interpretan el DOM de una página web, pero no su contenido visual: imágenes, gráficos, captchas o la estructura espacial de un sitio quedan fuera de su alcance. Esta memoria propone y valida un prototipo que, a partir de capturas de pantalla de un sitio web, usa un modelo de visión y lenguaje (VLM) para interpretar ese contenido visual y comunicarlo por voz, como complemento a los lectores de pantalla existentes.

La metodología de trabajo sigue cuatro etapas: una encuesta a personas con discapacidad visual para levantar y validar el problema, el desarrollo de un prototipo funcional, un benchmark para seleccionar el modelo VLM más adecuado, y una validación final con usuarios reales.

## Contenido del repositorio

El documento se compila a partir de `main.tex`, que incluye un archivo por capítulo:

| Archivo | Contenido |
|---|---|
| `main.tex` | Preámbulo, portada, resumen y palabras clave |
| `000_portadas.tex` | Portadas |
| `100_glosario.tex` | Glosario de siglas |
| `200_introduccion.tex` | Introducción |
| `300_definicion_del_problema.tex` | Capítulo 1 — Definición del problema |
| `400_marco_conceptual.tex` | Capítulo 2 — Marco conceptual |
| `500_propuesta_de_solucion.tex` | Capítulo 3 — Propuesta de solución |
| `600_validacion_de_la_solucion.tex` | Capítulo 4 — Validación de la solución |
| `700_conclusiones.tex` | Conclusiones |
| `800_anexos.tex` | Anexos |
| `bibliografia.bib` | Referencias bibliográficas (BibTeX) |

Este es un fork de [autopawn/tex-thesis-template](https://github.com/autopawn/tex-thesis-template), la planilla LaTeX estándar usada para memorias de título en el Departamento de Informática de la UTFSM.

## Compilación

Requiere `xelatex` (no `pdflatex`, por el uso de fuentes del sistema vía `fontspec`) y `bibtex`. Los siguientes paquetes se deben instalar para compilar el documento, al menos en `Fedora`:

```
texlive
texlive-latex
texlive-amsmath
texlive-xetex
texlive-bibtex

texlive-babel-spanish
texlive-hyphen-spanish
texlive-fontspec
texlive-anyfontsize
texlive-titlesec
texlive-lastpage
texlive-tocloft
texlive-float
texlive-koma-script
```

En Windows, una alternativa es instalar [MiKTeX](https://miktex.org/), que resuelve los paquetes faltantes automáticamente.

Con los requisitos instalados, se puede compilar con:

```
make document
```

Que ejecuta `xelatex -> bibtex -> xelatex -> xelatex` (varias pasadas son necesarias para que numeración de páginas, tabla de contenidos y bibliografía queden correctas).

## Fuente tipográfica

La fuente principal es `Calibri`. En Windows suele venir preinstalada; en otros sistemas se puede usar la alternativa libre y métricamente compatible `Carlito` (reemplazando las referencias a `Calibri` por `Carlito` en `main.tex`), descargable desde [fontlibrary.org](https://fontlibrary.org/en/font/carlito).
