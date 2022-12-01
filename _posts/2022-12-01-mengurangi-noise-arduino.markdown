---
layout: post
title:  "Mengurangi Noise Pada Pin Analog Arduino"
date:   2022-12-01 06:06:14 +0700
categories: otomisasi
tag: Otomisasi
---

![arduino_img](https://images.theengineeringprojects.com/image/main/2018/06/introduction-to-arduino-nano-13.png)

Arduino Nano adalah suatu papan sirkuit pengembang berukuran kecil yang didalamnya sudah tersedia mikrokontroler serta mendukung penggunaan breadboard.
Arduino Nano khusus dirancang dan diproduksi oleh perusahaan Gravitech dengan menggunakan basis mikrokontroler Atmega328 (untuk Arduino Nano V3) atau Atmega168 (untuk Arduino Nano V2).

Pin analog pada arduino sangatlah sensitif terhadap perubahan tegangan. Saking sensitifnya, menyentuh dengan jari saja sudah cukup untuk merusak data analog yang masuk ke arduino. Untuk menyiasati masalah tersebut, kita akan menggunakan sebuah algoritma mean untuk menghitung nilai rata rata data yang dapat diambil dari pin analog arduino.

Berikut adalah sebuah snippet kode:

{% highlight cpp %}

int average(int pin, int sample)
{
  float values[sample] = {};
  float total = 0;
  
  for (int i = 0; i < sample; i++)
  {
    values[i] = analogRead(pin);
  }
  for (float value : values)
  {
    total += value;
  }
  return (int)(total / sample);
}

{% endhighlight %}

Kode diatas akan mengambil lebih dari satu iterasi (pengulangan) data dari salah satu pin analog arduino. Jumlah iterasi tersebut dapat di tentukan melalui parameter sample. Setelah mendapatkan data-data tersebut, lalu akan di jumlahkan semua nilai-nilai tersebut lalu kita bagi dengan jumlah sample yang kita gunakan.

Contoh pengapliaksiannya adalah sebagai berikut:

{% highlight cpp %}

void setup() {
  Serial.begin(9600);
}

int average(int pin, int sample)
{
  float values[sample] = {};
  float total = 0;
  
  for (int i = 0; i < sample; i++)
  {
    values[i] = analogRead(pin);
  }
  for (float value : values)
  {
    total += value;
  }
  return (int)(total / sample);
}

void loop() {
  Serial.println(average(A2, 200));
}

{% endhighlight %}