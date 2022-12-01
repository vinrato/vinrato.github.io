---
layout: post
title:  "Mengubah ZTE F609 Menjadi Access Point"
date:   2022-12-01 06:06:14 +0700
categories: jaringan
tag: Jaringan
---

![header_img](https://3.bp.blogspot.com/-78eqbDg8bDA/XpFfTrKM1bI/AAAAAAAAAms/9Jx6g8DyQYM0dddz0HJck1nDseTnDuRnQCNcBGAsYHQ/s1600/ztef609.jpg)

Salah satu cara memperluas jangkuan WiFi modem ZTE F609 Indihome adalah dengan menambahkan Access Point atau dalam bahasa indonesinya “titik akses”.

Terutama pada rumah dengan lebih dari dua lantai, untuk mengatasi area yang terhalang oleh dinding dan tidak dapat dijangkau, perlu ditambahkan Access Point (AP). Anda dapat menggunakan modem ZTE F609 untuk membuat Access Point. Anda dapat membelinya dengan harga berkisar antara Rp. 50.000,- hingga Rp. 100.000,- dengan kondisi bekas di markeplace macam Tokopedia. Selain itu, Anda memerlukan kabel LAN UTP dan laptop untuk mengkonfigurasi modem. Panjang kabel LAN UTP bisa diatur sesuai kebutuhan. Gunakan kabel LAN UTP ini untuk menghubungkan set modem sebagai titik akses ke sumber Internet. Sumber daya internet dapat berasal dari modem Indihome atau router mikrotik.

Untuk menjadikan modem ZTE F609 sebagai Access Point, ikuti langkah-langkah di bawah ini untuk mengaturnya:

**Reset dulu modem ZTE F609. Berikut cara reset modem wifi indihome ZTE F609:**

Tekan dan tahan tombol reset di bagian samping modem selama 5 hingga 10 detik.

![step1](https://www.nooblasto.com/wp-content/uploads/2021/09/cara-setting-modem-zte-f609-menjadi-acces-point.jpg.webp)

**Gunakan kabel UTP untuk menghubungkan port LAN ke laptop.**

Untuk konfigurasi alamat IP laptop 192.168.1.2 dan netmask 255.255.255.0

**Buka panel jaringan modem melalui browser.**

Masukkan URL di browser 192.168.1.1 dan tekan Enter.

Untuk masuk ke panel web modem, gunakan data administrator masuk ZTE F609 atau menggunakan data berikut:

{% highlight bash %}
user: admin
password: Telkomdso123
{% endhighlight %}

**Masuk ke pengaturan panel web modem ZTE F609. Jika berhasil login masuk ke web panel modem ZTE f609, muncul gambar berikut:**

![step_](https://www.nooblasto.com/wp-content/uploads/2021/09/cara-setting-modem-zte-f609-menjadi-acces-point-1.jpg.webp)

Masuk menu Network > LAN > DHCP Server.

Untuk pengaturannya, lihat gambar di bawah ini:

![step__](https://www.nooblasto.com/wp-content/uploads/2021/09/cara-setting-modem-zte-f609-menjadi-acces-point-8.jpg.webp)