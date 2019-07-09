# PHP'De Güvenlik

## Dosya Ve Dizin Güvenliği 

```
htaccess 'e deny from all yazarsak kimse dosyamıza giremez 
Option -Indexes

#deny all access
deny from all
allow from 10.0.0.1 # tek ip adresi
allow from 192.168.0.0/24 # ip bloğu
ip bloğunu yazmak zorunda değiliz ip adresine de ipv4ü yazacağız.
```
