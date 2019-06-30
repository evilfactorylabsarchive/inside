---
title: 'Be Curious'
author: 'faultable'
tags: ['culture']
date: 2019-06-30T18:55:19+07:00
draft: false
---

on _"How to doing a Research?"_

<!--more-->

evilfactorylabs merupakan "tim" riset & development di bidang **modern** teknologi web. Di tulisan
ini gue akan berbagi tentang "value" yang ingin dibangun di evilfactory, yakni: Be curious. Yang
khususnya, tulisan ini akan membahas seputar "blueprint" yang digunakan oleh evilfactorylabs dalam
melakukan proses r&d, atau yang sering kita dengar dengan "litbang" (penelitian dan pengembangan).

## Face the problem

Hal pertama yang harus dimiliki adalah "hadapi sebuah masalah". Jika sesuatu tersebut bukanlah
sebuah masalah, jadikanlah sebuah masalah, selagi layak dijadikan masalah. Lihat, bagaimana
sulitnya membuat UI yang stateful? Lihat, bagaimana sulitnya membuat UI yang "reaktif" terhadap
interaksi user?

Lihat, bagaimana sulitnya mengatur state terhadap suatu DOM?

Atau, betapa ribet & kurang efektifnya proses _maintenance_ dan _development_ terhadap aplikasi
monolith?

Apakah hal-hal tersebut bukan suatu masalah? Tergantung. Mungkin bukan masalah ketika UI kita tidak
membutuhkan perubahan "real-time", atau aplikasi kita masih monolith karena memang yang mengerjakan
1-4 orang.

Namun beda cerita ketika, misalnya, tim sudah besar. Sedangkan kita ingin _ship fast_ tanpa
mengurangi _quality_ yang ada.

## What if?

Setelah kita menghadapi masalah tersebut, atau bukan masalah namun kita jadikan masalah (berdasarkan
pengalaman kita, contoh monolith tadi), silahkan penasaran: Bagaimana jika...

...aplikasi bisa dipecah menjadi lebih kecil, namun loosely coupled?

...membuat UI reactive, namun dengan low overhead?

...dan sebagainya

Ingat, kita tau "tujuannya" namun tidak tau "jawabannya". Pertanyaan simple didunia nyata seperti:
Bagaimana cara menempuh dari kos ke kampus selama 10 menit, tanpa terhindar macet. Apakah kita tau
jawabannya? Mungkin belum. Apakah kita tau tujuannya? Jelas, 10 menit & menghindari macet.

## Tinkering

Waktunya bermain-main, gue analogikan dengan real-life terlebih dahulu.

Gimana kalau gue naik gojek aja? Daripada harus naik motor, soalnya kalau macet gue suka kesel.

Gimana kalau gue jalan kaki lewat jalan tikus aja? Sekalian nyari jalan baru.

Dan sebagainya.

Dari situ, kita bisa mendapatkan insight baru.

## Measure

Ternyata, naik gojek lebih cepat namun lebih memakan biaya dari sebelumnya naik motor sendiri

Ternyata, lewat jalan tikus lebih cepat dan efektif! Sekaligus, gue dapet jalan yang lebih cepet
buat ke tempat ngopi favorit.

Dan sebagainya.

Gagal atau sukses, kita mendapat insight baru. Pengalaman baru. "Kegagalan" tersebut, bisa kita fix
atau biarkan. Begitupula dengan kesuksesan tersebut, bisa kita "kembangkan lagi" atau biarkan. Yang
penting, terukur.

"Coba-coba" yang tidak terukur, jatuhnya adalah menjadi "hanya iseng". Bukan tinkering.

## Take a choice

Setelah melewati 4 langkah tersebut, kita sudah mendapatkan insight. Waktunya memilih pilihan: Take
it or leave it?

Apakah A lebih X daripada B?

Dalam menentukan pilihan, kita harus memiliki beberapa variable dan parameter sebagai pembanding.

- Cost?
- Time?
- Resource?
- Effectiveness?
- Efficiencies?
- Dsb

Karena kita sudah memiliki variable & parameter tersebut (yang didapat dari 4 langkah yang sudah
kita lakukan), waktunya kita menentukan pilihan.

## Studi Kasus

Lihat aplikasi (web) yang ada saat ini, bagaimana kondisinya?

1. Sangat bergantung dengan jaringan
2. Tidak bisa beroperasi bila offline
3. Bergantung dengan API Endpoint dari backend
4. Tracking _every single_ thing we did
5. Memiliki pengalaman yang "kurang" untuk mobile web dibanding native

### What if?

1. Kita membuat aplikasi yang tidak bergantung dengan jaringan? (alias, network is optional)
2. Bisa beroperasi bila offline?
3. Tidak bergantung dengan API endpoint dari backend?
4. Tidak nge-track setiap langkah kita?
5. Memiliki pengalaman, yang setidaknya, bisa di adu dengan native mobile app?

