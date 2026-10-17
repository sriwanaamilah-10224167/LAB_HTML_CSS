# Jawaban Praktikum: SRIWANAAMILAH (10224167)

## Bagian 1: Pemanasan

1. Selector: nav a.active:hover
   Deklarasi: color: red;
   Property: color
   Value: red
   Pseudo-class: :hover

2. Block: p, li, h2.
   Inline: span, a, strong.

3. Paragraf A dan B menjadi hijau karena keduanya merupakan elemen p yang berada di dalam elemen dengan class box.

4. Warnanya merah karena selector #title memiliki specificity paling tinggi dibandingkan selector .heading dan h1.

5. Tag HTML tidak ditutup dengan urutan yang benar. Tag <strong> harus ditutup sebelum tag </p>, sehingga menjadi <p>Hello <strong>world</strong></p>.

## Bagian 3: Prediksi Selector Golf

P1. Prediksi:
(a) Weekly hack nights: biru.
(b) Bring your own laptop: oranye.
(c) © 2026 Student Affairs: biru.

P2. Urutan specificity tertinggi ke terendah:
1. #tech p
2. .club p
3. main section p
4. p

Setelah diuji (hasil sebenarnya):
(a) Weekly hack nights: hijau.
(b) Bring your own laptop: oranye.
(c) © 2026 Student Affairs: biru.

## Bagian 4: Box Model

Q1 (content-box):
Lebar yang terlihat = width + padding kiri dan kanan + border kiri dan kanan.
= 300px + 16px + 16px + 1px + 1px
= 334px.

Q2 (border-box):
Dengan box-sizing: border-box, lebar 300px sudah mencakup content, padding, dan border. Jadi, lebar dari tepi border ke tepi border adalah 300px. Ukuran content menyesuaikan agar padding dan border tetap masuk dalam lebar tersebut.

Pengecekan DevTools:
Saya memeriksa bagian Computed pada DevTools untuk melihat ukuran content, padding, border, dan margin pada salah satu section.

## Bagian 5: Tabel Debug

| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|-------|-----|-----------|-------------------|
| 1 | CSS body | colour bukan property CSS yang benar | Ganti menjadi color | Membaca kode dan DevTools |
| 2 | CSS header | Kurang titik koma setelah background: #dbe7f3 | Tambahkan ; | Membaca kode |
| 3 | CSS .Card | Nama class tidak sesuai dengan HTML yang menggunakan card | Ganti .Card menjadi .card | Membandingkan HTML dan CSS |
| 4 | CSS #news-list | 18 px memiliki spasi yang salah | Ganti menjadi 18px | Membaca kode dan DevTools |
| 5 | CSS footer | Nilai centre tidak valid | Ganti menjadi center | Membaca kode dan DevTools |
| 6 | Heading | Tag <h1> ditutup dengan </h2> | Ganti menjadi </h1> | W3C Validator |
| 7 | Link About | Tanda kutip pada atribut href tidak lengkap | Perbaiki menjadi href="about.html" | W3C Validator |
| 8 | Gambar | Elemen <img> tidak memiliki atribut alt | Tambahkan alt="Berita kampus" | W3C Validator |
| 9 | Daftar berita | ID HTML newsList tidak sesuai dengan selector CSS #news-list | Samakan nama ID dan selector, misalnya news-list | Membandingkan HTML dan CSS |

## Bagian 6: Tabel Code Review

| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|-------|---------|-----------------|----------------|
| 1 | 1 | Tidak ada deklarasi <!DOCTYPE html> | Browser dapat menggunakan mode rendering yang tidak diharapkan | Tambahkan <!DOCTYPE html> |
| 2 | 1–3 | Elemen <html> tidak memiliki atribut lang | Membantu pembaca layar dan mesin pencari mengenali bahasa halaman | Tambahkan lang="id" |
| 3 | 2–4 | Tidak ada metadata charset dan viewport | Karakter dan tampilan pada perangkat seluler dapat bermasalah | Tambahkan meta charset dan viewport |
| 4 | 12–14 | Menggunakan banyak <div> untuk struktur halaman | Struktur menjadi kurang semantik dan sulit dipahami | Gunakan header, nav, main, section, dan footer |
| 5 | 13 | Nama kampus menggunakan <b> dan bukan heading utama | Struktur heading tidak jelas bagi pembaca layar | Gunakan <h1> |
| 6 | 20 dan 24 | Judul bagian dibuat menggunakan <div> | Judul tidak dikenali sebagai heading | Gunakan <h2> |
| 7 | 18–28 | Menggunakan <br> berulang untuk mengatur jarak | Jarak halaman seharusnya diatur dengan CSS | Gunakan margin dan padding |
| 8 | 5 | Menggunakan !important pada aturan link | Membuat cascade CSS lebih sulit dikelola | Hapus !important dan atur specificity dengan benar |
| 9 | 4 | Lebar header tetap 1200px | Halaman dapat melampaui layar perangkat kecil | Gunakan max-width: 960px dan margin otomatis |
| 10 | 6 | Warna teks konten #bbbbbb kurang kontras dengan latar putih | Membuat teks sulit dibaca | Gunakan warna teks yang lebih gelap |
| 11 | 7 | Sidebar menggunakan float, tetapi tidak ada elemen sidebar pada HTML | Aturan CSS tidak digunakan | Hapus aturan yang tidak diperlukan atau buat sidebar sesuai kebutuhan |
| 12 | 27 | Input email menggunakan type="text" | Validasi email bawaan browser tidak tersedia | Gunakan type="email" |
| 13 | 26–27 | Input tidak memiliki label yang terhubung | Pengguna pembaca layar sulit mengetahui tujuan input | Tambahkan <label for="..."> |
| 14 | 21 | Gambar tidak memiliki atribut alt | Informasi gambar tidak tersedia bagi pembaca layar | Tambahkan deskripsi alt |
| 15 | 28 | Tombol menggunakan JavaScript inline yang hanya menampilkan alert | Tombol belum benar-benar mengirim formulir | Gunakan <form> dan tombol submit |
| 16 | 31 | Footer tidak menggunakan elemen semantik <footer> | Struktur bagian bawah halaman kurang jelas | Gunakan <footer> |

### Refleksi

1. Masalah yang paling sulit disadari adalah tidak adanya label pada input dan atribut alt pada gambar. Halaman masih terlihat baik di browser, tetapi masalah tersebut berpengaruh pada aksesibilitas.

2. Masalah-masalah tersebut tetap penting karena kode yang baik tidak hanya harus terlihat benar, tetapi juga mudah diakses, dipahami, dipelihara, dan digunakan pada berbagai perangkat.

3. Saya akan memeriksa struktur HTML, konsistensi selector CSS, aksesibilitas, dan hasil W3C Validator sebelum mengumpulkan tugas.

## Bagian 7: Exit Ticket

1. Aturan CSS terdiri dari selector dan blok deklarasi. Selector menentukan elemen yang dipilih, sedangkan deklarasi berisi property dan value untuk mengatur tampilannya.

2. Saya masih perlu berlatih memahami specificity ketika beberapa selector mengatur elemen yang sama.

3. Saya sekarang bisa membuat struktur HTML semantik, menghubungkan file CSS, dan menggunakan selector dasar untuk mengatur tampilan halaman.