# Capítulo III: Requirements Specification
## 3.1. To-Be Scenario Mapping.

Segmento 1:

| Fases    |  fase 1 as is | fase 2| fase 3|
| -------- | ------- | ---- | ---------------- |
| Doing    | | texto| texto | texto| texto|
| Thinking | | texto| texto | texto| texto|
| Feeling  | | texto| texto | texto| texto|

Segmento 2:
| Fases    |  fase 1 as is | fase 2| fase 3|
| -------- | ------- | ---- | ---------------- |
| Doing    | | texto| texto | texto| texto|
| Thinking | | texto| texto | texto| texto|
| Feeling  | | texto| texto | texto| texto|

## 3.2. User Stories.


| EPIC/ USER STORY ID | Titulo | Descripción | Criterio de aceptación |Relacionado a la epica #|
|-|-|-|-|-|
| E01 | Registro |Como empresario pesquero o productor de maquinaria, Quiero poder registrarme o iniciar sesión para acceder a las funciones asignadas a mi rol. | | |
| E02 | Monitoreo de equipos| Como empresario pesquero, Quiero poder verificar el estado de mis equipos a través de la aplicación web | | |
| E03 | Facturación  | Como productor de maquinaria pesquera, Quiero realizar mi facturación de manera más rápida. | | |
| E04 | Inventario | Como productor de maquinaria pesquera deseo tener un inventario al que  | | |
| E05 | Solicitudes de Equipos | Como empresario pesquero, quiero poder realizar solicitudes de compra de equipos a la empresa productora para que me brinden el equipo necesario. | | |
| E06 | Landing Page y Precios | Como usuario potencial,<br> Quiero navegar por una Landing Page Informativa<br> Para poder informarme sobre los beneficios y costos de un producto | | |
|E07|Inventory Management|Como desarrollador, <br> Quiero desarrollar y mantener endpoints de API para gestionar el inventario de los productores de maquinaria, <br> Para permitir la gestion de inventario a traves de la aplicacion web|||
| E08 | Fishing Machinery Management | Como desarrollador,<br> Quiero desarrollar y mantener endpoints de API para gestionar el catálogo de productos hechos por los productores de maquinaria,<br> Para permitir la visualización, creación, actualización y eliminación de productos en la aplicación web. | | |
| E09 | Users Management | Como desarrollador,<br> Quiero desarrollar y mantener endpoints de API para la gestión de usuarios,<br> Para permitir el registro, inicio de sesión, actualización y eliminación de cuentas de usuarios dentro de la aplicación web. | | |
| E10 | Billing Management | Como desarrollador,<br> Quiero desarrollar y mantener endpoints de API para gestionar la facturación de los productos y servicios ofrecidos por los productores de maquinaria,<br> Para permitir la creación, consulta y administración de facturas a través de la aplicación web. | | |
| US01                | Registro de un nuevo usuario  | **Como** empresario pesquero o productor de maquinaria <br>**Quiero** registrar una cuenta en la aplicación <br> **Para** acceder a las funciones asignadas a mi rol. | **Escenario 1: Registro exitoso del usuario** <br><br>Dado que el usuario ingresa información válida <br>Cuando el usuario envía el formulario de registro <br> Entonces el usuario recibe una confirmación de registro por email y puede iniciar sesión. <br><br>**Escenario 2: Registro fallido por usuario ya existente** <br><br>Dado que el usuario intenta registrar un email que ya está en uso <br>Cuando el usuario envía el formulario de registro <br> Entonces el sistema muestra un mensaje indicando que el email ya está registrado y solicita usar uno diferente. | E01                      |
| US02                | Inicio de sesión              | **Como** empresario pesquero o productor de maquinaria <br>**Quiero** iniciar sesión en la aplicación <br> **Para** acceder a las funciones de mi cuenta. | **Escenario 1: Inicio de sesión exitoso** <br><br>Dado que el usuario ingresa credenciales correctas <br>Cuando el usuario envía el formulario de inicio de sesión <br> Entonces el usuario es redirigido a su panel de control. <br><br>**Escenario 2: Error en el inicio de sesión por credenciales incorrectas** <br><br>Dado que el usuario ingresa credenciales incorrectas <br>Cuando el usuario envía el formulario de inicio de sesión <br> Entonces el sistema muestra un mensaje de error indicando que las credenciales son incorrectas y permite al usuario intentar de nuevo. | E01                      |
| US03                | Estado de equipos              | **Como** empresario pesquero <br>**Quiero** verificar el estado actual de mis equipos <br> **Para** saber si están operativos o necesitan mantenimiento. | **Escenario 1: Visualización del estado de equipos** <br><br>Dado que el usuario accede a la sección de estado de equipos <br>Cuando el usuario consulta el listado <br> Entonces el estado de cada equipo se muestra correctamente (operativo, en mantenimiento, etc.). <br><br>**Escenario 2: Equipos no visibles en el listado** <br><br>Dado que el usuario accede a la sección de estado de equipos <br>Cuando el usuario no puede ver algunos equipos <br> Entonces el sistema muestra un mensaje indicando que no se pueden recuperar todos los datos y sugiere al usuario intentar más tarde.  | E02  |
| US04                | Notificaciones de estado       | **Como** empresario pesquero <br>**Quiero** recibir notificaciones sobre el estado de mis equipos <br> **Para** estar informado sobre cualquier cambio crítico. | **Escenario 1: Recepción de notificaciones** <br><br>Dado que el estado de un equipo cambia a crítico <br>Cuando el sistema detecta el cambio <br> Entonces el usuario recibe una notificación por email o dentro de la aplicación. | E02                      |
| US05             | Historial de mantenimiento     | **Como** empresario pesquero <br>**Quiero** consultar el historial de mantenimiento de mis equipos <br> **Para** revisar las actividades realizadas. | **Escenario 1: Consulta de historial de mantenimiento** <br><br>Dado que el usuario selecciona un equipo <br>Cuando el usuario consulta el historial <br> Entonces el historial de mantenimiento se muestra con todas las actividades realizadas. <br><br>**Escenario 2: Historial vacío o no disponible** <br><br>Dado que el usuario consulta el historial de un equipo sin mantenimiento registrado <br>Cuando el usuario no encuentra registros <br> Entonces el sistema muestra un mensaje indicando que no hay historial disponible para ese equipo. <br><br>**Escenario 3: Problemas en la carga del historial** <br><br>Dado que el usuario intenta acceder al historial <br>Cuando el sistema experimenta problemas de carga <br> Entonces el sistema muestra un mensaje de error y sugiere al usuario intentar más tarde. | E02                      |
| US06                | Alertas de equipos críticos    | **Como** empresario pesquero <br>**Quiero** establecer alertas para el estado crítico de mis equipos <br> **Para** recibir notificaciones cuando un equipo necesite atención urgente. | **Escenario 1: Configuración de alertas** <br><br>Dado que el usuario establece un umbral crítico para un equipo <br>Cuando el estado del equipo alcanza el umbral <br> Entonces el usuario recibe una alerta por dentro de la aplicación. | E02                      |
| US07                | Generación de facturas         | **Como** productor de maquinaria pesquera <br>**Quiero** generar facturas automáticamente <br> **Para** acelerar el proceso de facturación. | **Escenario 1: Generación de factura** <br><br>Dado que el usuario ingresa los detalles de la venta <br>Cuando el usuario genera la factura <br> Entonces la factura se crea con los datos proporcionados y puede ser exportada en formato PDF. <br><br>**Escenario 2: Error en la generación de factura** <br><br>Dado que el usuario ingresa datos incompletos o incorrectos <br>Cuando el usuario intenta generar la factura <br> Entonces el sistema muestra un mensaje de error indicando qué datos son inválidos o faltantes y permite corregir los datos.| E03                      |
| US08               | Personalización de plantillas  | **Como** productor de maquinaria pesquera <br>**Quiero** personalizar las plantillas de mis facturas <br> **Para** que reflejen la identidad de mi empresa. | **Escenario 1: Personalización de plantilla** <br><br>Dado que el usuario accede a la configuración de plantillas <br>Cuando el usuario elige y edita una plantilla <br> Entonces la plantilla personalizada se guarda y puede ser utilizada para futuras facturas. <br><br>**Escenario 2: Plantilla no aplicada correctamente** <br><br>Dado que el usuario utiliza una plantilla personalizada <br>Cuando la factura generada no refleja los cambios <br> Entonces el sistema muestra un mensaje indicando que la plantilla no se aplicó correctamente y permite al usuario aplicar los cambios nuevamente. | E03|
| US09                | Historial de facturación       | **Como** productor de maquinaria pesquera <br>**Quiero** consultar el historial de todas mis facturas <br> **Para** llevar un registro completo de las transacciones. | **Escenario 1: Consulta de historial de facturación** <br><br>Dado que el usuario accede al historial de facturación <br>Cuando el usuario aplica filtros (por fecha, cliente, etc.) <br> Entonces el historial se muestra con las facturas correspondientes. <br><br>**Escenario 2: Historial vacío o incompleto** <br><br>Dado que el usuario consulta el historial <br>Cuando no hay facturas registradas o el historial está incompleto <br> Entonces el sistema muestra un mensaje indicando que no hay facturas disponibles y permite al usuario ajustar los filtros de búsqueda. <br><br>**Escenario 3: Problemas en la carga del historial** <br><br>Dado que el usuario intenta acceder al historial <br>Cuando el sistema experimenta problemas de carga <br> Entonces el sistema muestra un mensaje de error y sugiere al usuario intentar más tarde.|E03                      |
| US10  | Notificaciones de estado | **Como** empresario pesquero <br>**Quiero** recibir notificaciones sobre el estado de mis equipos <br> **Para** estar informado sobre cualquier cambio crítico. | **Escenario 1: Recepción de notificaciones** <br><br>Dado que el estado de un equipo cambia a crítico <br>Cuando el sistema detecta el cambio <br> Entonces el usuario recibe una notificación por email o dentro de la aplicación. <br><br>**Escenario 2: Falta de notificación por cambio crítico** <br><br>Dado que el estado de un equipo cambia a crítico <br>Cuando el usuario no recibe una notificación <br> Entonces el sistema muestra un mensaje indicando un fallo en el envío de notificaciones y el usuario tiene la opción de verificar la configuración de notificaciones.| US04| Alertas de equipos críticos    | **Como** empresario pesquero <br>**Quiero** establecer alertas para el estado crítico de mis equipos <br> **Para** recibir notificaciones cuando un equipo necesite atención urgente. | **Escenario 1: Configuración de alertas** <br><br>Dado que el usuario establece un umbral crítico para un equipo <br>Cuando el estado del equipo alcanza el umbral <br> Entonces el usuario recibe una alerta por email o dentro de la aplicación. <br><br>**Escenario 2: Error en la configuración de alertas** <br><br>Dado que el usuario establece una alerta <br>Cuando el sistema falla al guardar la configuración <br> Entonces el sistema muestra un mensaje de error y solicita al usuario intentar nuevamente. <br><br>**Escenario 3: Alertas no recibidas** <br><br>Dado que el estado de un equipo alcanza el umbral crítico <br>Cuando el usuario no recibe la alerta <br> Entonces el sistema muestra un mensaje indicando problemas en el envío de alertas y permite al usuario verificar la configuración de notificaciones. | E02                      |
| US11                | Gestión de inventario          | **Como** productor de maquinaria pesquera <br>**Quiero** gestionar el inventario de mis productos <br> **Para** saber qué productos están disponibles para la venta. | **Escenario 1: Gestión exitosa del inventario** <br><br>Dado que el usuario ingresa al sistema de inventario <br>Cuando el usuario actualiza las cantidades de los productos <br> Entonces el sistema guarda los cambios y muestra el inventario actualizado. <br><br>**Escenario 2: Error en la actualización del inventario** <br><br>Dado que el usuario intenta actualizar el inventario <br>Cuando el sistema experimenta problemas técnicos <br> Entonces el sistema muestra un mensaje de error y solicita intentar más tarde. | E04                      |
| US12               | Gestión de inventario          | **Como** productor de maquinaria pesquera <br>**Quiero** gestionar el inventario de mis productos <br> **Para** saber qué productos están disponibles para la venta. | **Escenario 1: Gestión exitosa del inventario** <br><br>Dado que el usuario ingresa al sistema de inventario <br>Cuando el usuario actualiza las cantidades de los productos <br> Entonces el sistema guarda los cambios y muestra el inventario actualizado. <br><br>**Escenario 2: Error en la actualización del inventario** <br><br>Dado que el usuario intenta actualizar el inventario <br>Cuando el sistema experimenta problemas técnicos <br> Entonces el sistema muestra un mensaje de error y solicita intentar más tarde. | E04                      |
| US13                | Consulta de productos en inventario | **Como** productor de maquinaria pesquera <br>**Quiero** consultar el inventario actual de productos <br> **Para** planificar mis próximas ventas. | **Escenario 1: Consulta exitosa del inventario** <br><br>Dado que el usuario accede al sistema de inventario <br>Cuando el usuario selecciona la categoría de productos <br> Entonces se muestran todos los productos disponibles y sus cantidades. <br><br>**Escenario 2: Error en la consulta del inventario** <br><br>Dado que el usuario accede al sistema de inventario <br>Cuando el sistema no puede cargar los datos del inventario <br> Entonces el sistema muestra un mensaje de error e indica que el usuario debe intentar más tarde. | E04                      |
| US14 | Solicitud de compra de equipo estándar | Como empresario pesquero, quiero poder seleccionar un equipo estándar y realizar la compra a través de la plataforma, para asegurarme de tener el equipo que necesito rápidamente. | **Escenario 1: Solicitud de compra enviada exitosamente**<br>Dado que el usuario accede al catálogo de equipos,<br>Cuando selecciona un equipo estándar y completa el formulario de compra,<br>Entonces el sistema confirma la solicitud y el usuario recibe una notificación de compra exitosa.<br><br>**Escenario 2: Error en la solicitud de compra**<br>Dado que el usuario intenta completar la solicitud de compra,<br>Cuando hay un error en el envío del formulario,<br>Entonces el sistema muestra un mensaje de error y solicita al usuario que lo intente nuevamente. | E05 |
| US36 | Solicitud de compra de equipo personalizado | Como empresario pesquero, quiero poder realizar una solicitud de compra de equipos personalizados, para obtener un equipo adaptado a las necesidades de mi operación. | **Escenario 1: Solicitud de equipo personalizado realizada con éxito**<br>Dado que el usuario accede a la sección de equipos personalizados,<br>Cuando completa el formulario con los detalles técnicos del equipo,<br>Entonces el sistema envía la solicitud al proveedor, y el usuario recibe una confirmación de que será contactado.<br><br>**Escenario 2: Error en la solicitud de equipo personalizado**<br>Dado que el usuario intenta enviar una solicitud personalizada,<br>Cuando hay un fallo en el formulario,<br>Entonces el sistema muestra un mensaje de error e informa al usuario sobre los campos incompletos. | E05 |
| US15 | Solicitud de alquiler de equipos | Como empresario pesquero, quiero poder alquilar equipos por un período limitado, para evitar comprar equipos que solo necesito temporalmente. | **Escenario 1: Solicitud de alquiler exitosa**<br>Dado que el usuario accede a la sección de alquiler de equipos,<br>Cuando selecciona el equipo y elige la duración del alquiler,<br>Entonces la solicitud se envía y el usuario recibe una confirmación del período de alquiler.<br><br>**Escenario 2: Error en la solicitud de alquiler**<br>Dado que el usuario intenta alquilar un equipo,<br>Cuando el equipo no está disponible o el sistema falla,<br>Entonces el sistema muestra un mensaje de error indicando que el equipo no puede ser alquilado en ese momento. | E05 |
| US16 | Seguimiento de solicitudes de equipos | Como empresario pesquero, quiero poder hacer seguimiento del estado de mis solicitudes de compra o alquiler, para saber cuándo recibiré los equipos solicitados. | **Escenario 1: Seguimiento exitoso de la solicitud**<br>Dado que el usuario ha realizado una solicitud de compra o alquiler,<br>Cuando accede a la sección "Mis Solicitudes",<br>Entonces puede ver el estado actual (En proceso, Aprobada, En camino, etc.) de cada solicitud.<br><br>**Escenario 2: Error al intentar hacer seguimiento**<br>Dado que el usuario intenta consultar el estado de una solicitud,<br>Cuando hay un problema de conexión o fallo en el sistema,<br>Entonces el sistema muestra un mensaje de error indicando que no se puede obtener el estado de la solicitud en ese momento. | E05 |
| US17 | Cancelación de solicitudes de equipos | Como empresario pesquero, quiero poder cancelar una solicitud de compra o alquiler de equipos, para adaptarme a cambios en mis operaciones. | **Escenario 1: Cancelación de solicitud exitosa**<br>Dado que el usuario ha realizado una solicitud y desea cancelarla,<br>Cuando accede a la opción de cancelar antes del envío del equipo,<br>Entonces el sistema confirma la cancelación y el usuario recibe una notificación.<br><br>**Escenario 2: Error en la cancelación de la solicitud**<br>Dado que el usuario intenta cancelar una solicitud,<br>Cuando el equipo ya ha sido enviado o el sistema falla,<br>Entonces el sistema muestra un mensaje indicando que no es posible cancelar la solicitud en ese momento. | E05 |
| US18 | Navegación por la Landing Page | Como usuario potencial, quiero poder navegar fácilmente por la landing page, para obtener información clara y precisa sobre los productos ofrecidos. | **Escenario 1: Navegación exitosa**<br> Dado que el usuario accede a la landing page,<br> Cuando navega por las diferentes secciones,<br> Entonces la página carga correctamente y el usuario puede ver toda la información sin problemas.  | E06 |
| US19 | Visualización de Precios | Como usuario potencial, quiero ver claramente los precios de los productos ofrecidos en la landing page, para evaluar si se ajustan a mi presupuesto. | **Escenario 1: Precios visibles en la página**<br> Dado que el usuario está en la landing page,<br> Cuando accede a la sección de precios,<br> Entonces los precios se muestran claramente y sin problemas. | E06 |
| US20 | Comparación de beneficios | Como usuario potencial, quiero comparar los beneficios de diferentes planes en la landing page, para decidir cuál es la mejor opción para mí. | **Escenario 1: Comparación exitosa**<br> Dado que el usuario accede a la landing page,<br> Cuando compara planes del productos,<br> Entonces puede ver una comparativa clara con los beneficios de cada producto.| E06 |
| US21 | Contacto con ventas desde la landing page | Como usuario potencial, quiero poder contactar al equipo de ventas directamente desde la landing page, para obtener más información sobre los productos o servicios. | **Escenario 1: Contacto exitoso**<br> Dado que el usuario accede a la landing page,<br> Cuando selecciona la opción de contacto y completa el formulario de contacto,<br> Entonces el sistema envía la solicitud correctamente. | E06 |
| US22 | Consulta de reseñas de clientes | Como usuario potencial, quiero ver reseñas de clientes en la landing page, para conocer la experiencia de otros usuarios con el producto. | **Escenario 1: Visualización exitosa de reseñas**<br> Dado que el usuario accede a la landing page,<br> Cuando accede a la sección de reseñas,<br> Entonces puede ver las reseñas de otros clientes sin problemas. | E06 |
| TS01 | Create Inventory Record | As a developer,<br> I want to implement the POST endpoint for creating inventory records,<br> To allow machinery producers to add new products to their inventory. | **Scenario 1: Successful creation of an inventory record**<br> Given the endpoint /api/v1/inventory is available,<br> When a POST request is sent with values for productId and quantity,<br> Then a response is received with status 201,<br> And the Inventory Resource is included in the Response Body, with a new ID and the registered values for productId and quantity.<br><br>**Scenario 2: Duplicate inventory record creation**<br> Given the endpoint /api/v1/inventory is available,<br> When a POST request is sent with values that already exist for productId,<br> Then a response is received with status 400,<br> And a message is included in the Response Body, with the value "All constraints are not satisfied for Inventory: An inventory record for this product already exists." | E07 |
| TS02 | Read Inventory Record | As a developer,<br> I want to implement the GET endpoint for reading inventory records,<br> To allow users to retrieve the details of inventory items. | **Scenario 1: Successful retrieval of an inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a GET request is sent with a valid id,<br> Then a response is received with status 200,<br> And the Inventory Resource is included in the Response Body with the details for the specified id.<br><br>**Scenario 2: Retrieval of a non-existing inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a GET request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Inventory record not found." | E07 |
| TS03 | Update Inventory Record | As a developer,<br> I want to implement the PUT endpoint for updating inventory records,<br> To allow users to modify existing inventory details. | **Scenario 1: Successful update of an inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a PUT request is sent with the id and updated values for productId and quantity,<br> Then a response is received with status 200,<br> And the updated Inventory Resource is included in the Response Body with the new values for productId and quantity.<br><br>**Scenario 2: Update of a non-existing inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a PUT request is sent with an invalid id and updated values,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Inventory record not found for update." | E07 |
| TS04 | Delete Inventory Record | As a developer,<br> I want to implement the DELETE endpoint for removing inventory records,<br> To allow users to delete inventory items from their records. | **Scenario 1: Successful deletion of an inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a DELETE request is sent with a valid id,<br> Then a response is received with status 200,<br> And a message is included in the Response Body, with the value "Inventory record deleted successfully.".<br><br>**Scenario 2: Deletion of a non-existing inventory record**<br> Given the endpoint /api/v1/inventory/{id} is available,<br> When a DELETE request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Inventory record not found for deletion." | E07 |
| TS05 | Create Fishing Machinery Record | As a developer,<br> I want to implement the POST endpoint for creating Fishing Machinery records,<br> To allow machinery producers to add new Fishing Machinery to their inventory. | **Scenario 1: Successful creation of a Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery is available,<br> When a POST request is sent with values for equipmentId and quantity,<br> Then a response is received with status 201,<br> And the Fishing Machinery Resource is included in the Response Body, with a new ID and the registered values for equipmentId and quantity.<br><br>**Scenario 2: Duplicate Fishing Machinery record creation**<br> Given the endpoint /api/v1/fishing-machinery is available,<br> When a POST request is sent with values that already exist for equipmentId,<br> Then a response is received with status 400,<br> And a message is included in the Response Body, with the value "All constraints are not satisfied for Fishing Machinery: An equipment record for this ID already exists." | E08 |
| TS06 | Read Fishing Machinery Record | As a developer,<br> I want to implement the GET endpoint for reading Fishing Machinery records,<br> To allow users to retrieve the details of Fishing Machinery items. | **Scenario 1: Successful retrieval of a Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a GET request is sent with a valid id,<br> Then a response is received with status 200,<br> And the Fishing Machinery Resource is included in the Response Body with the details for the specified id.<br><br>**Scenario 2: Retrieval of a non-existing Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a GET request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Fishing Machinery record not found." | E08 |
| TS07 | Update Fishing Machinery Record | As a developer,<br> I want to implement the PUT endpoint for updating Fishing Machinery records,<br> To allow users to modify existing Fishing Machinery details. | **Scenario 1: Successful update of a Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a PUT request is sent with the id and updated values for equipmentId and quantity,<br> Then a response is received with status 200,<br> And the updated Fishing Machinery Resource is included in the Response Body with the new values for equipmentId and quantity.<br><br>**Scenario 2: Update of a non-existing Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a PUT request is sent with an invalid id and updated values,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Fishing Machinery record not found for update." | E08 |
| TS08 | Delete Fishing Machinery Record | As a developer,<br> I want to implement the DELETE endpoint for removing Fishing Machinery records,<br> To allow users to delete Fishing Machinery items from their records. | **Scenario 1: Successful deletion of a Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a DELETE request is sent with a valid id,<br> Then a response is received with status 200,<br> And a message is included in the Response Body, with the value "Fishing Machinery record deleted successfully.".<br><br>**Scenario 2: Deletion of a non-existing Fishing Machinery record**<br> Given the endpoint /api/v1/fishing-machinery/{id} is available,<br> When a DELETE request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Fishing Machinery record not found for deletion." | E08 |
| TS09 | Create User Record | As a developer,<br> I want to implement the POST endpoint for creating user records,<br> To allow administrators to add new users to the system. | **Scenario 1: Successful creation of a user record**<br> Given the endpoint /api/v1/users is available,<br> When a POST request is sent with values for userId and userDetails,<br> Then a response is received with status 201,<br> And the User Resource is included in the Response Body, with a new ID and the registered values for userId and userDetails.<br><br>**Scenario 2: Duplicate user record creation**<br> Given the endpoint /api/v1/users is available,<br> When a POST request is sent with values that already exist for userId,<br> Then a response is received with status 400,<br> And a message is included in the Response Body, with the value "All constraints are not satisfied for User: A user record with this ID already exists." | E09 |
| TS10 | Read User Record | As a developer,<br> I want to implement the GET endpoint for reading user records,<br> To allow administrators to retrieve the details of user accounts. | **Scenario 1: Successful retrieval of a user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a GET request is sent with a valid id,<br> Then a response is received with status 200,<br> And the User Resource is included in the Response Body with the details for the specified id.<br><br>**Scenario 2: Retrieval of a non-existing user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a GET request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "User record not found." | E09 |
| TS11 | Update User Record | As a developer,<br> I want to implement the PUT endpoint for updating user records,<br> To allow administrators to modify existing user account details. | **Scenario 1: Successful update of a user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a PUT request is sent with the id and updated values for userId and userDetails,<br> Then a response is received with status 200,<br> And the updated User Resource is included in the Response Body with the new values for userId and userDetails.<br><br>**Scenario 2: Update of a non-existing user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a PUT request is sent with an invalid id and updated values,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "User record not found for update." | E09 |
| TS12 | Delete User Record | As a developer,<br> I want to implement the DELETE endpoint for removing user records,<br> To allow administrators to delete user accounts from the system. | **Scenario 1: Successful deletion of a user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a DELETE request is sent with a valid id,<br> Then a response is received with status 200,<br> And a message is included in the Response Body, with the value "User record deleted successfully.".<br><br>**Scenario 2: Deletion of a non-existing user record**<br> Given the endpoint /api/v1/users/{id} is available,<br> When a DELETE request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "User record not found for deletion." | E09 |
 TS01 | Create Billing Record | As a developer,<br> I want to implement the POST endpoint for creating billing records,<br> To allow users to generate new billing entries. | **Scenario 1: Successful creation of a billing record**<br> Given the endpoint /api/v1/billing is available,<br> When a POST request is sent with values for billingId and billingDetails,<br> Then a response is received with status 201,<br> And the Billing Resource is included in the Response Body, with a new ID and the registered values for billingId and billingDetails.<br><br>**Scenario 2: Duplicate billing record creation**<br> Given the endpoint /api/v1/billing is available,<br> When a POST request is sent with values that already exist for billingId,<br> Then a response is received with status 400,<br> And a message is included in the Response Body, with the value "All constraints are not satisfied for Billing: A billing record with this ID already exists." | E10 |
