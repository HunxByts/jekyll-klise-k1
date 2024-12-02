---
layout: post
title:  "Apa Itu Bug XSS Reflected"
date:   2024-11-30 21:13:20 +0700
categories: jekyll update
usemathjax: true
---


**BUG XSS REFLECTED**

adalah salah satu jenis celah keamanan pada aplikasi web yang memungkinkan hacker menyisipkan skrip [Html atau Javascript]() berbahaya ke server lalu di pantulkan kembali melalui respone pengguna pada browser.

**PAYLOAD XSS REFLECTED YANG SERING K1LLU PAKE**

- `<script>alert(document.domain)</script>`
- `<script>alert(document.cookie)</script>`
- `<script>alert("hacked_by_k1llu")</script>`

**PARAMETER YANG SERING TERDAMPAK XSS REFLECTED**

Apa saja sih parameter yang sering terdampak celah ini ??

- `search=`
- `query=`
- `cari=`
- `returnUri=`
- `page=`
- `Dll`

**BAGAIMANA CELAH INI DAPAT TERJADI**

Celah ini terjadi karena kurang nya validasi pada inputan/parameter pengguna, dengan tidak dilakukan validasi maka server akan mengeksekusi skrip [Html atau Javascript]() yang di berikan.

*CARA ATASI CELAH INI GIMANA ?*

- Menggunakan htmlspecialchar atau htmlentities
- Melakukan validasi inputan seperti ( <>/() )

rill case yang sering K1llu temuin :
`https://targetweb.go.id/berita.php?cari=<script>alert(document.cookie)</script>`

![lihat xss](/assets/img/rxss.png)

mungkin itu saja yang dapat K1llu sharing semoga bermanfaat.

_Jaga Ruang Siber_
