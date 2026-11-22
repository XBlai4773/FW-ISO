# Memoria Backups

Se va a poner los backups donde están, como y que metodo.

## Mikrotik

Se ha hecho con la herramienta crontab para hacer las copias automáticas y las manuales. Los archivos de la configuración son dos: `.rsc` y `.backup`. El `.backup` es donde está toda la configuración del mikrotik para restaurar en el equipo local. Está almacenado en ServerCom para hacer la copia automática.

## OPNsense

Se ha hecho con la herramienta crontab para hacer las copias automáticas y las manuales. El unico archivo que hay para restaurar es `config.xml`. Tiene todo lo que es la configuración tipo usuarios, reglas del firewall. DHCP, etc.

## ServerCom

Se ha hecho con la herramienta crontab para hacer las copias automáticas y las manuales. Se ha elegido los archivos de `/etc` y `/var/log/` y para los datos de usuarios y otros datos `/home`.

## WinServer2025

Se ha hecho con la herramienta de Copias de seguridad de windows. Se ha agregado un VDI en el TrueNAS conectado al WinServer2025 como disco virtual, entonces las copias van a ese disco virtual el cual está dentro del TrueNAS y la información se pasa automáticamente.

## Proxmox1, 2 y 3

Se ha creado en el proxmox por vía web un espacio compartido entre el TrueNAS y el clúster entero. Y ya para automatizar las copias seleccionas el nombre del almacenamiento, se elije la hora en la que se va a hacer la copia y seleccionar el modo snapshot.