Misal, karena alasan:

1. Reliable app but not reliable network
2. Aplikasi "dari dulu" dibuat untuk mempermudah pekerjaan manusia, bukan nambah ribet (internet
   required contohnya)
3. Agar "frontend" bisa bergerak lebih cepat, tanpa harus menunggu "backend" secara singkronous?
4. Karena alasan privasi?
5. Karena, why not?

### Tinkering

Kalau lo tim internal `@evilfactorylabs/nadya`, pasti sudah tau. Jika belum, tunggu kita mempublish
tulisan khusus yang membahas seputar tinkering ini :))

### Measure

Karena ini masih proses, jadi gue gak bisa cerita banyak tentang measure. Kalau kalian ingin tau,
yang gue ukur dari proses riset ini adalah:

#### Team

- Efficiencies. Bagaimana tim bisa "bergerak cepat" dengan tech stack choice yang ada
- Effectiveness. Bagaimana tim bisa "menyelesaikan" dengan resource yang ada, dan spesifikasi yang
  dibuat.
- Team work. Bagaimana tim bisa saling berkolaborasi antar tim tanpa gap dengan pengetahuan yang
  dimiliki.
- Connecting the dots. Bagaimana tim bisa "saling terhubung" sehingga mereka sudah biasa menghadapi
  sesuatu yang sudah familiar dengan mereka, dan sesuatu yang belum familiar dengan mereka.
- Goals oriented. Daripada harus ber-orientasi terhadap hasil, kita akan mencoba ber-orientasi
  terhadap goals. Goals disini konteksnya adalah "rilis".

#### User

- Reliability. Bagaimana user bisa membuat aplikasi kita dapat diandalkan.
- Effectiveness. Bagaimana user bisa menggunakan aplikasi kita, tanpa khawatir akan "disk space"
  yang minim dan "koneksi internet" yang kurang stabil.
- Privacy-related. Bagaimana user bisa "aware" bahwa data mereka aman (karena hanya berada di device
  mereka) dan bahwasannya aplikasi kita tidak tracking apa yang user lakukan (yang biasanya demi alasan
  optimasi UX)

Setidaknya untuk sekarang itu poin-poin yang ingin kita ukur. Untuk user, bagaiman bisa kita
mengukur sesuatu tanpa melakukan proses "pengintaian"? Jawabannya, ada di anonymous feedback. Gue
yakin "no news is good news" alias tidak ada feedback "buruk" berarti kabar baik untuk kita, user
merasa "netral" ketika menggunakan aplikasi kita tersebut.

Dan gue yakin, "great news is a gift" alias user memberikan feedback baik tanpa disuruh (apalagi
dipaksa) berarti user benar-benar menyukai aplikasi kita. Yang perlu kita lakukan adalah agar
mengubah response "netral" menjadi "happy", dan mengembangkan dari "happy menjadi happier".

Fyi, user akan selalu mengakses API endpoint update untuk mengetahui apakah ada update terbaru
seputar versi aplikasi yang digunakan itupun bila ada koneksi internet aja (dan pastinya ada koneksi).
Pengaturan tersebut bisa diganti ke "jangan cek update otomatis", atau malah "jangan pernah cek
update". Kenapa? Yaa karena itu aplikasimu, lo yang gunain. Bukankah lo merasa bebas melakukan
sesuatu, ketika lo _memiliki_ sesuatu tersebut, bukan?

---

Biasanya di setiap perusahaan/startup memiliki "departement" khusus untuk R&D, alias memisahkan
antara tim "Core product" atau tim "Operational", production things. Karena mereka memiliki
produk yang sudah berjalan dan stabil.

Mengapa membutuhkan tim R&D? Yaa karena agar perusahaan tersebut terus ber-inovasi, menciptakan hal
baru, membuat sesuatu menjadi lebih efektif & efisien, memperbaiki kesalahan yang ada, dsb.

Tim R&D di evilfactory berada dibawah naungan `evilfactorylabs`, yang member nya bisa di cek di
[GitHub](https://github.com/evilfactorylabs). Untuk tim yang berada dibawah naungan `evilfactory`
sendiri belum ada seorang pun, karena kita belum memiliki produk yang benar-benar sudah kita rilis.

Kesimpulannya, "Be curious" adalah salah satu "value" yang ingin kita bangun di kultur evilfactory.
Langkah awal yang dilakukan adalah membuat blueprint pertama (yang diatas studi kasus itu) agar
setidaknya kita tau cara riset, tujuannya, dan mengapa nya.

Riset pertama sudah dilakukan sekitar 2 minggu, dan progress nya untuk mencapai "stabil" sudah
hampir 80% (17% di code coverage, dan 3% di fitur penyempurna). Progress nya akan di share di
next tulisan. Riset ini akan dilakukan sekitar sampai Agustus, yang artinya, setelah Agustus kita
akan benar-benar di "development" nya, so, stay tune.

Thanks.
