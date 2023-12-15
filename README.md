# Panduan Belajar CSS

Selamat datang di panduan belajar CSS! Dokumen ini memberikan langkah-langkah dasar untuk memahami CSS.

## Daftar Isi

1. [Pengenalan CSS](#1-pengenalan-CSS)
2. [Menambah CSS ke HTML](#2-menambah-css-ke-html)
3. [Komentar CSS](#3-komentar-css)
4. [Selector](#4-selector)
5. [Color](#5-color)
6. [Text](#6-text)
7. [Font](#7-font)
8. [Font](#7-font)
9. [Background](#7-background)
10. [Box Model](#7-box-model)
11. [Min dan Max Size](#7-min-dan-max-size)
12. [Border](#7-border)
13. [Referensi dan Sumber Belajar](#8-referensi-dan-sumber-belajar)
14. [Berkontribusi](#9-berkontribusi)

## 1. Pengenalan CSS

Apa itu CSS?

- CSS adalah singkatan dari Cascading Style Sheet
- CSS menjelaskan bagaimana elemen HTML ditampilkan di layar, kertas, atau di media lain
- CSS menghemat banyak pekerjaan. Itu dapat mengontrol tata letak beberapa halaman web sekaligus
- Stylesheet eksternal disimpan dalam file CSS

**Definisi Singkat:** CSS adalah bahasa untuk mengatur tampilan halaman web. Ini memisahkan desain (warna, font, layout) dari konten HTML, memastikan tampilan yang konsisten di seluruh situs web.

## 2. Menambah CSS ke HTML

- **Inline:** Inline CSS memungkinkan penerapan gaya langsung pada elemen HTML menggunakan atribut style. Ini berguna untuk menetapkan gaya khusus pada satu elemen.

```html
<h1 style="color: lightblue;">Hello, World!</h1>
```

- **Internal:** Dalam HTML, gaya internal dapat dimasukkan di dalam tag <style> yang terletak di bagian <head> dokumen. Ini memungkinkan penulisan gaya langsung di dalam file HTML.

```html
<head>
  <style>
    body {
      background-color: lightblue;
    }
  </style>
</head>
```

- **Eksternal:** Dengan menggunakan file CSS terpisah, gaya dapat diorganisir dan dipisahkan dari HTML. File CSS ini kemudian dihubungkan ke dokumen HTML menggunakan tag <link> di bagian <head>.

```html
<head>
  <link rel="stylesheet" type="text/css" href="style.css" />
</head>
```

## 3. Komentar CSS

- **Komentar:** digunakan untuk memberikan keterangan pada kode. Mereka tidak mempengaruhi tampilan halaman web dan hanya berguna sebagai panduan bagi pengembang.

```css
/* ini adalah komentar yang tidak akan di execute oleh program */
```

## 4. Selector

- **Element:** Memilih elemen HTML berdasarkan tipe elemennya.
  Contoh: `p` untuk memilih semua elemen paragraf.
- **ID:** Memilih elemen berdasarkan atribut ID uniknya.
  Contoh: `#header` untuk memilih elemen dengan ID "header".
- **Class:** Memilih elemen berdasarkan atribut class.
  Contoh: `.button` untuk memilih semua elemen dengan class "button".
- **Gabungan:** Menggabungkan beberapa selector untuk memilih elemen yang memenuhi kriteria tertentu.
  Contoh: `nav ul` untuk memilih semua elemen `<ul>` yang berada di dalam elemen `<nav>`.
- **Anak (Child):** Memilih elemen yang merupakan anak langsung dari elemen lain.
  Contoh: `ul > li` untuk memilih semua elemen `<li>` yang langsung berada di dalam elemen `<ul>`.
- **Pseudo-class:** Memilih elemen berdasarkan keadaan atau status tertentu.
  Contoh: `:hover` untuk memilih elemen ketika kursor berada di atasnya.
- **Pseudo-element:** Memilih bagian-bagian spesifik dari suatu elemen.
  Contoh: `::first-line` untuk memilih baris pertama dari suatu elemen teks.

Contoh penggunaan beberapa selector:

```css
/* Selector Elemen */
p {
  color: blue;
}

/* Selector ID */
#header {
  font-size: 20px;
}

/* Selector Class */
.button {
  background-color: green;
}

/* Selector Gabungan */
nav ul {
  list-style-type: none;
}

/* Selector Anak */
ul > li {
  font-weight: bold;
}

/* Selector Pseudo-class */
a:hover {
  text-decoration: underline;
}

/* Selector Pseudo-element */
p::first-line {
  font-style: italic;
}
```

## 5. Color

color digunakan untuk mengatur warna teks pada elemen HTML. Nilai dapat berupa nama warna, kode hex, nilai RGB, atau nilai RGBA (dengan transparansi).
Contoh:

```css
p {
  color: red; /* Nama warna */
}

h1 {
  color: #3498db; /* Kode warna hex */
}

a {
  color: rgb(255, 0, 0); /* Nilai RGB (merah) */
}

.transparent-bg {
  color: rgba(0, 0, 255, 0.5); /* Biru dengan transparansi 0.5 */
}
```

## 6. Text

Dalam contoh ini, properti CSS text digunakan untuk mengontrol warna, ukuran, penataan, kapitalisasi, dan jarak huruf pada teks. Sementara properti text-decoration digunakan untuk mengatur dekorasi teks seperti garis bawah, menghilangkan dekorasi, dan menentukan jenis garis melintang pada teks.

```css
/* Mengatur warna dan ukuran teks */
p {
  color: #333;
  font-size: 16px;
}

/* Menentukan penataan teks tengah */
h1 {
  text-align: center;
}

/* Mengubah kapitalisasi teks */
h2 {
  text-transform: uppercase;
}

/* Menentukan jarak antar huruf */
span {
  letter-spacing: 2px;
}
/* Mengatur dekorasi teks menjadi garis bawah */
a {
  text-decoration: underline;
}

/* Menghilangkan dekorasi teks */
a.no-decoration {
  text-decoration: none;
}

/* Menentukan jenis garis melintang pada teks */
p.crossed {
  text-decoration: line-through;
}
```

## 7. Font

Dalam contoh ini, properti CSS seperti font-family, font-size, font-weight, dan font-style digunakan untuk mengatur berbagai aspek font pada elemen HTML. Font-family menentukan jenis font yang akan digunakan, font-size menentukan ukuran font, font-weight menentukan ketebalan, dan font-style menentukan apakah teks harus dimiringkan atau tidak. Properti-properti ini memungkinkan pengaturan yang fleksibel dan sesuai dengan desain yang diinginkan.

```css
/* Menentukan jenis font dan ukuran untuk seluruh body */
body {
  font-family: "Arial", sans-serif;
  font-size: 16px;
}

/* Menentukan gaya font untuk heading level 1 */
h1 {
  font-family: "Georgia", serif;
  font-weight: bold;
  font-size: 24px;
}

/* Menentukan ukuran dan gaya huruf tebal untuk elemen dengan class 'highlight' */
.highlight {
  font-size: 18px;
  font-weight: bold;
}

/* Menggunakan font dengan gaya miring pada elemen dengan class 'italic-text' */
.italic-text {
  font-style: italic;
}

/* Menentukan gaya font berdasarkan tingkat kepentingan */
h1 {
  font-weight: bold;
}

h2 {
  font-weight: normal;
}

/* Mengatur warna dan bayangan teks */
h3 {
  color: #007bff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
```

## 8. Background

- **Background-color:** Menentukan warna latar belakang.
- **Background-image:** Menambahkan gambar latar belakang.
- **Background-size:** Mengatur ukuran gambar latar belakang (contoh: `cover` untuk menutupi seluruh elemen).
- **Background-position:** Menentukan posisi gambar latar belakang.
- **Background-repeat:** Menentukan apakah gambar latar belakang diulang atau tidak.

```css
/* Menentukan warna latar belakang */
body {
  background-color: #f0f0f0;
}

/* Menambahkan gambar latar belakang */
.header {
  background-image: url("header-background.jpg");
  background-size: cover;
  background-position: center;
}

/* Menggabungkan warna dan gambar latar belakang */
.call-to-action {
  background-color: #007bff;
  background-image: url("cta-icon.png");
  background-repeat: no-repeat;
  background-position: right center;
  color: #fff;
  padding: 20px;
}

/* Menerapkan efek transparansi pada latar belakang */
.transparent-box {
  background-color: rgba(255, 255, 255, 0.7);
  padding: 10px;
}
```

## 9. Box Model

**Box Model** pada CSS adalah cara elemen HTML direpresentasikan sebagai kotak, terdiri dari beberapa bagian: content, padding, border, dan margin.

- **Content:** Bagian isi elemen (teks, gambar, dll.).
- **Padding:** Ruang tambahan di sekeliling konten, memberikan jarak antara konten dan batas elemen.
- **Border:** Garis batas di sekitar padding, memberikan kerangka elemen.
- **Margin:** Ruang tambahan di luar border, memberikan jarak antara elemen ini dan elemen lain di sekitarnya.

```css
/* Mendefinisikan box model untuk elemen dengan class 'box' */
.box {
  width: 200px; /* Lebar konten */
  height: 100px; /* Tinggi konten */
  padding: 10px; /* Ruang padding */
  border: 2px solid #333; /* Garis border */
  margin: 20px; /* Ruang margin */
}
```

## 10. Min dan Max Size

- **min-width:** Menetapkan lebar minimum untuk suatu elemen.
- **max-width:** Menetapkan lebar maksimum untuk suatu elemen.
- **min-height:** Menetapkan tinggi minimum untuk suatu elemen.
- **max-height:** Menetapkan tinggi maksimum untuk suatu elemen.

```css
/* Menetapkan lebar minimum dan tinggi minimum untuk elemen 'box' */
.box {
  min-width: 200px; /* Lebar minimum 200px */
  min-height: 150px; /* Tinggi minimum 150px */
}

/* Menetapkan lebar maksimum untuk elemen 'image-container' */
.image-container {
  max-width: 100%; /* Lebar maksimum sesuai dengan lebar parent */
}

/* Menetapkan tinggi maksimum untuk elemen 'scrollable-section' */
.scrollable-section {
  max-height: 400px; /* Tinggi maksimum 400px */
}

/* Menggabungkan lebar minimum dan maksimum untuk elemen 'responsive-box' */
.responsive-box {
  min-width: 100px; /* Lebar minimum 100px */
  max-width: 300px; /* Lebar maksimum 300px */
}

/* Menggunakan dimensi relatif untuk elemen 'percentage-dimensions' */
.percentage-dimensions {
  width: 50%; /* Lebar 50% dari lebar parent */
  height: 75vh; /* Tinggi 75% dari tinggi viewport */
}
```

## 11. Border

**Border** digunakan untuk menentukan garis batas suatu elemen. Garis batas ini bisa berupa garis solid, putus-putus, bergelombang, atau tidak ada garis batas sama sekali.

- **Komponen Border:**  
  -- 2px: Ketebalan garis (dapat diubah sesuai kebutuhan).
  -- solid: Jenis garis (solid, dashed, dotted, dsb.).
  -- red: Warna garis (nama warna, kode hex, dll.).
- **Komponen Optional:**  
  -- border-radius: Menambahkan sudut melengkung pada border.
  -- border-style: Menentukan jenis garis secara terpisah.
  -- border-color: Menentukan warna border secara terpisah.

```css
/* Border dengan sudut melengkung (border-radius) */
.rounded-box {
  border: 2px solid #3498db;
  border-radius: 10px; /* Sudut melengkung 10px */
}

/* Jenis border yang berbeda pada setiap sisi (border-style) */
.different-borders {
  border-top: 3px dashed #e74c3c; /* Garis putus-putus merah di bagian atas */
  border-right: 2px dotted #27ae60; /* Garis titik-hubung hijau di bagian kanan */
  border-bottom: 4px double #f39c12; /* Garis ganda oranye di bagian bawah */
  border-left: 1px solid #3498db; /* Garis solid biru di bagian kiri */
}

/* Warna border yang berbeda untuk setiap sisi (border-color) */
.colored-borders {
  border-width: 2px;
  border-top-color: #e74c3c; /* Warna merah di bagian atas */
  border-right-color: #27ae60; /* Warna hijau di bagian kanan */
  border-bottom-color: #f39c12; /* Warna oranye di bagian bawah */
  border-left-color: #3498db; /* Warna biru di bagian kiri */
}
```

## 12. Referensi dan Sumber Belajar

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools](https://www.w3schools.com/css/default.asp)
- [ProgrammerZamanNow](https://www.youtube.com/watch?v=8FhmFuGLhaQ)

## 13. Berkontribusi

Jika Anda menemui masalah atau memiliki saran, silakan berkontribusi pada rencana ini dengan melakukan fork repositori dan mengirim pull request.

Selamat belajar! 🚀
