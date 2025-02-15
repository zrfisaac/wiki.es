<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->
<!-- # - version : zrfisaac.wiki.es.archlinux : 0.0.1 -->

<!-- # [ markdown ] -->
# Arch Linux

## Descripción
Arch Linux es una distribución ligera y de lanzamiento continuo para usuarios avanzados, que ofrece personalización completa y las últimas actualizaciones. Cuenta con Pacman y AUR para un amplio soporte de software.

---

## Índice
- Predeterminado
  - dd : `dd bs=4M if=/zrfisaac/repository/os/archlinux/archlinux-amd64.iso of=/dev/sda conv=fsync oflag=direct status=progress`
  - /etc/default/grub : `cryptdevice=UUID=7b927af8-fd64-4dcc-9c4e-a9819b6d150c:ZRFISAAC`
  - /etc/mkinitcpio.conf : `HOOKS=(base udev autodetect microcode modconf kms keyboard keymap consolefont block ` **encrypt** ` filesystems fsck)`
- [Shell](#shell)
  - [Medio de instalación USB](#medio-de-instalación-usb)

---

## [Shell](#índice)

### [Medio de instalación USB](#índice)

- usando `cat` :
```bash
cat /zrfisaac/repository/os/archlinux/archlinux-amd64.iso > /dev/sda
```

- usando `cp` :
```bash
cp /zrfisaac/repository/os/archlinux/archlinux-amd64.iso /dev/sda
```

- usando `dd` :
```bash
dd bs=4M if=/zrfisaac/repository/os/archlinux/archlinux-amd64.iso of=/dev/sda conv=fsync oflag=direct status=progress
```

- usando `tee` :
```bash
tee < /zrfisaac/repository/os/archlinux/archlinux-amd64.iso > /dev/sda
```

- usando `pv` :
```bash
pv /zrfisaac/repository/os/archlinux/archlinux-amd64.iso -Yo /dev/sda
```
