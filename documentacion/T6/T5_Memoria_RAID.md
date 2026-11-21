# Configuración de los RAID

En este apartado se va a especificar la creación de los RAID.

Los RAID se han creado en el SvrComm, en el cual se han añadido 7 VDI más: 2 para el RAID 0, 3 para el RAID 5 y 2 para el RAID 1.

Para crear el RAID como tal hay que utilizar `mdadm` para asignar cada disco. Por ejemplo, para crear el RAID 0 sería seleccionar dos discos cualquiera, darles formato, y montarlo para que sea funcional. Lo mismo con el RAID 1 y el RAID 5 pero con más discos.

## Características y funcionamiento

| Característica | RAID 0 | RAID 1 | RAID 5 |
| :--- | :--- | :--- | :--- |
| **Discos mínimos** | 2 VDI | 2 VDI | 3 VDI |
| **Tolerancia a fallos** | No tiene, si falla uno de los dos se pierde la información | Si falla uno de los discos se puede recuperar. Tiene tolerancia alta | Si falla uno de los discos tiene bastante tolerancia |
| **Ventaja** | La velocidad de lectura/escritura es más rápida que con los otros | Tiene mucha disponibilidad y seguridad, duplica la información en los dos discos | Es una combinación entre los dos, aprovecha el espacio de los discos y tiene protección ante un fallo de disco |
| **Capacidad real** | Total | La mitad del espacio | Depende, en mi caso tengo 3 discos de 2GB, entonces son 4GB de espacio |