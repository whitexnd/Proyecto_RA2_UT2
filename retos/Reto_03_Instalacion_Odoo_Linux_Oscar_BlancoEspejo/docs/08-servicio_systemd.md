# 08 — Servicio systemd (`odoo.service`)

1. Creamos el servicio en `/etc/systemd/system/odoo.service` (sudo nano /etc/systemd/system/odoo.service) con el siguiente contenido:
   ```ini
   [Unit]
   Description=Odoo Service
   After=network.target postgresql.service

   [Service]
   Type=simple
   User=odoo
   Group=odoo
   ExecStart=/opt/odoo/venv/bin/python /opt/odoo/odoo-src/odoo-bin -c /etc/odoo/odoo.conf
   Restart=on-failure

   [Install]
   WantedBy=multi-user.target
   ```

![Creación del servicio](../assets/img/08-servicio_systemd/paso08_crear-servicio.png "Creación del servicio")

2. Recargamos y arrancamos:
   ```bash
   sudo systemctl daemon-reload
   sudo systemctl enable --now odoo
   sudo systemctl status odoo
   ```

![Estado del servicio Odoo](../assets/img/08-servicio_systemd/paso08_status-odoo.png "Estado del servicio Odoo")
