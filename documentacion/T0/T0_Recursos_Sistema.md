# Recursos del Sistema

Aquí se van a plasmar los recursos que tiene cada sistema y los problemas encontrados y solucionados.

---

## Recursos asignados a cada máquina

| Máquina | Almacenamiento | Red | Especificaciones |
| :--- | :--- | :--- | :--- |
| **MIKROTIK** | VDI con 128 MB | Dos interfaces: una NAT que da al exterior y una Red interna que es la LAN. | RAM 1 GB, SO Linux x64 |
| **OPNsense** | VDI de 16 GB | Dos interfaces: una NAT que da al exterior y una Red interna que es la LAN. | 4 GB de RAM, SO FreeBSD |
| **ServerCom** | VDI de 20 GB | Dos interfaces: una NAT que da al exterior y una Red interna que es la LAN. | 5 GB de RAM, SO Debian x64 |
| **TrueNAS** | VDI de 32 GB para el SO y otro VDI de 2 TB para copias de seguridad | Única interfaz: Red interna. | 8 GB de RAM, SO FreeBSD |
| **Debian_Pruebas** | VDI de 20 GB | Única interfaz: Red interna. | 7 GB de RAM, SO Debian x64 |
| **Proxmox** | VDI de 60 GB | Única interfaz: Red interna. | 4 GB de RAM, SO Debian x64 |
| **WinServer2025** | VDI de 70 GB | Única interfaz: Red interna. | 8 GB de RAM, SO Windows Server 2025 |
| **Dual-Boot** | VDI de 100 GB | Única interfaz: Red interna. | 8 GB de RAM, SO Windows 11 |
| **WindowsCliente1** | VDI de 80 GB | Única interfaz: Red interna. | 8 GB de RAM, SO Windows 11 |
| **DebianCliente4** | VDI de 40 GB | Única interfaz: Red interna. | 4 GB de RAM, SO Debian x64 |

---

## Problemas obtenidos con soluciones

| Problema | Solución |
| :--- | :--- |
| Error al arrancar el sistema: dos sistemas de virtualización ejecutados al mismo tiempo. | Matar uno de los dos procesos de virtualizado y dejar solo uno. |
| La pantalla se queda en negro. | Una posible solución es comprobar que el sistema operativo puesto sea el correcto o revisar el controlador de la pantalla de la máquina. |
