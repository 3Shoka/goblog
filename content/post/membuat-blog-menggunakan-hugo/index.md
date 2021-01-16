---
title: "Membuat Blog Menggunakan Hugo"
description: Langkah-langkah membuat blog menggunakan Hugo dengan theme Stack
date: 2021-01-16T08:54:30+07:00
categories:
    - Hugo
---

Berikut adalah langkah-langkah yang saya lakukan untuk membuat blog ini menggunakan [Hugo](https://gohugo.io/) dengan tema [Stack](https://github.com/CaiJimmy/hugo-theme-stack).

Hugo adalah salah satu static site generator yang populer saat ini (setidaknya saya mengetahui tentang Hugo ini ya karena memang sedang populer saat ini 😁️). Dan kenapa saya memilih tema Stack, karena saya suka saja dengan model card nya ini.

Pertama kali yang harus dilakukan adalah menginstall Hugo bisa dilihat [disini](https://gohugo.io/getting-started/quick-start/) dan selanjutnya menambahkan tema Stack bisa di dapat dari [sini](https://github.com/CaiJimmy/hugo-theme-stack).

{{< highlight bash >}}
# install hugo
pamac install hugo

# membuat site baru bernama 'goblog'
hugo new site goblog

cd goblog

git init

# menambahkan tema Stack, sebagai submodule git
git submodule add https://github.com/CaiJimmy/hugo-theme-stack/ themes/hugo-theme-stack

# copy folder content, plugins dan file config.yaml yang ada di folder themes/hugo-theme-stack/exampleSite ke direktori utama 'goblog'
cp -r {themes/hugo-theme-stack/exampleSite/content/,themes/hugo-theme-stack/exampleSite/plugins/,themes/hugo-theme-stack/exampleSite/config.yaml} .

# hapus file config.toml, kita akan menggunakan config.yaml dari bawaan tema Stack
rm config.toml

# tes jalankan server
hugo server
{{< /highlight >}}


Setelah jalankan server, web nya bisa dibuka di `http://localhost:1313/` jadi deh. Selanjutnya menyesuaikan file config sesuai kebutuhan.
