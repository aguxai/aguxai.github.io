---
layout : post
title : Flash Player Tidak Berfungsi Pada Opera Dan Chromium Di Arch Linux
---

Saya menemukan error ketika menjalankan game berbasis web pada opera dan chromium yang dimana game tersebut masih menggunakan
flash player, secara default opera dan chromium telah menyediakan flash player pada saat instalasi namun ketika dijalankan
flash player tidak berfungsi dengan semestinya, setelah di selidiki ada satu file yang missing yatu chromium pepper flash.

![Flash Player](https://articles-images.sftcdn.net/wp-content/uploads/sites/3/2017/07/flash-player-1024x576.jpg)

Image Source : https://adobe-flash-player.en.softonic.com

Dengan adanya masalah ini kita hanya perlu menginstall peper flash yang disediakan dalam official repository arch linux

**Permasalahan**

Ketika menjalankan aplikasi berbasis flash player di opera dan chromium maka akan menemui error yang berupa adobe flash player
tidak terdeteksi, padahal flash player secara default sudah terinclude ke dalam aplikasi opera dan chromium.

**Solusi**

Permasalahan muncul karena ada satu file yang missing pada opera dan chromium, yang secara tidak langsung sudah tidak tersedia
lagi pada official repository arch linux melainkan pada AUR repository.

**Penyelesaian**

Kita hanya perlu menginstall pepper flash dengan mengeksekusi via command atau via instalasi manual pada package.

**The Last World**

Mudah.

**Sumber**

https://wiki.archlinux.org/index.php/Browser_plugins
