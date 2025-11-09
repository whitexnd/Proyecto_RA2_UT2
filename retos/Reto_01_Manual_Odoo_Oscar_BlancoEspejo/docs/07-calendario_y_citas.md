# 07 — Calendario y Citas

## Calendario

En el panel de aplicaciones, seleccionamos el módulo de Calendario para poder ver y gestionar nuestras citas y reuniones con vista diaria, semanal o mensual

![Calendario vistas](../assets/img/07-calendario_y_citas/paso07_calendario-vistas.png "Calendario vistas")

### Integración con Google Calendar
Para integrar nuestro calendario de Odoo con Google Calendar, debemos ir a google cloud console y crear otro proyecto nuevo

![Creación proyecto](../assets/img/07-calendario_y_citas/paso07_creacion-proyecto.png "Creación proyecto")

Buscamos en la parte superior "Google Calendar API" y la habilitamos
![Calendar API](../assets/img/07-calendario_y_citas/paso07_calendar-api.png "Calendar API")

Una vez habilitada debemos crear las credenciales para ello seguimos el mismo proceso que en el paso 5, hasta llegar al paso 3 de los permisos
- [Credenciales](05-integracion_gmail.md#credenciales)


Cuando lleguemos al paso 3, selecionaremos el permiso openid y todos los permisos de Google Calendar API, siguiendo con el paso 4 donde seleccionaremos aplicación web y rellenaremos los datos de nombre y URI de redirección 
>**Importante colocar la URL correctamente**

![ID cliente OAuth](../assets/img/07-calendario_y_citas/paso07_idcliente-oauth.png "ID cliente OAuth")

Y como está explicado en el paso 5 ya tendremos el ID y el secreto el cual debemos copiar en Odoo en la configuración de Google Calendar en el apartado de calendario en los ajustes
![Odoo Google Calendar](../assets/img/07-calendario_y_citas/paso07_odoo-googlecalendar.png "Odoo Google Calendar")

### Odoo Meet
Habiendo configurado Google calendar podemos crear reuniones desde Odoo calendar, donde incluso podremos proporcionar un enlace de una reuinión de zoom o meet o usar Odoo meet para crear una videollamada directamente desde Odoo, para ello clickamos sobre el dia y se nos abarirá un desplegable donde en mas opciones podemos configurar la reunión y activar la opción de odoo meet
![Odoo Meet](../assets/img/07-calendario_y_citas/paso07_odoo-meet.png "Odoo Meet")

Accediendo al enlace o clickando en el icono que aparece al lado podremos unirnos a la videollamada
![Llamada Odoo](../assets/img/07-calendario_y_citas/paso07_llamada-odoo.png "Llamada Odoo")

## Módulo Citas (Enterprise)
Odoo cuenta con un módulo de citas muy potente que nos permite generar un enlace para que nuestros clientes puedan reservar citas
![Panel citas](../assets/img/07-calendario_y_citas/paso07_panel-citas.png "Panel citas")

Al crear una cita podemos modificar distintos detalles entre ellos:
- Preguntas previas
![Preguntas cita](../assets/img/07-calendario_y_citas/paso07_preguntas-cita.png "Preguntas cita")
- Configurar buffers entre citas
![Citas buffer](../assets/img/07-calendario_y_citas/paso07_citas-buffer.png "Citas buffer")

Continuando, en la esquina superior izquierda nos saldra un boton para compartir el enlace de la cita
![Compartir cita](../assets/img/07-calendario_y_citas/paso07_compartir-cita.png "Compartir cita")

Al abrir el enlace el cliente (o nostros mismos para probar) podra ver la disponibilidad del equipo y reservar una cita en el horario disponible
![Calendario citas](../assets/img/07-calendario_y_citas/paso07_calendario-citas.png "Calendario citas")

Al clickar en un horario disponible, se nos abrirá un formulario para rellenar los datos de la cita y despues veremos la cita programada, donde el usuario podra añadirla a su calendario de google o outlook (en este caso usaremos google calendar para probar)
![Cita programada](../assets/img/07-calendario_y_citas/paso07_cita-programada.png "Cita programada")

Ahora podemos volver al calendario de Odoo y ver que la cita ya aparece en nuestro calendario
![Cita calendario](../assets/img/07-calendario_y_citas/paso07_cita-calendario.png "Cita calendario")

