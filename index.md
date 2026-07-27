# Cuando la versión equivocada llega al cliente: un post-mortem sobre control de versiones en documentos

## Contexto

Dirijo Lumai, una consultora que ofrece servicios de recursos humanos, marketing y contabilidad para personas y pymes. Uno de nuestros servicios más solicitados es la optimización de currículums: trabajamos con un flujo estandarizado que genera versiones internas de trabajo (con comentarios, notas de revisión y ajustes pendientes) y una versión final lista para entregar al cliente en formato DOCX y PDF.

Como muchas operaciones pequeñas, durante un tiempo gestionamos estos archivos de forma manual: carpetas locales, nombres de archivo improvisados y envíos directos por correo. El sistema "funcionaba"... hasta que dejó de funcionar.

## Problema

Un día, al enviar la entrega final a una clienta, adjunté por error una versión interna de trabajo de su CV en lugar de la versión final. La versión interna contenía notas de revisión y elementos que no estaban pensados para ojos del cliente.

El problema técnico de fondo no fue el descuido de un momento: fue la ausencia de un sistema de control de versiones. Ambos archivos convivían en la misma carpeta, con nombres casi idénticos, sin ninguna barrera que impidiera confundirlos. El error era cuestión de tiempo; si no ocurría ese día, iba a ocurrir otro.
## Acciones

Apliqué un protocolo de post-mortem constructivo, enfocado en causas y no en culpas:

1. **Contención inmediata:** envié un reenvío correctivo a la clienta con la versión final, reconociendo el error con honestidad y profesionalismo, sin excusas.
2. **Descripción objetiva del incidente:** documenté qué se envió, cuándo y por qué canal, para entender la secuencia exacta.
3. **Análisis de causa raíz:** la causa no fue "falta de atención", sino un flujo de trabajo sin separación entre archivos de trabajo y entregables finales. Preguntándome "¿por qué?" varias veces, llegué a la raíz: no existía una convención de versiones ni una carpeta exclusiva de entregables.
4. **Acciones correctivas y preventivas:**
   - Convención de nombres obligatoria: los archivos internos llevan sufijo `_BORRADOR` y los finales `_FINAL_v1`, `_FINAL_v2`, etc.
   - Carpeta separada de "Entregables" desde la cual se hace todo envío a clientes; nada se envía desde la carpeta de trabajo.
   - Verificación previa al envío: abrir el adjunto antes de enviar, siempre.
   - Adopción de control de versiones real (Git/GitHub) para la documentación de procesos, precisamente lo que estoy aplicando al publicar este blog.
## Aprendizajes

- **El control de versiones no es solo para código.** Cualquier flujo que produzca múltiples versiones de un archivo —un CV, un manual, una propuesta— necesita convenciones claras de nombres, separación entre trabajo en curso y entregables, e historial de cambios. Git resuelve de forma nativa lo que yo intentaba resolver con memoria y buena voluntad.
- **Los errores de proceso se corrigen con procesos, no con promesas.** "Voy a fijarme más" no es una acción correctiva; una carpeta de entregables con verificación previa sí lo es.
- **Un post-mortem sin culpas produce mejoras reales.** Al enfocarme en la causa raíz en lugar de castigarme por el descuido, salieron mejoras concretas que hoy son parte estándar de mi flujo de trabajo.
- **La transparencia fortalece la relación con el cliente.** El reenvío honesto y rápido fue mejor recibido que cualquier intento de disimular el error.

## Reflexión: feedback radicalmente sincero

Este incidente me obligó a practicar el feedback radicalmente sincero en dos direcciones. Primero, hacia el cliente: reconocer el error de frente, sin minimizarlo ni sobreexplicarlo, cuidando la relación con honestidad y respeto. Segundo —y más difícil—, hacia mí misma: aceptar que el problema no era un descuido puntual sino una falla de diseño en mi propio proceso, algo incómodo de admitir cuando una es la fundadora y responsable de todo el flujo.

Durante la creación de este blog también apliqué ese principio: cada commit de este repositorio documenta una etapa real del trabajo, con mensajes claros que cualquier persona puede auditar. La sinceridad radical, aplicada al proceso técnico, se traduce en trazabilidad: que el historial cuente la verdad de cómo se construyó el resultado.
