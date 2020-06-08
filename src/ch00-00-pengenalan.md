# Pengenalan

> Catatan: Buku edisi ini sama dengan [The Rust Programming
> Language][nsprust] tersedia dalam bentuk print dan format ebook
> dari [No Starch
> Press][nsp].

[nsprust]: https://nostarch.com/rust
[nsp]: https://nostarch.com/

Selamat datang di *Bahasa Pemrograman Rust*, sebuah buku pengenalan tentang Rust.
Bahasa pemrograman Rust akan membantu mu menulis software yang lebih cepat dan
dapat diandalkan. Ergonomis level tinggi dan kendali level bawah sering menjadi
permasalahan dalam rancangan bahasa pemrograman; Rust menantang konflik ini. 
Dengan menyeimbangkan kapasitas teknis yang kuat dan pengalaman yang bagus bagi 
pengembang, Rust memberi kamu opsi untuk mengkontrol detil level bawah (seperti 
penggunaan memori) tanpa merasa terganggu hal yang biasanya dekat dengan kontrol
seperti itu.

## Untuk siapa Rust ditujukan

Rust adalah pilihan ideal bagi sebagian orang karena alasan yang beragam. Mari 
kita lihat sebagian grup yang penting

### Tim dari Pengembang/Developer

Rust telah membuktikan menjadi alat yang produktif untuk kolaborasi diantara
tim pengembang yang mempunyai beragam tingkat pemahaman di bahasa pemrograman sistem.
Kode "level bawah" rentan dari berbagai variasi bug yang rumit, dimana untuk sebagian
besar bahasa pemrograman hanya bisa ditangkap dengan pengetesan yang ekstensif dan
penilaian kode dengan seksama oleh pengembang yang berpengalaman. Di Rust, *compiler*
memainkan peranan penting sebagai penjaga gerbang dengan menolak kompilasi kode yang
mempunyai bug yang tidak nampak, termasuk bug konkurensi. Dengan bekerja bersama *compiler*,
tim dapat menggunakan waktunya untuk fokus dalam logika program daripada mengejar bug.

Rust juga membawa peralatan pengembang yang kontemporer untuk dunia bahasa sistem:

* Cargo, pengelola dependensi dan alat pembangun yang disertakan, menjadikan 
  menambahkan, kompilasi, dan mengelola dependensi tidak menyakitkan dan konsisten
  di seluruh ekosistem Rust.
* Rustfmt menjaga gaya pemrograman yang konsisten untuk seluruh pengembang.
* Server Bahasa Rust menyediakan integrasi *Integrated Development Environment* (IDE)
  untuk penyelesaian kode dan barisan pesan error.

Dengan menggunakan ini dan alat yang lain di ekosistem Rust, pengembang dapat
menjadi produktif sambil menulis kode dengan level sistem.

### Pelajar

Rust ditujukan untuk pelajar dan bagi yang tertarik belajar tentang konsep 
sistem. Menggunakan Rust, banyak orang telah memahami tentang topik seputar
pengembangan sistem operasi. Dengan komunitas yang sangat ramah dan senang
untuk menjawab pertanyaaan pelajar. Dengan usaha seperti buku ini, Tim Rust
menginginkan konsep sistem menjadi lebih terbuka kepada orang yang lebih banyak,
khususnya yang baru dalam pemrograman.

### Perusahaan

Ratusan perusahaan, besar maupun kecil, menggunakan Rust didalam produksi demi
berbagai macam tugas. Tugasnya termasuk peralatan lini perintah, layanan web, 
peralatan DevOps, peralatan *embedded*, analisis dan transcoding audio dan video,
mata uang crypto, bioinformatika, alat pencarian, aplikasi *Internet of Things*,
*machine learning*, dan bahkan bagian utama dari web browser Firefox.

### Pengembang Open Source

Rust untuk orang yang ingin ikut andil dalam membangun bahasa pemrograman Rust,
komunitas, alat pengembang, dan pustaka-Nya. Kami senang dalam kontribusi kamu
di bahasa Rust ini.

### Orang yang menghargai Kecepatan dan Kestabilan

