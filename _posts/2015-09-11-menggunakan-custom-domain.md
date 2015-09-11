---
layout: post
title:  "Menggunakan Custom Domain Pada Github Pages"
date:   2015-09-11 10:00:00
categories: github subdomain jekyll
---
Blog ini sebenarnya diletakan di github dan menggunakan [jekyll](http://jekyllrb.com/) sebagai engine nya. Tapi karena domain yang disediakan oleh github saya rasa kurang keren maka lebih baik diganti menggunakan subdomain dari domain pribadi saya yaitu [harry.yunanto.net](http://harry.yunanto.net).

Caranya mudah saja, dengan menambahkan cname di dns servernya, kebetulan untuk dns saya menggunakan layanan [cloudflare](http://cloudflare.com/), maka tambahkan di cloudflare nya dengan alias ke iorme.github.io. Dan saat dibuka ternyata error 404, halaman tidak ditemukan :))

Setelah mencari kesana kemari, ternyata solusinya simpel saja. Cukup tambahkan file dengan nama CNAME ke dalam root repository blog nya kemudian diisi dengan custom domain yang akan digunakan. Dan voila sukses.

> Happy Blogging
