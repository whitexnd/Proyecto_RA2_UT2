# 11 — Problemas comunes (FAQ)

- **Puerto 8069 ocupado** → Cambia puerto en `odoo.conf` o libera el actual.
- **PostgreSQL no accesible** → Revisa servicio, roles y permisos.
- **wkhtmltopdf no compatible** → Instala versión recomendada para tu Odoo.
- **Permisos/propiedad** → Ajusta dueños (`odoo:odoo`) y permisos de rutas.
- **Servicio falla al arrancar** → Revisa `journalctl -u odoo` y `odoo.log`.

Cualquier problema lo podemos encontrar en los logs de Odoo ubicados en `/var/log/odoo/odoo.log` o consultando el estado del servicio con `sudo systemctl status odoo` y buscar en la documentacion oficial de Odoo o en foros especializados.
