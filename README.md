# Instalacion de Arhch Linux

## Load Keys
```
loadkeys la_latin1
```

## Conectarse a la red
```
ip link
```
Y despues utilizar 
```
iwctl
```
Lo primero es listar los dispositivos wifi
```
device list
```

Escaneamos las networks
```
station device scan
```
Para escanear las networks activas
```
station device get-networks
```
Conectarnos a nuestra red
```
station device connect SSID
```

## Actualizar el reloj del sistema
Utilizamos timedatectl para asegurarnos que sea mas preciso
```
timedatectl set-ntp true
```

## Particionar disco
```
fdisk -l
```

## Formatear las particiones
Para la particion raiz
```
mkfs.ext4 /dev/sdX1
```
Para la home "Si la pusiste"
```
mkfs.ext4 /dev/sdX3
```
Para la particion swap
```
mkswap /dev/sdX2/
swapon /dev/sdX2/
```

## Montar el sistema de archivos
Root
```
mount /dev/sdX1 /mnt
```
Home
```
mount /dev/sdX3 /mnt/home
```
