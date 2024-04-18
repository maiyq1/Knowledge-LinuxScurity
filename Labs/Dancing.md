- Tipo de máquina: Windows
- SMB
- IP target: 10.129.214.147

# *Parte teórica*
---
- SMB: Server Message Block
	- Protocolo de comunicación usado para compartir archivos, impresoras, puertos seriales y diversas misceláneas de comunicación entre los nodos de una red
	- Componentes
		- Server
		- Workstation
	- Common port: 445

# Scans
---
- Servicios
	- `nmap -sV 10.129.214.147`
	- 135/tpc: msrpc (Microsoft Windows RPC)
	- 139/tcp: netbios-ssn (Microsoft Windows netbios-ssn)
	- 445/tcp: microsoft-ds
- Parámetro para listar usando `smbclient`: `-L`
	- Sirve para lista los Shares
		- Son carpetas o recursos específicos en un server SMB que están disponibles a clientes SMB a través de la red
- Cantidad de shares en el target: 4
		![[LabDancing1.png]]
- Nombre del share al cual somos capaces de acceder con la contraseña en blanco: WorkShares
	- Porque este este es un share customizado
		![[LabDancing2.png]]
- Comando para descargar un archivo en un server SMB: `get`
### Obteniendo la flag
A falta del comando `cat`/ `less`, deberemos descargar el archivo con `get` y leerlo de manera local
![[LabDancing3.png]]
- flag.txt: 5f61c10dffbc77a704d76016a22f1664