# Cuando la versión equivocada llega al cliente: un post-mortem sobre control de versiones en documentos

## Contexto

Dirijo Lumai, una consultora que ofrece servicios de recursos humanos, marketing y contabilidad para personas y pymes. Uno de nuestros servicios más solicitados es la optimización de currículums: trabajamos con un flujo estandarizado que genera versiones internas de trabajo (con comentarios, notas de revisión y ajustes pendientes) y una versión final lista para entregar al cliente en formato DOCX y PDF.

Como muchas operaciones pequeñas, durante un tiempo gestionamos estos archivos de forma manual: carpetas locales, nombres de archivo improvisados y envíos directos por correo. El sistema "funcionaba"... hasta que dejó de funcionar.

## Problema

Un día, al enviar la entrega final a una clienta, adjunté por error una versión interna de trabajo de su CV en lugar de la versión final. La versión interna contenía notas de revisión y elementos que no estaban pensados para ojos del cliente.

El problema técnico de fondo no fue el descuido de un momento: fue la ausencia de un sistema de control de versiones. Ambos archivos convivían en la misma carpeta, con nombres casi idénticos, sin ninguna barrera que impidiera confundirlos. El error era cuestión de tiempo; si no ocurría ese día, iba a ocurrir otro.
