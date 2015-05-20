---
layout: post
title: Cara Upgrade Memory VPS Ubuntu 14 Untuk Upload
date: 2015-05-06 16:27:31
disqus: y
---

Tergantung pada perusahaan web hosting yang Anda pilih dan paket yang Anda pilih , Anda masing-masing akan melihat batas upload file maksimum pada halaman Media Uploader Anda di WordPress . Bagi beberapa itu adalah serendah 2MB yang jelas tidak cukup untuk file media seperti ( audio / video ) . Kebanyakan gambar di bawah 2MB , sehingga baik untuk hanya gambar . Dalam artikel ini , kami akan menunjukkan cara untuk meningkatkan ukuran file upload maksimal di WordPress .

> Catatan : Ini adalah tutorial tingkat menengah . Ini mungkin tidak bekerja dengan beberapa host bersama dalam hal ini Anda harus meminta penyedia layanan hosting Anda untuk dukungan . Kami menggunakan HostGator , dan mereka lebih daripada membantu ketika datang ke masalah seperti ini .

### Theme Functions File

Ada kasus di mana kita telah melihat bahwa hanya dengan menambahkan kode berikut dalam file tema fungsi ini , Anda dapat meningkatkan ukuran upload :

{% highlight ruby %}
@ini_set( 'upload_max_size' , '64M' );
@ini_set( 'post_max_size', '64M');
@ini_set( 'max_execution_time', '300' );
{% endhighlight %}