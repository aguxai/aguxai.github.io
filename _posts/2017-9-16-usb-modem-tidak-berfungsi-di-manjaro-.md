---
layout: post
title: USB Modem Tidak Berfungsi Di Manjaro
---

Manjaro tergolong distro yang 'fastest growing' yang dimana distro linux ini berkembang sangat pesat pada release-release sebelumnya,
namun distro ini menurut saya masih meninggalkan fitur yang menurut saya sangat penting untuk ditindak lanjuti dan dimasukkan
ke dalam update selanjutnya yaitu usb_modeswitch.

![lsusb usb_modeswitch](https://raw.githubusercontent.com/aguxai/aguxai.github.io/ce847fef5a38647b315b49322ae38e9a96984b85/_posts/images/Screenshot_2017-09-16_22-58-47.png)

Secara default, usb_modeswitch sudah terinclude ke dalam beberapa distro linux populer lainnya seperti halnya Ubuntu, Fedora, Debian,
dan lainnya, saya tidak akan menjelaskan spesifik tapi dari point yang dituju biar lebih efisien.

**Permasalahan**

Ketika mencolokan usb modem network manager applet tidak menunjukkan konektivitas mobile broadband seperti sinyal dari provider dan profil
dari mobile broadband itu sendiri, ketika ditindak lanjuti melalui eksekusi command 'lsusb' maka pesan yang muncul bukan networkcard
melainkan storage.

**Solusi**

Permasalahan muncul karena kita membutuhkan sebuah switch atau memindah dari storage mode ke dalam networkcard mode yang dimana
fungsi dari kedua hal tersebut memang berbeda, storage mode yaitu file bawaan dari modem untuk instalasi pada windows dan mac,
file ini secara default terkunci sama halnya sepeti DVD-R yang satu kali burning data secara permanen tidak akan bisa dihapus. Networkcard
mode yaitu yang dimana fungsi ini untuk mengakses internet.

Nah yang kita butuhkan adalah networkcardnya karena kita butuh untuk mengakses internet, maka untuk itu kita membutuhkan software
yang digunakan untuk memindah dari storage mode ke dalam networkcard mode, software ini adalah usb_modeswitch.

**Panduan Instalasi**

Sama halnya package manager, seperti fedora berbasis .rpm. debian dan ubuntu berbasis .deb, arch linux mempunyai package yang berbasis
tar.xz, panduan yang saya bahas di paper ini adalah panduan yang mudah bukan panduan yang sulit yang dimana kita harus mengcompile
source dan menginstallnya, tapi wajib memiliki dependencies, oh tar.xz ini juga membutuhkan dependencies untuk bisa melakukan
instalasi, maka kita harus membutuhkan dependencies dulu sebelum mengeksekusi software tersebut.

1. Hal pertama, kita membutuhkan dependencies dari usb_modeswitch yang bernama tcl.
..* x86_64 : [Tcl Programming Language x86_64](https://www.archlinux.org/packages/extra/x86_64/tcl/)
..* i686 : [Tcl Programming Language i686](https://www.archlinux.org/packages/extra/i686/tcl/)
2. Setelah dependencies berhasil di install maka kita bisa menginstal usb_modeswitch.
..* x86_86 : [usb_modeswitch x86_64](https://www.archlinux.org/packages/community/x86_64)
..* i686 : [usb_modeswitch i686](https://www.archlinux.org/packages/community/i686/usb_modeswitch/)
3. Selesai.

**Penutup**

Mudah sekali kan instalasinya, bagi yang menemukan error silahkan post di forum manjaro, ingat bedakan achitecture i686 dan x86_64
jangan install architecture i686 di x86_64 atau sebaliknya hal ini akan menemukan error tentang kompatibilitas, i686 adalah 32 bit dan
x86_64 adalah 64 bit.

**Sumber**

* [Manjaro Packages](https://www.archlinux.org/packages/)
* [usb_modeswitch official website](http://www.draisberghof.de/usb_modeswitch)
* [Arch Linux Wiki](https://wiki.archlinux.org/index.php/USB_3G_Modem)
