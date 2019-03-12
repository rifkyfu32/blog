---
title: "Hello Word, Hello Hugo!"
slug: hello-word
date: 2019-03-12T17:29:51+07:00
draft: false
meta:
    image: ""
    description: ""
---

Hello World!

ini adalah tulisan pertama di blog ini. Baru saja saya membuat blog
dengan Hugo. Sekarang lagi dikembangkan dengan tema [Hugo Bootstrap v4 Blog](https://github.com/alanorth/hugo-theme-bootstrap4-blog).

Saya memilih Hugo, karena rasanya lebih mudah dari pada Jekyll dan Octopress.
Meskipun saya belum mengerti bahasa pemrograman Go.

Saya menggunakan skrip dari [dokumentasi Hugo](https://gohugo.io/tutorials/github-pages-blog/) untuk melakukan deploy.
Karena saya tidak menggunakan _Continous Integration_ (CI). Jadi setiap
mau deploy harus eksekusi skrip tersebut. Berikut ini skripnya.

```bash
#!/bin/bash

echo -e "\033[0;32mDeploying updates to GitHub...\033[0m"

# Build the project.
hugo # if using a theme, replace by `hugo -t <yourtheme>`

# Go To Public folder
cd public
# Add changes to git.
git add -A

# Commit changes.
msg="rebuilding site `date`"
if [ $# -eq 1 ]
  then msg="$1"
fi
git commit -m "$msg"

# Push source and build repos.
git push origin master

# Come Back
cd ..

```

Sepertinya template atau tema yang saya gunakan ini terlihat masih berantakan.
Mungkin nanti, saya akan perbaiki.