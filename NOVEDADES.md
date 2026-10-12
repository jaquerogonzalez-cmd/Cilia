# Cilia · Novedades por versión

**Cilia** es un asistente web que orienta a personas con molestias de oído, audición o equilibrio antes de su consulta.
Autor: Rodrigo Jaque, TM ORL.

> **Versión beta.** Cilia no es un dispositivo médico, no diagnostica y no reemplaza una consulta. Sus reglas aún no han sido validadas clínicamente. No guarda ni envía las respuestas del paciente: quedan solo en su navegador.

## Resumen de versiones

| Versión | Enfoque | Estado |
|---|---|---|
| **Beta 1** | Base: flujo completo de orientación | Publicada |
| **Beta 1.1** | Manejo de la pantalla | Publicada |
| **Beta 1.2** | Casos especiales de pacientes | Publicada |
| **Beta 1.3** | Menos repetición e impresión | Publicada |
| **Beta 1.4** | Estructura y datos del paciente | Publicada |
| **Beta 1.5** | Protección, accesibilidad y revisión clínica | **En desarrollo** (4 de 6 partes listas) |

---

## Beta 1 · Base

**Qué incluye**
- Conversación guiada: consentimiento, datos (nombre, edad, sexo registrado al nacer) y seis preguntas de seguridad (banderas rojas).
- Si hay una bandera roja, aviso de urgencias (131 SAMU) y opción de continuar de todos modos.
- Motivo de consulta, lateralidad y síntomas: escucha menos, zumbido, oído tapado, secreción, dolor y fiebre.
- Bloque de mareo: tipo, duración, frecuencia, desencadenantes y náuseas.
- Evolución (hace cuánto, si fue repentino) y antecedentes (ruido, infecciones, cirugías, familiares, medicamentos).
- Respuestas Sí / No / No sé; "No sé" nunca se trata como "No".
- Orientación en tres niveles y pautas generales de cuidado.
- "Tu resumen" con las alertas ordenadas, y botones para copiar e imprimir.
- Modo oscuro automático y crédito *by Rodrigo Jaque TM ORL*.

**Limitaciones de esta versión**
- Todos los pacientes recibían las mismas preguntas, con mucho énfasis en mareo.
- No se podía corregir una respuesta.

---

## Beta 1.1 · Manejo de la pantalla

**Novedades**
- Botón **← Volver**: retrocede una pregunta a la vez y recalcula las alertas.
- La conversación tiene su propio desplazamiento; el título y los botones de respuesta quedan fijos.
- La pantalla baja sola hasta la pregunta nueva.
- Etiqueta de versión junto al nombre.

---

## Beta 1.2 · Casos especiales de pacientes

**Novedades**
- **Respuesta de un tercero:** preguntas redactadas con signos observables ("¿se queja de zumbidos?").
- **Vía rápida:** los controles sin molestias saltan el cuestionario de síntomas.
- **Mareo en lenguaje funcional:** si no sabe describirlo, pregunta si puede caminar solo o debe quedarse acostado.
- **Freno de seguridad:** un "No sé" en una pregunta de alerta detiene el cuestionario y sugiere ayuda presencial o urgencias.
- **Límite de tolerancia:** a la tercera respuesta evasiva se cierra la sesión con una nota.

**Cambios de comportamiento**
- El motivo de consulta pasó a ir antes de las preguntas de seguridad.

---

## Beta 1.3 · Menos repetición e impresión

**Novedades**
- Las preguntas ya respondidas se saltan solas: un "Sí" a pérdida súbita de audición completa "escucha menos" e inicio repentino.
- **Lateralidad automática:** si el relato menciona un solo lado (o "ambos"), no se vuelve a preguntar.
- **Dos impresiones:** resumen o conversación completa.
- Los bloques impresos no se cortan entre páginas, y el texto sale legible aunque el paciente use modo oscuro.

---

## Beta 1.4 · Estructura y datos del paciente

**Novedades**
- **El rol va primero:** "¿esta consulta es para ti o para otra persona?". La ficha queda a nombre del paciente desde el inicio, con su sexo y edad.
- **Edad en años o meses**, para lactantes.
- **Molestias por selección múltiple:** cada molestia activa solo sus preguntas. Un dolor de oído simple pasa de unas 15 preguntas a 8, sin preguntas de mareo.
- **Vía rápida en dos capas:** no se ofrece si el motivo tiene palabras de síntoma, y antes se confirma que no hay molestias.
- **Detección de fármacos ototóxicos** tolerante a errores de escritura ("gintamicina", "kimioterapia").
- **Botonera final** reordenada: copiar como acción principal, imprimir agrupado y "Nueva evaluación" aparte, con confirmación.
- **Más indicaciones** (no poner gotas ni remedios caseros, cuándo ir a urgencias por mareo) y un bloque **"Por qué te lo sugiero"**.
- Resumen con "Molestias referidas" y "No referidas".
- Orden interno del estado de la app (sin cambios visibles).

**Cambios de comportamiento**
- "Dolor de oído" ahora orienta a *consultar con un otorrino en los próximos días*.
- Las pautas se activan solo con un "Sí" explícito.

---

## Beta 1.5 · Protección, accesibilidad y revisión clínica *(en desarrollo)*

**Listo**
- **Aviso de beta** visible en todo momento y en el primer mensaje de Cilia.
- **Planilla de revisión clínica** (`Cilia_Revision_Clinica.xlsx`) con todas las preguntas, reglas, pautas y listas, para que un profesional de ORL las apruebe o corrija.
- **Accesibilidad:** botones **A−** y **A+** (4 tamaños de letra) y **alto contraste**, que se adapta al modo claro u oscuro. La preferencia se recuerda en el navegador; al imprimir todo vuelve a lo normal.
- **Compartir resumen** con el menú del celular y **Enviar comentarios** por correo.
- **Pruebas automáticas** (`pruebas/`): 35 pruebas que se corren con Node.js antes de publicar.

**Pendiente**
- **Menores de edad:** pedir que continúe un adulto responsable. *Necesita revisión legal.*
- **Triaje por edad:** tramos de edad y banderas rojas pediátricas. *Necesita la revisión de un profesional de ORL.*
- Actualizar la etiqueta de la app a "Beta 1.5" cuando se cierre la versión.

---

## Lo que no ha cambiado en ninguna versión
- Cilia no diagnostica ni reemplaza la evaluación médica.
- Aviso de urgencias con el 131 (SAMU).
- Las respuestas no se guardan ni se envían.
- Crédito *by Rodrigo Jaque TM ORL*.

## Cómo saber qué versión estás usando
La etiqueta aparece junto al nombre **Cilia**, en la pestaña del navegador y en la nota final del resumen.

## Limitaciones conocidas
- Las reglas clínicas fueron redactadas por el desarrollador y no están validadas por profesionales.
- No hay envío del resumen a ningún sistema ni equipo clínico: el paciente decide si lo copia, imprime o comparte.
- Los menores de edad aún no tienen un flujo propio.
- Alcance acotado a audición y equilibrio.

## Próximo
**Beta 2:** árbol de decisión mejorado, a partir de la propuesta de German, sobre la estructura ya ordenada.
