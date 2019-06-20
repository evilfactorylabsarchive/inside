---
title: 'Briefing #2'
author: 'faultable'
tags: ['Briefing']
date: 2019-06-20T17:54:07+07:00
draft: false
---

On workflow, about how we work.

<!--more-->

Seperti yang kita ketahui sebelumnya, _workflow_ kita sangat bergantung dengan GitHub. GitHub
menjadi tempat untuk menyimpan kode, sekaligus menjadi tempat bagaimana kita mengerjakan project
kita di evilfactory, khususnya project nadya.

Dalam halaman [about](/about) kita sudah menyebutkan bahwa kita _agile_.
[Agile](https://en.wikipedia.org/wiki/Agile_software_development) disini maksud kita adalah
"incremental", "iterative", dan fast. Bukan agile yang sudah kalian kenal dari SCRUM atau apapun itu.

Gue akan menjelaskan singkat bagaimana kita akan menerapkan agile-ish workflow dalam bagaimana cara kita
bekerja, tanpa harus mempelajari "lagi" hal-hal yang sudah kalian tau (GitHub Issues, GitHub
Projects, GitHub Milestone, dsb).

## Terminology

### Sprint

Gue mulai dari Sprint. Sprint singkatnya adalah sebuah proses yang berisi kumpulan pekerjaan yang dilakukan dalam
tenggat waktu yang sudah ditentukan. Seminggu, dua minggu, sebulan, tergantung waktu yang sudah kita
tentukan berdasarkan _task_ yang akan kita kerjakan pada rentang waktu tersebut.

Di GitHub, Sprint bisa direpresentasikan sebagai [Milestones](https://github.com/evilfactorylabs/nadya/milestones).
Milestone/Sprint mungkin yang menentukannya adalah **gue**, namun tenggat waktu; task yang
akan dikerjakan, dsb yang menentukannya adalah **seharusnya kalian**.

### Task dan Epic

Singkatnya adalah jenis "pekerjaan" yang akan kalian lakukan. Epic singkatnya adalah "sebuah
kumpulan" task, atau task yang dilihat secara high-level. "Membuat fitur untuk add subscription"
adalah salah satu contoh Epic, mungkin task-task nya adalah "Membuat UI untuk add subscription",
"Menulis fungsional test add subscription", atau "Membuat fungsi untuk add subscription".

Epic berguna untuk meningkatkan rasa "kolaboratif"/team work. Disisi lain teman mengerjakan
pembuatan UI, kita bisa membantunya, misal, dengan menulis fungsional test untuk add subscription
tersebut.

Task juga banyak ragamnya, bisa [Story](https://en.wikipedia.org/wiki/User_story)
(as a X I want to Y so Z), Bug (bugfix/hotfix), Improvement (enhancement/refactor), New Feature, dsb.

## The Workflow(s)

Selalu ingat dengan spesifikasi dari software yang akan kita buat, anggap spesifikasi tersebut
sebagai blueprint. Berdasarkan spesifikasi tersebut, nantinya bisa kita eksplor lebih lanjut selagi
tidak keluar dari koridor spesifikasi yang sudah ditentukan.

### Create Issue

Alias, plan the backlog.

Sprint backlog adalah GitHub Issues (Backlog) dengan Milestone (Sprint). Mungkin kita bisa membuat sebanyak
mungkin backlog, namun tetap yang kita fokuskan adalah ke Sprint backlog tersebut. Sisanya,
issues-issues/backlog-backlog tersebut berada di Icebox.

Singkatnya, backlog = issues. Hal-hal yang berkaitan dengan project. Fix bug, refactor, upgrade
infra, dsb. Jika dirasa task yang ingin dikerjakan tersebut terlalu besar cakupannya, mungkin bisa
dibuat sebagai Epic, lalu membuat task-task yang lebih kecil lagi berdasarkan epic tersebut.

Setiap orang bisa membuat Issue, dan setiap orang bisa "meng-assign" ke siapapun, berdasarkan
kesepekatan diantara kedua belah pihak. Membuat task dan di-assign ke diri sendiri pun welcome.

### Plan the sprint/miletone

Yang perlu diingat, _due date_ disini bukan berarti "Deadline", melainkan "Estimasi". Berguna untuk
mengukur performa kalian. Berapapun Issues/backlog yang ada, kita tetap fokus ke Sprint Backlog yang
ada.

Setiap issue/backlog memiliki estimasinya sendiri, biasanya estimasi dirancang dari tingkat
kompleksitas pekerjaan tersebut. Range nya, 1, 2, 3, 5, 8, 13, 21 (alias the fibonacci number).
Semakin besar, maka semakin kompleks.

Berguna untuk mengukur performa, produktifitas, dll.

Karena di GitHub Issue tidak ada cara untuk menambahkan Estimasi, maka silahkan tulis saja di
description (di GitHub Issue).

### The Retrospectives

Setiap seminggu sekali kita akan melakukan retrospectives, secara asingkronous. Mudahnya,
di retrospectives ini kita akan membahas "terkait performa", seperti "Apa yang kamu senangi dari
X?", "Apa yang kamu harapkan dari X agar Y?", atau "Bagaimana jika X? Bagaimana bila Y?", dan
sebagainya. Begitupula pertanyaan seperti "Apa yang menjadi bottleneck?".

Sebelumnya, ingat, kan? Kalau kita melakukan hal ini harus "Having Fun". Retrospectives berguna
untuk meningkatkan apa yang telah kita lakukan di sebelumnya, entah agar lebih produktif; efektif,
efisien, ataupun fun.

Retrospektif kita akan dipublish [disini](/tags/retrospectives), selain agar tim lain juga belajar
juga agar orang diluar project/diluar evilfactory juga belajar. Feels free to contact me if you
won't publish your "retrospectives".

Singkatnya, retrospektif mungkin sama seperti "ber-muhasabah".

### Repeat

Agile means iterative, right? But incremental. Membuat software prosesnya tidak akan pernah selesai.
PR nya adalah, bagaimana kita menyikapi tersebut agar setidaknya kita tidak merasa boring, apalagi
"tidak tertantang". And I think that is my chore, with your help of course.

## Demo

Mari kita analogikan. TL;DR nya ada dibagian ini. Kita baca specs dari software yang akan kita buat,
lalu kita membuat GitHub issue (backlog) dengan judul: "Membuat empty state screen". Tambahkan
"Labels" agar lebih mudah dipahami.

Siapakah yang seharusnya mengerjakan task tersebut? Apakah lo atau orang lain? Pastikan kalau orang lain,
kenapa dia, bukan lo?

Kasih estimasi terhadap task tersebut berdasarkan kompleksitasnya & kemampuan yang dimiliki diri
lo/orang lain.

Apakah task tersebut blocking/blocked issue lain? Kalau iya, mention issue lain tersebut.

Apakah ada task lagi? Misal, ada. "Bump React to 16.7" misal. Sama seperti pertanyaan sebelumnya,
namun disini ada tambahan: Apakah task tersebut berdampak kepada versi aplikasi kita? Misal (1.0.0)?
Jika iya, mention, ini memudahkan kita untuk perilisan aplikasi (menggunakan semver), sehingga kita
bisa merelease versi baru tersebut (1.0.1) ke end user dengan changelog terkait.

Ingat kita akan publish ini ke playstore, kan?

Lanjutkan proses tersebut sampai benar-benar "cukup" untuk sprint kita. Dan gue rasa, lo semoga udah
mengerti apa itu Epic, kalau belum, feels free to DM me.

Due date sprint ditentukan oleh kita bersama. Dan setiap Sprint, harus memiliki goal. Contoh
singkatnya, _pada sprint ini, user bisa menambahkan subscription dan sekarang bisa login via email_. Itu termasuk goal, kan?

## Current State

Gue sudah membuat 8 issues di GitHub. Untuk sekarang, sebagai gambaran, sudah ditentukan beberapa
pointnya, seperti:

- Due date milestone (Sprint) sekitar 8 hari. 17-24 june
- Sprint Backlog (8 issue tersebut, I'm sorry)
- Estimasi per-task (dari yang paling kecil yakni 1, dan yang paling besar: 8)

Perlu perhatikan, point-point diatas, didapat **berdasarkan kapabilitas gue** terhadap task yang ada. Bukan dari
**kapabilitas lo**. Maka dari itu gue gak nge-assign siapapun. Kecuali si Kevin, buat ngetest. Sorry Kev,
haha.

Silahkan apakah kalian ingin kerjakan task tersebut pada Sprint sekarang atau menunggu next Sprint
dan membuat task sendiri. Workflow ini hanya sebagai "baseline", karena yang paling penting adalah
_[you should having
fuuun.](https://open.spotify.com/track/4wsMIV7XbRRmvMtqNAnY4k?si=I5ZUwW13RR2njZjDPdbUcg)_

Once again, feels free to DM me if you have any question, thanks.

P.S: Basically gue pakai [ZenHub](https://zenhub.com), "layer" diatas GitHub untuk Project
Management. Kasih tau gue aja kalau lo pakai juga. ZenHub hanyalah tools, semuanya kembali ke
"fundamental" kita dalam memanage project.
