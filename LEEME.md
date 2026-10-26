# Pruebas automáticas de Cilia

Verifican que los cambios nuevos no rompan lo que ya funcionaba. Cuando cambies algo en `index.html`, corre las pruebas antes de publicar.

## Cómo correrlas
1. Instala Node.js (https://nodejs.org, versión LTS). Solo se hace una vez.
2. Guarda esta carpeta `pruebas` junto a tu `index.html`, dentro del repositorio.
3. Abre una terminal en la carpeta del repositorio y escribe:

    node pruebas/pruebas_cilia.js

   (Para ver también las pruebas que pasan: en Windows `set V=1 && node pruebas/pruebas_cilia.js`, en Mac o Linux `V=1 node pruebas/pruebas_cilia.js`).

Al final dice cuántas pruebas pasaron. Si alguna falla, muestra cuál es con una ✗ y el programa termina con error.

## Qué cubren (110 pruebas)
Dolor de oído simple, combinación de molestias, solo mareo, pérdida súbita de audición, tercero con "No sé", paciente con "No sé" en seguridad, vía rápida (y cuándo NO se ofrece), tres respuestas evasivas, consentimiento rechazado, mareo con impacto funcional, inicio súbito de audición, fármacos mal escritos, lateralidad automática, botón Volver (retroceder y cambiar una respuesta), botón de llamada al 131 (cuándo aparece y cuándo no), recomendaciones en dos bloques (según lo referido y generales), inicio súbito con reconocimiento de la respuesta previa y confirmación de pérdida parcial, pregunta de hablar o entender con opciones, secreción y sangre por separado, ruido reciente o laboral, preguntas ancladas a la molestia (lado solo para molestias del oído, inicio repentino con el nombre de la molestia, opciones según lo referido), molestia principal (cuál molesta más, duración sobre esa molestia, orden de las recomendaciones), ayuda cuando no sabe el lado del oído, impacto en el día a día, condiciones o alergias y lo que ya usó (registro sin cambiar la orientación), y pruebas de las funciones internas.

## Qué NO cubren
- Cómo se ve la app (botones, colores, letra grande, impresión, scroll).
- Que los botones respondan al tocarlos en un celular.
- Que las reglas clínicas sean correctas: las pruebas solo comprueban que la app hace lo que está definido, no que lo definido sea clínicamente adecuado.

## Si cambias el código a propósito
Si cambias una regla o una pregunta, es normal que alguna prueba falle. Actualiza esa prueba en `pruebas_cilia.js` para reflejar el nuevo comportamiento esperado.
Si el programa dice "El código de la app cambió y el cargador de pruebas ya no encaja", significa que se modificó alguna de las 4 funciones que las pruebas reemplazan (`say`, `ask`, `end` o la barra de progreso). Hay que ajustar la lista `cambios` al inicio del archivo.
