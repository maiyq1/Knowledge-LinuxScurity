#hackthebox #very-easy 
- FTP: File Transferer Protocol
- Puerto común usado para FTP: 21
- SFTP -> Secure FTP (versión segura de FTP)

# Haciendo los scans...
---
![[LabFawn1.png]]

- Versión de FTP: vsftpd 3.0.3
- OS de target: Unix

**IMPORTANTE**
Default username for FTP: anonymous
	-> no requiere contraseña
Error cometido por el target: Falta de configuración

***Accediendo al target mediante FTP***
![[LabFawn2.png]]

Listamos los archivos disponibles y vemos que está la bandera, pero al intentar leer con **cat** no se puede
![[LabFawn3.png]]

## OPCIÓN 1: Descargar el archivo a nuestro PC
Comando **get**
```
get flag.txt
```
![[LabFawn4.png]]

Luego, abrimos el archivo en el directorio
![[LabFawn5.png]]

## Opción 2: Leyendo con una alternativa a "cat"
Comando **less**
![[LabFawn6.png]] 