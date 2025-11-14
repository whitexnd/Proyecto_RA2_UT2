# 04 — PostgreSQL en Linux

Instalamos postgresql con el siguiente comando:
   ```bash
   sudo apt -y install postgresql
   ```

![Instalación PostgreSQL](../assets/img/04-postgresql_linux/paso04_instalar-postgresql.png "Instalación PostgreSQL")


Cuando haya finalizado el comando anterior ejecutaremos el siguiente comando para verificar que el servicio de postgresql está en funcionamiento:
```bash
sudo systemctl status postgresql
```