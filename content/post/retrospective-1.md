---
title: 'Retrospective #1'
author: 'faultable'
tags: ['retrospectives']
date: 2019-06-25T20:22:45+07:00
draft: false
---

Our first retrospectives!

<!--more-->

Retrospektif ini dilakukan pada hari Selasa 25 Juni 2019 dan dihadiri oleh tim [Project
Nadya](https://github.com/orgs/evilfactorylabs/teams/nadya/members), antara lain:

- Afwa Bagas Wahuda
- Afrijal Dzuhri
- Kevin Anantha
- Randy Vianda Putra

Yang membahas seputar proses development terhadap project Nadya. Kesimpulannya, _bottleneck_ yang ada antara lain adalah:

- Bingung mulai dari mana
- Kurang familiar dengan tech stack yang digunakan
- Kurang pemahaman terhadap _user workflow_ terkait project yang sedang dikembangkan
- Takut merusak workflow yg udah dibangun
- Testing

Dan itulah alasan mengapa masih banyak [backlog](https://github.com/evilfactorylabs/nadya/issues)
yang belum tersentuh namun tetap dimonitor oleh tim. Sengaja masalah-masalah diatas kita tampung
dulu dan akan dibahas disini, bukan karena anti-feedback tapi agar setiap orang (baik internal
maupun external evilfactory) siapa tau memiliki permasalahaan yang sama juga, dan (siapa tau)
permasalahan tersebut bisa terselesaikan.

As always (we (evilfactory), especially me) is always welcome with feedback. Jika memiliki umpan
balik terhadap yang dibahas, feels free to tell it (via 1:1, #channel, or telegram if you are not
evilfactory member).

## Bingung mulai dari mana

Sejujurnya, pada dasarnya kita membuat evilfactory ini untuk menyelesaikan masalah tersebut, namun
di scope yang lebih luas:

> Membantu orang-orang, khususnya _entry-level_ atau yang memang baru ingin menjadi developer agar
> tidak bingung **untuk membuat apa**. Membantu membangun portfolio untuk anggota tim.

Sayangnya, ada 1 masalah yang belum gue fikirkan (meskipun sudah pernah dibahas oleh @ri7nz),
yakni: di bagian **bingung mulai dari mana**. Mungkin gue bisa menjawab pertanyaan "bingung membuat
apa", namun gue belum menyiapkan jawaban untuk pertanyaan "bingung mulai dari mana?".

I'm very sorry guys.

Dan berdasarkan ngobrol dengan anggota tim, ada beberapa jalan keluar terkait masalah ini. Ada yang
dengan cara _subjektif_ maupun _objektif_.

### Subjektif

Ada yang tipe nya _micromanage_. Sebelumnya juga gue pernah diskusi dengan @ri7nz seputar _micro
management_ ini, dan ya, ketika pertama kali beliau kerja di kantornya, awal-awal masih micro manage
dalam cakupan _task assignment_.

Dia di assign untuk melakukan task tersebut.

Dan ini bukan masalah, meskipun di [briefing pertama](/post/briefing-1/) yang gue harapkan kepada
member evilfactory adalah menjadi pribadi yang _self-driven_. Kenapa enggak gue jadikan masalah? Karena
gue melihat proses juga, enggak hanya selalu tentang input & output.

Selagi anggota tim melakukan tersebut secara _fun_ apalagi bukan sebagai beban, berarti bukan masalah.
Dan untuk cara ini (micromanage), akan gue terapkan kepada orang-orang yang memang _belum siap_ self-driven,
sampai orang-orang tersebut siap.

Jadi kesimpulannya, _"lu (nama orang) kerjain tentang (nama task)"_ alias berdasarkan dengan tunjukkan
gue, tanpa melupakan tingkat kompleksitas terhadap task tersebut.

### Objektif

Sekarang mari kita cari jalan keluarnya dengan melihat inti permasalahannya bukan secara subjektif.
Poin inti dari permasalahan ini adalah karena project ini kita buat dari nol dan benar-benar
**sangat** bergantung kepada **proses kreatif** kita.

Blueprintnya hanyalah spesifikasi software yang sudah dijelaskan di
[GitHub Discussion](https://github.com/orgs/evilfactorylabs/teams/nadya/discussions/1). Sorry guys
itu link internal hanya untuk tim Nadya.

Dan sayangnya, **otak** nya adalah gue. Hanya gue **persis nya** yang tau dari 0 sampai 1 nya tentang project
ini. Dan ini salah, (dan) gak boleh berkelanjutan terjadi.

Dan gue rasa, hampir setiap orang yang "awal nya" bingung mau buat apa, masalah selanjutnya adalah
"bingung mulai dari mana", dan gue baru sadar akan hal itu baru sekarang. Kecuali kalau lo emang
sudah kefikiran ingin buat apa, dan sudah kefikiran hasilnya akan bagaimana nanti. Thanks to your
creative idea.

Dan disini, ide dari project ini adalah dari gue. Beruntungnya, anggota tim siap bekerja sama untuk
mengerjakan project ini, karena project ini nantinya akan menjadi portfolio untuk anggota tim, sekaligus
menjadi aplikasi yang akan digunakan oleh anggota tim bila memang membutuhkan aplikasi ini.

Btw ada berapa "dan" pada bagian ini?

### Solusi

Berdasarkan diskusi yang sudah dilakukan di channel #nadya, jalan keluarnya adalah gue buat versi 1
nya. Dan anggota tim setuju. Solusi tersebut gue pilih agar kita bisa _connecting the dots_
between us terlebih dahulu. Project ini bukanlah milik gue, melainkan Tim Nadya. Karena kebetulan gue ada ide, gue
memberitahukan ide ini kepada anggota tim, dan anggota tim siap untuk bekerja sama membuat ide ini, jadi
itulah alasan mengapa kita dipertemukan~

PR gue (as a... let's just call it "lead" for short) adalah menyatukan pemikiran antar anggota tim.
Langkah awalnya adalah dengan merilis versi 1 canary (nanti akan gue bahas) by myself & @ri7nz.

Setelah aplikasi ini sudah bisa digunakan (in high-level view), gue harap setiap anggota tim
sudah benar-benar mengerti tentang aplikasi apa yang sedang anggota tim kembangkan, dan anggota tim bisa
mem-fix; meng-improve, dsb terhadap aplikasi tersebut, karena yang pertama anggota tim sudah tau
userflow nya secara high-level, dan kedua semoga pemikiran anggota tim sudah sync (terkait aplikasi ini) antar anggota.

Kesimpulannya, sikap kreatif memang harus terus dilatih. Kita tidak bisa memaksa orang lain ataupun diri kita
sendiri untuk kreatif, kecuali kita terus melatih cara kreatif kita. Karena "kreatif" terlalu luas,
dan dalam konteks ini, gue menuntut tim untuk _ber-kreatif dalam membuat_ padahal yang
diinginkan adalah mungkin untuk _ber-kreatif dalam mengembangkan_. Itulah alasannya mengapa masalah ini
terjadi.

Ada masa nya ketika kita sampai ke proses "_kreatif dalam membuat_", dan berdasarkan feedback yang
sudah diutarakan, mungkin kita belum siap untuk itu. Tell me if I am wrong. Terlebih kita tidak ada
proses brainstorming bersama untuk connecting the dots dari awal.

Dan gue yakin suatu saat nanti kita akan siap, setelah melewati beberapa latihan yang kita lakukan
sendiri terhadap pemikiran kita, cara kita berfikir, ber-eksplorasi, dan memandang sesuatu.
Something called "experience" will agree with that argument.

## Kurang familiar dengan tech stack yang digunakan

This is fine and probably my mistake. Yang perlu diingat, kita adalah tim riset. Dan Project Nadya
adalah implementasi dari hasil riset tersebut.

Lalu, dimana masalahnya?

Diktator yang riset tersebut! Ya, it's me.

### Masalah

Gue ingin riset tentang offline-first app, PWA reliability, dsb. Dan gue sudah menjelaskan itu ke
member tim, dan member tim setuju untuk gabung. Dan semoga having fun. Riset adalah tentang mencoba
sesuatu yang (mungkin) sebelumnya belum pernah kita lakukan, atau mungkin pernah kita lakukan namun
belum sampai terlalu dalam.

Masalah disini adalah tetang bagaimana cara gue (selaku pemilih tech stacks) untuk menjelaskan
tentang mengapa menggunakan teknologi X bukan Y, dan kenapa kita harus setuju untuk pilihan tersebut.

Mengapa gue bilang gitu? Karena **pemilihan** tech stacks dilakukan se-arah. Kita bisa aja dong
mungkin menggunakan Vue daripada React, menggunakan Firebase daripada PouchDB, dsb. Lalu berdiskusi
bersama tentang tech stack mana yang harus kita gunakan.

Dan ini menjadi PR juga untuk gue agar setidaknya kita bersama setuju akan pemilihan tech stack tersebut.

### Solusi

Ini sedikit sulit, karena pertama mungkin kita belum familiar dengan Firebase, sedangkan gue
sudah. Atau kita sudah familiar dengan Vue, sedangkan gue belum. Kenapa membandingkannya dengan gue?
Karena gue adalah orang dibalik mengapa menggunakan tech stack tersebut.

Dan ya, gue adalah orang dibalik mengapa kita mendapatkan masalah seputar "Kurang familiar dengan
tech stack yang digunakan". Blame fariz!

Jalan keluarnya ada 3:

1. **memaksakan** diri untuk mempelajari teknologi tersebut
2. **menghindari** sesuatu yang terkait dengan teknologi tersebut
3. **mengganti** tech stack yang sudah dipilih

Dan izinkan gue untuk menjawab masalah selanjutnya terkait 3 poin tersebut.

#### Memaksakan

Namanya dipaksa pasti enggak enak dong. Apalagi kalau ternyata kita tidak menyukai apa yang dipaksakan
tersebut. Meskipun konsep dasar tentang "kebiasaan" adalah:

```
dipaksa -> terpaksa -> terbiasa -> bisa -> biasa
```

Namun hal yang perlu dilihat disini adalah tentang "suka". Lu suka gak melakukan hal tersebut?
Merasa beban enggak terhadap pilihan yang ada? Kalau merasa beban, silahkan lanjut ke nomor 2. Jika
tidak merasa beban, pilih pilihan ini.

Dan ya, kalau lo tipe orang yang tidak bisa menjawab pertanyaan ini, gue sarankan untuk memilih
pilihan ini dengan dasar tentang konsep dasar seputar kebiasaan.

#### Menghindari

Ini cara paling mudah, namun seperti yang kita tau: masalah ada untuk diselesaikan, bukan untuk
dihindari. Dan masalah disini adalah tentang "kurang familiar". Ketika lo memilih cara ini, mau gak
mau lo harus terus menghindari tech stack yang sudah dipilih. Entah sampai lo memilih poin nomor 1 ataupun
poin nomor 3.

Dengan menghindari, kita bisa tetap senang dan merasa aman terhadap tech stack yang kurang familiar
tersebut. Dan dengan memaksakan, kita bisa mempelajari sesuatu yang baru, khususnya tentang tech
stack yang sudah dipilih tersebut.

You choose.

#### Mengganti

Baik, sebelum kita membahas lebih lanjut tentang poin ini, yang perlu kita ingat adalah tidak semua
solusi bisa menjadi _silver bullet_ terhadap setiap masalah. Kita tidak bisa **langsung** bilang:
_"Halaman kita lambat, kita perlu ganti jQuery dengan Vue"_. Karena ada hal lain yang perlu
diperhatikan, seperti:

- Effort yang dikeluarkan untuk proses pergantian tersebut
- Waktu yang dilakukan untuk proses pergantian tersebut
- Sumber daya yang digunakan untuk proses pergantian tersebut

Dan sebagainya seperti dimasalah _scalability_, _reliability_, dan ity-ity lainnya baik terhadap
user; developer, ataupun computer.

Bukannya menyelesaikan masalah, malah menambah masalah baru (technical debt salah satunya).

Sekali lagi, it's your choice. My PSA: Pilih nomor satu, agar kita dapat terbiasa berhadapan dengan
sesuatu yang kurang familiar dengan kita.

## Kurang pemahaman terhadap user workflow terkait project yang sedang dikembangkan

Ini mungkin sudah dijelaskan di bagian "Bingung mulai dari mana", namun akan gue jelaskan sedikit
seputar Canary version.

Semoga sedikit ya.

[Canary](https://martinfowler.com/bliki/CanaryRelease.html) version pada dasarnya adalah versi dari
suatu aplikasi yang tidak di rilis ke semua pengguna. Pada konteks ini, versi aplikasi khusus untuk
ditunjukkan kepada developer.

Apa bedanya dengan versi Beta? Singkatnya, versi beta adalah versi aplikasi yang sudah lolos
kualifikasi "menjadi beta". Sedangkan versi canary adalah versi yang benar-benar masih panas, masih
_fresh graduate_ klo bahasa mahasiswa, mungkin terdapat banyak bug, mungkin belum lulus uji test, dsb.

Alasan kita memutuskan untuk membuat "channel" canary untuk menyelesaikan masalah bagian pertama,
dan bagian ini. Alias, agar kita sudah mengerti high-level nya userflow aplikasi kita. Sehingga
ketika kita membuat feature baru (untuk v1 khususnya), fitur tersebut langsung bisa digunakan oleh
pengembang, dan bisa langsung mendapatkan feedback (enhancement, bug fix, dsb).

Dari sisi pengguna, agar pengguna bisa mendapatkan pengalaman yang "hampir" bug-free. Ya, kita
percaya setiap software pasti memiliki bug, namun setidaknya sudah lolos uji baik smoke test maupun
user acceptance test.

Branch `canary` ini menjadi branch default untuk project kita. Setiap membuat bug fix, feature baru,
dsb harus berdasarkan dari branch canary. Karena branch `canary` pun ter-singkron dengan branch
`master`, bedanya, branch `master` adalah branch versi "stable" dari software kita. Versi yang
dirilis untuk semua user, versi yang siap & layak untuk digunakan.

Kesimpulannya, kalau lu tim member project Nadya (ataupun external yang tertarik untuk develop
project ini), lu harus _stay in touch_ with this version. Nantinya, versi ini akan dirilis dibawah
domain https://canary.nadya.app. Jadi lu bisa coba-coba dengan software tersebut sekaligus memahami
userflow yang ada, dan userflow yang mungkin bisa dibuat menjadi lebih baik lagi.

## Takut merusak workflow yg udah dibangun

Sekali lagi gue ingatkan, kita ini tim riset. Tinkerer. Takut merusak bukanlah sifat seorang
Tinkerer. Meskipun kita dapat banyak belajar banyak dari suatu kesuksesan, dan gue yakin kita dapat
lebih banyak belajar juga dari suatu kegagalan.

Gue lebih sering mendengar "belajar dari kegagalan" daripada "belajar dari kesuksesan", IMO.

Yang salah adalah ketika kita mengulangi kesalahan tersebut, pada waktu yang salah. Kesalahan adalah
hal yang wajar, tergantung waktu ketika kita melakukan kesalahan tersebut. Gue ambil contoh, kagak
masuk kelas perkuliahan. Wajar, kan? Coba kalau lo gak masuk kelas perkuliahan ketika UAS, pasti jadi gak
wajar dong.

Kembali kepada konteks, merusak adalah salah satu kegiatan yang dihasilkan oleh bermain-main;
Tinkering.

Lihat, inovasi apa yang tidak dihasilkan dari sebuah kerusakan? Cracking, membuat developer untuk
lebih memperkuat security nya. Gadget rusak karena air, membuat pengembang gadget membuat fitur
gadget tahan air. Dsb, silahkan ambil contoh sendiri di kehidupan nyata.

Dan ingat, "kerusakan" dan "kesalahan" akan menjadi masalah karena waktu yang tidak tepat. Peretasan
pada bank mungkin akan melahirkan inovasi, ketika waktunya Hackathon/Hackday. Gadget rusak karena
air mungkin akan melahirkan inovasi, ketika pengujiannya terhadap milik pengembang sendiri.

Dan di evilfactory, maksud dari waktu yang salah adalah "ketika masalah tersebut terjadi
berulang-ulang". Kita gak peduli seberapa banyak kamu merusak, selagi tidak merusak sesuatu yang sama,
mengapa tidak? Maksudnya, _ngapain sih ngerusak ini terus, kan sudah tau hasilnya gimana.
Bukannya masih banyak hal lain yang belum pernah dirusak?_

Takut dirusak hanyalah untuk orang-orang yang berada pada zona nyaman. Status quo. Kalau lu ingin
berada di zona nyaman, gue rasa itu bukan tempatnya evilfactory.

## Testing

Mungkin ini sedikit _out of context_, karena pada dasarnya setiap retrospektif kita membahas seputar
"praktis" bukan "teknis" seputar development. Jangan terlalu menganggap testing seputar testing,
karena pada dasarnya banyak cara untuk melakukan testing.

Bedanya cuma di proses nya aja, ingin manual atau ter-otomasi. Anggap kita memiliki 20 userflow,
silahkan testing 20 userflow tersebut setiap suatu perubahan terjadi (bug fix, new feature, dsb) atau
silahkan buat proses testing tersebut otomatis, alias dilakukan oleh kode testing yang sudah kita
buat tersebut.

Menulis kode testing memang sedikit sulit, dimasalah mindset. Bila sebelumnya mindset kita "sebagai
developer", ketika menulis testing kita harus bertindak "sebagai user", sang pengguna aplikasi yang
kita kembangkan.

Masalah lain seputar testing adalah API, kita harus familiar dengan API yang ditawarkan baik oleh
testing framework maupun testing runner. Namun percayalah, mempelajari API lebih mudah daripada
mempelajari cara fikir user.

Harusnya, mungkin skenario test ditulis oleh _tester_, bukan _developer_. But, whatever. Kalau
tertarik dengan _menulis testing_, ya monggo. Kalau tertarik dengan _melakukan testing_ secara
manual, ya monggo.

Sejauh yang gue tau, hampir perusahaan besar (you know, the "enterprise") hampir menerapkan workflow
TDD dalam proses pengembangan. Singkatnya, developer harus menulis test terlebih dahulu sebelum
bisa menulis "kode untuk production". Yang berarti, mau tidak mau kita harus familiar dalam
pembuatan/penulisan _automated test_ demi mengikuti standar industri ataupun demi bisa bekerja di
perusahaan besar yang menerapkan TDD.

Sekali lagi, it's your choice. Disini kita mencoba untuk melakukan _automated test_, dari unit;
integration, mungkin sampai end-to-end. Kita bisa belajar bersama tentang bagaimana menulis test
dari hal-hal yang paling kecil, sampai ke yang paling besar (seperti e2e yang biasa nya untuk
menguji "userflow").

---

That's it! Sorry kalau terlalu panjang, karena memang semua ini yang ingin gue utarakan. Dan gue
harap, lu jangan _manut-manut_ aja terhadap apa yang gue sampaikan dan ternyata ada hal yang
tidak/kurang lo setujui.

Seperti biasa, lo bisa kirim feedback terhadap gue baik di #channel maupun 1:1 langsung ke gue.
Untuk non-member evilfactory, [telegram gue](https://t.me/faultable) masih yang lama kok.

Thank you!
