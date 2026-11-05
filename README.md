# CRISTAL AZUL – Ecosistema de Automatización con Inteligencia Artificial

## 1. Descripción del proyecto

Cristal Azul es un ecosistema de automatización inteligente desarrollado para gestionar solicitudes de clientes de un servicio de limpieza de vidrios en altura.

El sistema permite recibir solicitudes, almacenar información, generar respuestas mediante inteligencia artificial y enviar comunicaciones por correo electrónico luego de una aprobación humana.

## 2. Objetivos

- Automatizar la recepción de solicitudes.
- Centralizar la información de los clientes.
- Utilizar inteligencia artificial para generar respuestas.
- Incorporar supervisión y aprobación humana.
- Automatizar el envío de correos electrónicos.

## 3. Tecnologías utilizadas

- **Make:** orquestación de los procesos.
- **Airtable:** base de datos y gestión de solicitudes.
- **Google Gemini AI:** generación de respuestas inteligentes.
- **Gmail:** envío de respuestas a los clientes.
- **GitHub:** documentación y almacenamiento de archivos del proyecto.

## 4. Arquitectura del sistema

### Escenario 1 – Recepción y procesamiento con IA

1. Un cliente envía una solicitud mediante un Webhook.
2. Make recibe los datos.
3. Airtable crea un registro con la información recibida.
4. Google Gemini AI analiza la solicitud y genera una respuesta.
5. Airtable actualiza el registro con la respuesta generada y el estado correspondiente.

**Estado final:** Procesado por IA.

### Escenario 2 – Aprobación humana y envío

1. Make busca en Airtable las solicitudes que tienen el estado «Aprobado por Humano».
2. Se recuperan los datos del cliente y la respuesta generada por Gemini.
3. Gmail envía automáticamente el correo electrónico al cliente.
4. Airtable actualiza el estado del registro a «Enviado al Cliente».

**Resultado:** el cliente recibe una respuesta por correo electrónico luego de la aprobación humana.

## 5. Control humano

El sistema incorpora una instancia de supervisión humana. La respuesta generada por inteligencia artificial debe ser revisada antes de habilitar el envío al cliente.

La aprobación se realiza mediante la actualización manual del estado en Airtable.

## 6. Base de datos

La base de Airtable permite consultar y administrar las solicitudes recibidas.

[Consultar la base de datos de Cristal Azul](https://airtable.com/appiiuDw3KiCGl5fN/shr2OEpkZ88fOyY51)

## 7. Evidencias y documentación

- [Arquitectura del proyecto](docs/Arquitectura_Cristal_Azul.pdf)
- [Escenario 1 – Recepción y procesamiento IA](make/Escenario_1_Recepcion_IA.json)
- [Escenario 2 – Aprobación y envío](make/Escenario_2_Aprobacion_Envio.json)
- [Capturas de evidencia](evidencias/)

## 8. Video demostrativo

[Ver demostración del funcionamiento de Cristal Azul](https://youtu.be/ddm7N-O3k3s)

## 9. Pruebas realizadas

Se realizaron pruebas de:

- Recepción de solicitudes mediante Webhook.
- Creación de registros en Airtable.
- Generación de respuestas con Google Gemini AI.
- Actualización de estados.
- Aprobación humana.
- Envío de correos mediante Gmail.
- Confirmación de recepción del correo electrónico.

## 10. Mejoras pendientes

- Ampliar el manejo automático y registro de errores.
- Incorporar validaciones para evitar envíos duplicados.
- Mejorar las notificaciones ante fallos de procesamiento.

## 11. Proyecto académico

**Proyecto:** Cristal Azul  
**Entrega:** Ecosistema de Automatización IA Autónomo para Negocios  
**Orquestador:** Make  
**Base de datos:** Airtable  
**Inteligencia artificial:** Google Gemini AI  
**Comunicación:** Gmail


