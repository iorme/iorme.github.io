---
title:  "Menghitung Jumlah File Dengan Perintah Baris Linux"
date:   2015-10-21 20:50:00
description: Menghitung Jumlah File Dengan Perintah Baris Linux
---

Ada kalanya kita butuh untuk menghitung jumlah file yang ada pada sebuah folder. Salah satu cara yang paling mudah adalah dengan memadukan antara perintah "ls" dan "wc".

Menghitung total jumlah file dan folder:

```bash
$ ls -al | wc -l
```
 
Menghitung hanya file saja:
- dengan menyertakan yang hidden

```bash
$ ls -l | grep ^- | wc -l
```
- tanpa menyertakan yang hidden

```bash
$ ls -p | grep -v / | wc -l
```

Menghitung hanya yang directory saja:

```bash
$ ls -p | grep / | wc -l
```

Menghitung jumlah file yang nama file nya mengandung kata "saya"

```bash
$ ls -l | grep saya | wc -l
```

Menghitung jumlah file yang nama file nya tidak mengandung kata "saya"

```bash
$ ls -l | grep -v saya | wc -l
```

Sekian saja, karena kebetulan yang dibutuhkan saat ini hanya seperti perintah-perintah diatas.