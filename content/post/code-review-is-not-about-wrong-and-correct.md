---
title: 'Code Review Is Not About Wrong and Correct'
author: 'faultable'
tags: ['briefing']
date: 2019-07-10T03:17:47+07:00
draft: false
---

Karena review bukanlah revisi

<!--more-->

Dari beberapa feedback yang gue dapet seputar Code Review––karena gue sering "mengajak" member untuk
melakukan code review––adalah mereka merasa seperti "masih belum berpengalaman" dalam memahami
perubahan kode yang ada.

Simplenya, anggap gue melakukan perubahan terhadap iterasi untuk menampilkan tulisan yang bukan draft, misal seperti ini:

```javascript
let filteredData

for (let i = 0; i < datas.length; i++) {
  if (!!datas[i].draft !== true) filteredData.push(datas[i])
}

return filteredData
```

Lalu gue ubah menjadi seperti ini:

```javascript
const filteredData = datas.filter(data => !!data.draft !== true)

return filteredData
```

Perubahannya adalah:

```diff
+ const filteredData = datas.filter(data => !!(data.draft) !== true)
- let filteredData
-
- for (let i = 0; i < datas.length; i++) {
-   if (!!datas[i].draft !== true) filteredData.push(datas[i])
- }

return filteredData
```

Tujuan review yang gue lakukan adalah agar "team" sadar akan perubahan yang gue lakukan, sehingga
tidak perlu lagi mengeksekusi `git blame`. Mengapa agar sadar? Agar ketika terjadi _kekurang
pahaman_ atau lainnya, bisa langsung didiskusikan **langsung** (direct feedback) sebelum _move
on_ ke task selanjutnya.

Khususnya dibagian refactor (seperti diatas), kita sekaligus bisa sambil "mempelajari hal baru" bila
kita sebelumnya belum mengetahuinya. Misal, _kenapa gue ubah looping for menjadi filter?_

Misal jawaban gue: Pertama, untuk mengurangi "penghindaran" akan terjadinya side effect, kedua agar
membuat memory lebih efisien, ketiga untuk mengurangi jumlah baris kode, dan keempat agar
fungsional karena why not?

Gue bisa jawab karena gue yang **melakukan perubahan tersebut**. Dan ketika code review ini, team
bisa mempelajari sesuatu yang baru (bila belum familiar dengan itu sebelumnya), bisa memberikan
feedback langsung (misal bila mereka tau hal yang "lebih baik" dari yang gue ubah), dsb.

Ingat, tujuan kita bukanlah untuk "kode siapa yang paling bagus, pintar, dsb", kita tidak
mengejar **pengakuan**. Melainkan yang kita kejar adalah **problem solving** nya, seperti kasus
diatas misalnya yang gue coba untuk men-solve masalah efisiensi memori.

Oke kita sudah membahas seputar refactoring & code review, sekarang implementasi fitur & code
review.

Hampir 70% commit yang dilakukan adalah mengembangkan fitur, sisanya paling refactoring; Fix bug,
styling, dsb. Code review dalam proses pengembangan fitur **sangat penting** agar anggota tim tetap
singkron.

Gue sebisa mungkin selalu menghindari perubahan yang menyebabkan **breaking changes**, jika memang
tidak bisa dihindari, mau gak mau harus gue buat se-backward compatibility mungkin jika API yang
dibuat sudah bisa diakses oleh public.

Meskipun topik diatas seputar "Design Choice", yang mau gue bahas adalah di singkronisasi nya. Team
tetap tersambung dengan apa yang sedang dikerjakan oleh tim lain.

<img src="/media/posts/review.png" class="zoomable" />

Gambar diatas adalah contoh bagaimana gue melakukan "Huge (internal) refactoring" terhadap codebase,
dan gue melibatkan @ri7nz karena masalah Code Ownership, ada kode yang ditulis oleh @ri7nz dan
strukturnya gue ubah. Gue melibatkan dia untuk mereview, agar dia tau perubahan mana saja yang
terjadi dan berdampak, mengapa gue ubah, dsb.

## Tidak ada benar/salah

Yang ada hanyalah "Pilihan". Code Review sering kali dipandang sebagai proses "seperti ujian" yang
mana ada jawaban benar/salah, padahal Code Review lebih seperti proses "perkuliahan".

Diakhir sesi, hampir sama seperti dosen menanyakan: "Apakah ada yang kurang jelas?", ketika kita
merasa sudah jelas, kita bisa melakukan "Approve" terhadap apa yang kita review tersebut. Terhadap
apa yang kita pelajari di kelas perkuliahan tersebut.

Feedback harusnya selalu ada, namun perbandingannya bukan antara "benar atau salah", melainkan
tentang "baik dan lebih baik". Intinya, gue cuma mau menjelaskan bahwa proses Code Review bukanlah
tentang menyalah/membenarkan suatu perubahan, melainkan yaa melihat perubahan yang ada dengan hasil
akhir setuju/menolak.

Ada kondisi dimana Pull Request (Code Review biasanya dilakukan ketika PR, kan?) dianggap "closed",
mungkin karena perubahan yang terjadi terlalu banyak, terlalu menyebabkan banyak konflik terhadap
cabang lain, atau mungkin karena menyebabkan breaking changes yang tidak bisa ditoleransi.

## What I learned

Berdasarkan dari hasil PR yang sudah gue lakukan, kebanyakan PR gue seperti ini:

- Too much scope. Mengubah sesuatu namun skop nya terlalu luas
- Too few information. Kadang gue buat PR tanpa deskripsi yang jelas.
- Dictatorship. I assume everybody will agree with my changes

Berdasarkan dari pelajaran yang gue dapet tersebut––dan tentunya gue gak bakal dapet pelajaran kalau
gue gak melakukan kesalahan––di next PR gue akan melakukan:

- Only affected to one/two scope. Scope itu seperti fitur A, bug fix B, refactor C, dsb.
- Writing more verbose information. Kenapa gue ubah ini, apa yang gue tambahkan, dsb.
- Consensus. Everybody should _agree_ or _disagree_ with my changes. Not only one flow
  agreement/disagreement.

Dan gue harap bukan cuma gue aja yang melakukan 3 poin diatas khususnya, namun semua anggota tim.

## Please review

Jika kamu memiliki waktu luang, dan diberikan "tanggung jawab" untuk melakukan Code Review, please
review, okay? Jika belum memiliki waktu luang, bisa langsung _sounding_ yang intinya agar setiap
orang yang terlibat saling tau.

Setuju atau tidak setuju, intinya tidak ada proses benar/salah. Kalau kamu mungkin memiliki solusi
yang lebih baik, suarakan. Kalau kamu kurang/tidak setuju dengan perubahan yang ada, suarakan.
Kita disini untuk memecahkan masalah dan mencari solusi yang paling baik, bukan untuk menilai
kode dan pemikiran siapa yang paling benar/salah.

Kita mencari pengalaman & pengetahuan, bukan mengejar pengakuan. Apalagi mengejar ketidaktahuan dan
ketidak-enakan.

Enjoy your Wednesday.
