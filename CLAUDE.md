# CLAUDE.md

Este archivo proporciona contexto a Claude Code (claude.ai/code) para trabajar en este repositorio.

## Qué es este repositorio

Repositorio personal de seguimiento del **Curso de Especialización en Big Data e Inteligencia Artificial para FP**, impartido por **Digitech**, curso lectivo **2026/2027**. Su propósito es almacenar, organizar y documentar en español todo el material generado o estudiado durante el curso: apuntes de asignaturas, cursos complementarios y proyectos.

Todo el contenido debe redactarse **siempre en español**, con texto enriquecido (Markdown), de forma clara, concisa y detallada.

## Estructura de directorios

El repositorio se organiza en tres carpetas de primer nivel:

- **`asignaturas/`** — Información y documentación de las asignaturas del curso oficial. Un subdirectorio por asignatura.
- **`cursos/`** — Cursos adicionales, tanto previos al curso lectivo como los realizados durante el mismo (p. ej. certificaciones, MOOCs, cursos de terceros). Un subdirectorio por curso.
- **`proyectos/`** — Proyectos desarrollados durante el curso. Un subdirectorio por proyecto/curso al que pertenezcan.

## Convención de subdirectorios (asignaturas y cursos)

Cada subdirectorio de asignatura o curso que tenga documentación generada a partir de material en bruto (transcripciones, apuntes en txt, etc.) sigue esta estructura interna:

```
<asignatura-o-curso>/
├── 00-indice.md          # Índice general + introducción/resumen del temario
├── cap1.md, cap2.md...   # Documentos Markdown, uno por capítulo o sección
├── raw/                  # Material original en crudo usado como fuente (cualquier formato)
│   ├── cap1.txt
│   └── ...
├── diagrams/             # Diagramas y esquemas de apoyo (.svg)
│   └── capN-descripcion.svg
└── other_formats/        # Versión completa del temario en otros formatos
    ├── Nombre-Curso-Completo.pdf
    └── Nombre-Curso-Completo.epub
```

Reglas clave:

- Los archivos en `raw/` son la fuente original y **no se editan**: la documentación Markdown se genera/deriva a partir de ellos. Pueden estar en cualquier formato (`.txt`, `.pdf`, `.docx`, transcripciones de audio/vídeo, capturas, etc.), no solo texto plano.
- Si el contenido se organiza por capítulos o secciones, debe existir un `.md` principal (p. ej. `00-indice.md`) con el índice y una introducción/resumen de la asignatura o curso, enlazando a cada capítulo.
- Cada capítulo es un documento Markdown autocontenido: conserva la información técnica original (ejemplos, comandos, definiciones) y añade formato enriquecido — encabezados, negritas en términos clave, bloques de código, tablas — y, cuando ayude a la comprensión, un resumen de puntos clave al final.
- Siempre que aporte claridad, incluir diagramas, esquemas o ilustraciones de apoyo en **SVG** (preferente, en `diagrams/`), PNG o arte ASCII embebido en el propio Markdown.
- `other_formats/` contiene el temario completo compilado en **PDF** y **EPUB**, generado a partir de los Markdown.
- Ver [cursos/fundamentos-linux/](cursos/fundamentos-linux/) como ejemplo de referencia de esta convención ya aplicada.

`proyectos/` no sigue necesariamente esta convención de `raw/diagrams/other_formats`, ya que su contenido son proyectos (código, memorias, entregables) y no material transcrito de clases; su estructura interna puede adaptarse a lo que cada proyecto requiera.

## Estilo de la documentación

- Idioma: español, siempre.
- Tono: claro, conciso y detallado; sin relleno ni repeticiones innecesarias.
- Formato: Markdown enriquecido (tablas, listas, bloques de código con el lenguaje indicado, citas cuando proceda).
- Fidelidad: no perder información técnica presente en el material en bruto (`raw/`) al redactar la versión enriquecida.
- Apoyo visual: priorizar diagramas SVG cuando ayuden a entender procesos, jerarquías, arquitecturas o flujos.

## Otras consideraciones

- El `README.md` de la raíz explica el propósito del repositorio, el índice de directorios y un descargo de responsabilidad; debe mantenerse en español y actualizado si cambia la estructura de alto nivel.
- Este es un repositorio personal de apuntes de estudio, no un producto de software: no se generan tests, builds ni pipelines de CI para su contenido.
- **Antes de cada `git push`**, comprobar que el `README.md` de la raíz sigue reflejando el estado actual del repositorio (índice de directorios, asignaturas/cursos/proyectos presentes) y actualizarlo si es necesario.
- **Al hacer `git commit`**, incluir únicamente los ficheros que ya estén en stage (`git add` previo); no añadir automáticamente otros ficheros modificados o sin trackear.
