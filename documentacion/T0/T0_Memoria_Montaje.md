# MEMORIA MONTAJE VM

En este documento se va a hablar de cómo se ha hecho el montaje y su respectiva configuración sobre VirtualBox.

## Arquitectura y máquinas creadas

Dentro de VirtualBox se ha creado un grupo de VM para organizar mejor las máquinas. En total hay 14 máquinas; la función de cada una se va a explicar a continuación:

| TIPO | EQUIPO |
| :--- | :--- |
| **Comunicaciones** | MikroTik, ServerCom y OPNsense |
| **Almacenamiento y virtualización** | TrueNAS y Proxmox 1, 2 y 3 |
| **Dominio** | Windows Server 2025 |
| **Clientes** | WindowsCliente1, 2 y 3, DebianCliente4 y un Dual-Boot con Windows y Debian |
| **De apoyo** | Debian_Pruebas |

Se ha puesto un Debian de prueba para poder entrar y comprobar las interfaces gráficas de los servidores y configurar con más comodidad

## Instalación de las máquinas virtuales en el entorno de pruebas

### Creación de las máquinas
Se han creado las máquinas poniendo el SO correspondiente y asignando un disco VDI para cada VM con el espacio conveniente

### Asignación de interfaces
Se ha puesto en la mayoría de máquinas una interfaz en modo **Red interna**. En los servidores y servicios **OPNsense**, **MikroTik** y **ServerCom**, aparte de la **Red interna** que conecta a los clientes y otros servidores, se ha puesto una interfaz **NAT** para tener salida a Internet

