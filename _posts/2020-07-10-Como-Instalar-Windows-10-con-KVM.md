- [x] Instalar kvm
- [ ] Descargar la imagen de Windows 10
- [ ] instalar windows
https://www.youtube.com/watch?v=2WDASJ0ye0A&ab_channel=EF-LinuxMadeSimple
https://getlabsdone.com/10-easy-steps-to-install-windows-10-on-linux-kvm/

#¿Como instanlar windows 10 en debian 10 con KVM?
Luego de intentar instalar virtualbox varias veces a traves del apt y solo encontrar errores en los repositorios decidi dejarme llevar por la sugerencia del documento del paquete de instalar qemu el cual utilice en mis años de universidad un par de veces y po esa razon me dio curiosidad. Buscando en internet econtre el siguiente tutorial https://www.linuxtechi.com/install-configure-kvm-debian-10-buster/ que nos permite utilizar KVM en debian 10:
## ¿Que es KVM?
Son las siglas para **Kernel-Based Virtual Machine** y es una solucion para la virtualizacion en linux y esta usa una version modificada de **qemu**
- Instalacion de KVM
```
sebas@LABURRITA:~$ sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virtinst libvirt-daemon virt-manager -y
```
- verificamos si el servicio esta arriba
```
sebas@LABURRITA:~$ sudo systemctl status libvirtd.service
```
<pre>
<font color="#8AE234"><b>●</b></font> libvirtd.service - Virtualization daemon
   Loaded: loaded (/lib/systemd/system/libvirtd.service; enabled; vendor preset: enabled)
   Active: <font color="#8AE234"><b>active (running)</b></font> since Thu 2021-07-08 10:46:07 -04; 6min ago
     Docs: man:libvirtd(8)
           https://libvirt.org
 Main PID: 26627 (libvirtd)
    Tasks: 17 (limit: 32768)
   Memory: 17.3M
   CGroup: /system.slice/libvirtd.service
           └─26627 /usr/sbin/libvirtd
</pre>