| TS02 | Read Billing Record | As a developer,<br> I want to implement the GET endpoint for reading billing records,<br> To allow users to retrieve the details of their billing entries. | **Scenario 1: Successful retrieval of a billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a GET request is sent with a valid id,<br> Then a response is received with status 200,<br> And the Billing Resource is included in the Response Body with the details for the specified id.<br><br>**Scenario 2: Retrieval of a non-existing billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a GET request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Billing record not found." | E10 |
| TS03 | Update Billing Record | As a developer,<br> I want to implement the PUT endpoint for updating billing records,<br> To allow users to modify existing billing details. | **Scenario 1: Successful update of a billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a PUT request is sent with the id and updated values for billingId and billingDetails,<br> Then a response is received with status 200,<br> And the updated Billing Resource is included in the Response Body with the new values for billingId and billingDetails.<br><br>**Scenario 2: Update of a non-existing billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a PUT request is sent with an invalid id and updated values,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Billing record not found for update." | E10 |
| TS04 | Delete Billing Record | As a developer,<br> I want to implement the DELETE endpoint for removing billing records,<br> To allow users to delete billing entries from the system. | **Scenario 1: Successful deletion of a billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a DELETE request is sent with a valid id,<br> Then a response is received with status 200,<br> And a message is included in the Response Body, with the value "Billing record deleted successfully.".<br><br>**Scenario 2: Deletion of a non-existing billing record**<br> Given the endpoint /api/v1/billing/{id} is available,<br> When a DELETE request is sent with an invalid id,<br> Then a response is received with status 404,<br> And a message is included in the Response Body, with the value "Billing record not found for deletion." | E10 |












## 3.3. Impact Mapping.



## 3.4. Product Backlog.

| #Orden | User Story ID | Titulo| Descripción| Story Points (1/2/3/5/8) |
| ------ | ------------- | ----- | ---------- | ------------------------ |
| 1      | HU01          | titulo his | desc  | 5                        |
