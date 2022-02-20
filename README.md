# **REDES1-PRACTICA1-G8**


### Leonardo Roney Martínez Maldonado - 201780044
### Cesar Leonel Chamale Sican - 201700634
###  Julio Enrique Wu Chiu - 201906180
### Marcos Enrique Curtidor Sagui - 201900874
---
---
## **CONFIGURACION DE LA VPCS**

| PASOS| DESCRIPCION| 
|-------------|------------------------|
| 1           | Colocar dispositivos nativos de GNS3 (Cloud, Ethernet switch y VPCS) |
| 2           | Click derecho en la VPCS y luego en Start |
| 3           | Abrir la consola de VPCS dandole doble click a la VPCS |
| 4           | Configurar el numero de ip, numero de mascara y el gateway|
| 5           | Escribir en la consola de VPC -> "ip 192.168.18.10 255.255.255.0 192.168.18.1"|
| 6           | Escribir en la consola de VPC -> "save" |
| 7           | Luego deben de conectar su VPC a su switch |
---


Se repitio estos pasos cada integrantes de grupo, donde cambia seria la configuracion de IP de la VPC que seria:
```sh
    # Coordinador
        ip 192.168.18.10 255.255.255.0 192.168.18.1
    # Compañero 2
        ip 192.168.18.20 255.255.255.0 192.168.18.1
    # Compañero 3
        ip 192.168.18.30 255.255.255.0 192.168.18.1
    # Compañero 4
        ip 192.168.18.40 255.255.255.0 192.168.18.1
```
---
---
## **CONFIGURACION DE LA VPN**
| PASOS| DESCRIPCION| 
|-------------|------------------------|
| 1           | Abrir consola de SSH |
| 2           | Ejecutar comando "sudo apt-get update" |
| 3           | Ejecutar comando "sudo apt-get upgrade"|
| 4           | Ejecutar comando "sudo wgethttps://cubaelectronica.com/OpenVPN/openvpn-install.sh"|
| 5           | Ejecutar comando "sudo bash openvpn -install.sh"|
| 6           | Ingresar la ip interna de la VM |
| 7           | Ingresar la ip externa de la VM |
| 8           | Seleccionar el protocolo (UDP) |
| 9           | Seleccionar el puerto (1194) |
| 10           | Seleccionar la DNS |
| 11           | Crear clientes para cada integrante |
| 12           | Descargar OPENVPN|
| 13           | Ejecutar el archivo .EXE |
| 14           | Aceptar termino y condiciones |
| 15           | Instalar software |
| 16           | Abrir el software|
| 17           | Importar el archivo .OVPN y conectar a la red|
---

* ## COORDINADOR -- 201700634
![nubes compañero 1](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/vpn_201700634.jpeg)

* ## COMPAÑERO 2 -- 201900874
![nubes compañero 2](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/VPN_201900874.png)

* ## COMPAÑERO 3 -- 201906180
![nubes compañero 3](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/VPN_201906180.JPG)

## **CONFIGURACION DE LAS NUBES**

| PASOS| DESCRIPCION| 
|-------------|------------------------|
| 1           | Colocar dispositivos nativos de GNS3 (Cloud, Ethernet switch y VPCS) |
| 2           | Click derecho en la Cloud y luego en Configure |
| 3           | Crear una configuración UDP Tunnel en el dispositivo cloud |
| 4           | Colocar en los puertos locales y remotos de manera invertidos|
| 5           | Colocar el la direcion ip que propociona el VPN en Remote host|
| 6           | Add, Apply y Ok|
| 7           | Luego conectar su switch a sus nubes |
---


* ## COORDINADOR -- 201700634
![nubes compañero 1](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/red_201700634.jpeg)

* ## COMPAÑERO 2 -- 201900874
![nubes compañero 2](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/red_201900874.png)

* ## COMPAÑERO 3 -- 201906180
![nubes compañero 3](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/Red_201906180.JPG)

* ## COMPAÑERO 4 -- 201780044
![nubes compañero 4](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/red_201780044.jpeg)
---
---
## **PINGS ENTRE LOS HOST**
| PASOS| DESCRIPCION| 
|-------------|------------------------|
| 1           | Hacer los anteriores pasos para cada integrante |
| 2           | Abrir la consola de VPC |
| 3           | Escribir en la consola -> "ping 192.168.18.20" |

El ping se hace para cada integrante de grupo menos con el ip de que hace el ping:
```sh
    # Coordinador -- IP=> 192.168.18.10
        ping 192.168.18.20
        ping 192.168.18.30
        ping 192.168.18.40
    # Compañero 2 -- IP=> 192.168.18.20
        ping 192.168.18.10
        ping 192.168.18.30
        ping 192.168.18.40
    # Compañero 3 -- IP=> 192.168.18.30
        ping 192.168.18.10
        ping 192.168.18.20
        ping 192.168.18.40
    # Compañero 4 -- IP=> 192.168.18.40
        ping 192.168.18.10
        ping 192.168.18.20
        ping 192.168.18.30
```

Si aparece el time es porque si se envio el paquete y aparece el timeout es porque no se envio el paquete

* ## COORDINADOR -- 201700634
![ping compañero 1](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/ping_201700634.jpeg)

* ## COMPAÑERO 2 -- 201900874
![ping compañero 2](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/ping_201900874.png)

* ## COMPAÑERO 3 -- 201906180
![ping compañero 3](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/Ping_201906180.JPG)

* ## COMPAÑERO 4 -- 201780044
![ping compañero 4](https://github.com/cesarchs/REDES1-PRACTICA1-G8/blob/main/img/ping_201780044.jpeg)