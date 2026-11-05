# Cristal-Azul-Automatizacion-IA
Ecosistema de automatización con inteligencia artificial para la gestión de clientes de Cristal Azul.
# Cristal Azul – Ecosistema de Automatización con IA

## Descripción del proyecto

Cristal Azul es un proyecto de automatización inteligente orientado a la gestión de solicitudes de clientes para un servicio de limpieza de vidrios en altura.

El sistema utiliza Make, Airtable, Google Gemini AI y Gmail para recibir solicitudes, generar respuestas automáticas asistidas por inteligencia artificial y permitir la aprobación humana antes del envío al cliente.

## Tecnologías utilizadas

- **Make:** automatización y coordinación de los procesos.
- **Airtable:** almacenamiento y gestión de solicitudes.
- **Google Gemini AI:** generación de respuestas.
- **Gmail:** comunicación por correo electrónico.

## Arquitectura del sistema

### Escenario 1 – Recepción y procesamiento con IA

1. Recepción de datos mediante Webhook.
2. Creación de un registro en Airtable.
3. Procesamiento de la solicitud mediante Google Gemini AI.
4. Actualización del registro con la respuesta generada.
5. Estado actualizado a «Procesado por IA».

### Escenario 2 – Aprobación humana y envío
## Video demostrativo

[Ver demostración del funcionamiento de Cristal Azul en YouTube](https://youtu.be/ddm7N-O3k3s)