Rust adalah untuk orang yang mencari kecepatan dan kestabilan dalam bahasa.
Dengan kecepatan, berarti kecepatan program yang kamu buat dengan Rust dan
kecepatannya dimana Rust membantu menulisnya. Kompiler Rust memeriksa kestabilan
melalui penambahan fitur dan refaktorisasi. Ini berbeda dengan bahasa tanpa fitur
pengujian yang menghasilkan kode legasi yang rapuh, dimana pengembang biasanya
takut untuk memodifikasi. Dengan berusaha tercapainya abstraksi tanpa beban, 
fitur level tinggi langsung terkompilasi ke kode level bawah secepat kode yang
ditulis manual, Rust mengusahakan untuk membuat kode yang aman bisa menjadi cepat 
juga

Bahasa Rust berharap untuk dapat melayani pengguna lainnya juga; mereka yang
disebutkan disini hanyalah sebagian dari stakeholder terbesar. Secara keseluruhan,
Rust berambisi besar mengeliminasi *trade-off* dimana programmer selama beberapa
dekade telah memaklumi dengan menyediakan keamanan *dan* produktivitas, atau speed 
*dan* ergonomis. Berikan Rust percobaan dan lihat apakah pilihan ini bagus untukmu.

## Untuk Siapa Buku ini Ditujukan

Buku ini asumsi bahwa kamu telah menulis kode di bahasa pemrograman lainnya namun
tidak menebak yang mana saja. Kami telah mencoba membuat bahasan dapat dipahami
oleh mereka yang berasal dari beragam variasi background pemrograman. Kami tidak
akan membahas lama bagaimana *seharusnya* pemrograman atau bagaimana cara seperti
itu. Jika kamu masih awam dalam pemrograman, kamu akan lebih baik memahami dengan
membaca buku yang dikhususkan menyediakan pengenalan untuk pemrograman.

## Bagaimana menggunakan Buku ini

Secara umum, buku ini berasumsi bahwa kamu membaca dari awal sampai akhir. Bab 
Bab yang jauh dibangun berdasarkan konsep bab yang awal, dan bab awalan mungkin
tidak akan terlalu mendalami detil dari suatu topik; kami biasanya secara khusus
akan mengunjungi topik kembali di bab akhiran.

Kamu akan menemukan dua jenis bab di buku ini: bab konsep dan bab projek. Di bab
konsep, kamu akan mempelajari aspek dari Rust. Di bab projek, kita akan membangun
bahasa pemrograman bersama, mengaplikasikan yang telah kamu pelajari sejauh ini.
Bab 2, 12, dan 20 adalah bab projek; sisanya adalah bab konsep.

Bab 1 menjelaskan bagaimana cara menginstall Rust, bagaimana menulis program
“Hello, world!”, dan cara menggunakan Cargo, manajer paket dan alat pengembang Rust.
Bab 2 akan menjadi pengantar langsung untuk bahasa Rust. Disitu kita akan membahas
konsep di level tinggi, dan bab lanjutannya akan menyediakan detil tambahan. Jika kamu
ingin langsung mempelajarinya, Bab 2 adalah tempat untuk itu. Pertama, kamu mungkin mau
melewati Bab 3 terlebih dahulu, dimana kita membahas fitur Rust yang mirip seperti
bahasa pemrograman lainnya, dan langsung melanjutkan ke Bab 4 dimana akan mempelajari
tentang sistem *Ownership* Rust. Namun, jika kamu pelajar yang teliti yang dimana 
lebih memilih belajar secara terperinci sebelum melewati yang berikutnya, kamu
mungkin mau untuk melewati Bab 2 dan langsung menuju Bab 3, dan kembali ke Bab 2
ketika kamu ingin memulai mengerjakan tugas dari yang telah kamu pahami.

Bab 5 membahas struct dan *method*, dan Bab 6 akan mencangkup enum, pernyataan `match`,
dan `if let` untuk konstruksi fungsi kontrol. Kamu akan menggunakan struct dan enum
untuk membuat tipe yang terkustomisasi Rust.

Di Bab 7, kamu akan mempelajari sistem modul Rust dan tentang aturan privasi untuk
mengorganisasikan kode-Mu dan publikasi-Nya Application Programming Interface
(API). Bab 8 membahas tentang bagian umum dari struktur koleksi data yang standar 
pustaka sediakan, seperti vector, string, dan peta/map hash. Bab 9 mempelajari
filosofi dan teknik penangkapan error di Rust.

