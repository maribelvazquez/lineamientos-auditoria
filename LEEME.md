# Mapa de Lineamientos de Auditoría PLD

App de estudio de 360Educa (GMC360) para Módulo 3 · Certificación CNBV PLD/FT.
Ruta: Sector financiero. Armada el 16/09/2026.

Fuente: Lineamientos para la elaboración del informe de auditoría para evaluar el cumplimiento de las disposiciones de carácter general en materia de PLD/FT, CNBV, DOF 18 de octubre de 2021 (abrogan los del 19 de enero de 2017).

## Qué hay en esta carpeta

- `index.html` — la app completa: mapa mental, Modo recitar, trampas, cifras y simulador con los reactivos. Al terminar una ronda o simulacro, el alumno puede imprimir o guardar en PDF su resultado y las preguntas que falló, con la respuesta y su fundamento. No necesita ningún otro archivo, base de datos ni clave de API; funciona en cualquier navegador.
- `LEEME.md` — este archivo.

Secciones de la app: Los 12, Octavo A: las 14, Octavo B·C·D, Cifras, Practicar ▸.

Banco de reactivos: 245 de opción múltiple (4 opciones), verificados contra el texto oficial:
  - Lineamientos 1–7 y 9–12: 85
  - OCTAVO A · fracciones: 124
  - OCTAVO B, C y D: 36

## Cómo publicarla

**Netlify, sin GitHub:** entra a app.netlify.com/drop y arrastra la carpeta que contiene `index.html`.

**GitHub + Netlify:**
1. Crea un repositorio (sugerido: `mapa-lineamientos`) y sube `index.html` a la raíz.
2. En Netlify: Add new site → Import from GitHub → elige el repositorio. Deja vacíos «Build command» y «Publish directory».
3. Cada vez que se reemplace `index.html` en el repositorio, Netlify publica la versión nueva sola.

## Cómo corregirla o actualizarla

- **No se edita `index.html` a mano.** Se arma a partir de:
  - la plantilla «Plantilla Mapa Interactivo 360Educa» (artifact en la cuenta de Claude de Maribel Vázquez; respaldo en Drive → 2. ACADEMIA 2026 / 00. METODO Y PLANTILLAS);
  - un archivo de datos (`datos.json`), guardado en el proyecto de Claude del curso.
- **Para cambiar un texto, un reactivo o los colores:** en Claude, con la skill **mapa-norma-360educa**, se corrige el `datos.json` y se vuelve a armar con `construir_app.py`.
- **Si cambia la norma** (reforma), hay que revisar el mapa y el banco contra el texto nuevo antes de volver a publicar.

## Aviso

Material didáctico: los textos están resumidos y no sustituyen la publicación oficial ni son asesoría para un caso concreto.
Progreso de los alumnos: el simulador lo guarda sólo en su propio navegador (clave `lin2021`); no se envía a ningún servidor.
