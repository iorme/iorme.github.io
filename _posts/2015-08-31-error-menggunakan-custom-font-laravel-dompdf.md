---
layout: post
title:  "Error Menggunakan Custom Font laravel-dompdf"
date:   2015-08-31 14:27:00
categories: laravel pdf laravel-dompdf php
description: Kasus nya terjadi saat menggunakan custom font pada view yang ingin di convert menjadi pdf dengan menggunakan library laravel-dompdf
---

Kasus nya terjadi saat menggunakan custom font pada view yang ingin di convert menjadi pdf dengan menggunakan library [laravel-dompdf](https://github.com/barryvdh/laravel-dompdf)

```css
@font-face {
  font-family: 'CustomFont';
  src: url('path/fonts/CustomFont.ttf')  format('truetype')
}
body{
  font-family: 'CustomFont';
}
```

Saat dijalankan terjadi error sebagai berikut:

```
ErrorException in font_metrics.cls.php line 343:
file_put_contents(/srv/tms/storage/fonts/7dbf6e66e752b847a17e2c05e16c8d94.ttf): failed to open stream: No such file or directory
```
Error ini terjadi karena folder fonts tidak ada, sehingga untuk solusinya bisa dengan membuat folder fonts di dalam folder storage:

```bash
$ mkdir storage/fonts
$ chmod -R 777 storage-fonts
```

Setelah itu jalankan lagi halaman convert pdf nya.