Bab 10 menjelajahi generik, trait, dan siklus hidup, dimana akan membuka kesempatan
untuk mendefinisikan kode yang mengaplikasikan beberapa tipe. Bab 11 seluruhnya tentang
pengetesan, dimana bahkan dengan jaminan keamanan Rust tetap diharuskan untuk 
menjaga logika dari program ini benar. Bab 12, kita akan membangun sendiri implementasi
sebagian dari fungsionalitas dari alat lini perintah `grep` yang mencari text
dari keseluruhan file. Untuk ini, kita akan menggunakan banyak konsep dari yang 
telah kita bahas di bab sebelumnya.

Bab 13 menjelajahi tentang closure (penutup fungsi) dan iterasi: fitur dari 
Rust yang datang dari bahasa pemrograman fungsional. Bab 14, kita akan mentelaah
Cargo secara lebih dalam dan berbicara tentang kebiasaan baik untuk membagikan 
pustaka ke orang lain. Bab 15 membahas pointer cerdas yang pustaka standar 
sediakan dan trait yang memungkinkan fungsinya mereka.

Bab 16, kita akan melewati beberapa model berbeda dari pemrograman konkurensi
dan berbicara tentang bagaimana Rust membantu kamu memprogram dengan banyak (multiple)
thread tanpa rasa takut. Bab 17 melihat bagaimana perbandingan idiom Rust
dengan prinsip bahasa pemrograman berorientasi objek yang kamu mungkin akrab dengannya

Bab 18 adalah referensi tentang pola dan pencocokan pola, dimana akan berguna
untuk mengekspresikan ide di sepanjang program Rust. Bab 19 berisi tentang
kumpulan topik lanjutan yang menarik, termasuk unsafe Rust, makro, dan
tentang siklus hidup (lifetime), trait, tipe, function, dan closure.

Bab 20, kita akan menyelesaikan projek dimana kita mengimplementasikan web server
yang/dari level-bawah!

Yang terakhir, beberapa appendix berisi informasi yang berguna tentang bahasa Rust
dalam bentuk format mirip referensi. Lampiran A berisi kata kunci Rust, Lampiran B
berisi operator dan simbol yang dimiliki Rust, Lampiran C berisi trait yang dapat
diturunkan yang disediakan oleh pustaka standar, Lampir C berisi peralatan pengembangan
yang berguna, dan Lampiran E berisi edisi-edisi Rust.

Tiada yang namanya langkah yang salah membaca buku ini: jika kamu ingin melewatkan dulu,
Silahkan! Kamu mungkin akan kembali ke bab sebelumnya jika kamu merasa ada yang
membingungkan. Namun lakukan apa yang cocok bagi-Mu.

<span id="ferris"></span>

Sebuah bagian yang penting dari proses belajar Rust adalah mempelajari bagaimana
membaca kode error yang kompiler tunjukkan: panduan berikut ini akan membimbing
kamu terhadap kode yang bekerja. Demikian, kami akan menyediakan banyak contoh
yang mungkin tidak bisa terkompilasi bersama dengan pesan error yang akan ditunjukan
oleh kompiler di setiap situasinya. Ketahui bahwa jika kamu mencoba contoh kode
yang acak, itu mungkin akan gagal terkompilasi! Jadi pastikan kamu telah membaca
sekeliling teks untuk melihat apakah contoh yang kamu coba jalankan itu memang
tertuju untuk gagal. Ferris akan juga membantu kamu membedakan kode 
yang akan gagal dan yang bukan.

| Ferris                                                                 | Arti                                          |
|------------------------------------------------------------------------|--------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain"/>    | Kode ini tidak akan terkompilasi                      |
| <img src="img/ferris/panics.svg" class="ferris-explain"/>              | Kode ini akan panik!                                |
| <img src="img/ferris/unsafe.svg" class="ferris-explain"/>              | Kode yang terdapat di blok ini terdapat kode tidak aman (unsafe code).            |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain"/>| Kode ini akan membuat hasil yang tidak diinginkan. |

Di kebanyakan situasi, kami akan membimbing versi yang benar dari kode
yang tidak terkompilasi

## Sumber Kode

Sumber file dari seluruh buku ini yang tercipta dapat ditemukan di
[Github][book]

[book]: https://github.com/rust-lang/book/tree/master/src
