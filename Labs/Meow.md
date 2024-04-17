#hackthebox #very-easy
Primera parte: Preguntas teóricas

- **VM**
	 Virtual Machine
- **Terminal**
	 Tool para interactuar con el OS mediante ordenes con comandos
- **openvpn**
	 Tool para conectarse con un archivo .vpn
- **ping**
	 tool para testear conexión entre nosotros y el objetivo mediante solicitudes ICMP
- **nmap**
	 tool para encontrar puertos abiertos en un target
- **root (telnet)**
	 username que permite hacer login en el target a través de telnet sin contraseña

Nos piden el nombre del servicio que corre en el puerto 23:

![[LabMeow1.png]]

Entramos a traves del servicio **telnet** al objetivo, luego usamos el usuario **root**

![[LabMeow2.png]]

Hacemos un listado para ver si la flag está en el mismo dir, y luego lo leemos con **cat**

![[LabMeow3.png]]