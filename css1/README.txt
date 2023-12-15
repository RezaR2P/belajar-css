BELAJAR CSS
 Ada inline ada internal dan ada eksternal, sangat di rekomendasikan menggunakn eksternal css
#INLINE
Menerapkan CSS langsung pada kodingan nya misalkan
<h1 style="color: aqua;">HALO KAMU</h1>

#INTERNAL
Menerapkan di file yg sama akan adanya di head dengan memanggil selector nya contohnya
<style>
        body{
            background-color: red;
        }
        h1{
            color: greenyellow;
        }
        p{
            font-family: Arial, Helvetica, sans-serif;
        }
        b{
            color: blue;
        }
        i{
            color: yellow;
        }
    </style>

#EKSTERNAL
CSS nya di pisah biasanya di simpan di folder, css/style.css 
css ini harus di link kan di bagian head contohnya
    <link rel="stylesheet" href="css/style.css">

#Selector
1.Universal Selector menggunakan * maka semuanya akan berubah contoh
* {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: larger;
}
!!font family dan size semuanya akan berubah maupun h1-h6 p dll pokonya text akan berubah
2.type selector digunukan ketika akan memilih element html contohnya
h1  {
    color: blueviolet;
}

h2 {
    color: darkorchid;
}
3.class selector diawali dengan . lalu diikutin nama kelas 
contoh pada html element <p> kita menggunakan class="makan" maka pada css nya kita menggunakan .makan ini sifatnya universal tapi jika ingin lebih spesifik gunakan element contoh p.makan
4.id selector diawali dengan # lalu diikutin nama id
contoh pada html element <h1> kita menggunakan id="makan" maka pada css nya kita menggunakan #makan
5.child selector digunakan dengan menggunakan tanda >
contoh nya kita mau merubah warna b pada li maka kita menggunakan li>b
6.decendant selector  digunakan dengan menggunakan spasi di antara elemen yang akan menjadi leluhur dan elemen yang akan menjadi keturunan
contoh nya italic di dalam nya ada bold yg di bungkus oleh p maka dalam css nya p b (p spasi b)

#ATURAN CSS CASCADE
1.aturan terakhir yg diambil adalah kodingan misalkan i pertama warna hijau lalu koding kembali warna biru maka jadinya akan biru
2.spesifik akan menampilkan berdasarkan level walaupun sama tapi mengutaman level contoh
b {
    color: saddlebrown; /* Level 1 */
}

p b{
    color: darkgreen; /* Level 2 */
}

b {
    color: aqua !important; /* Level 3 */
} 
!!maka yg akan keluar warna aqua

#INHERITANCE
di css bisa mengambil styles inherit dari orang tua sebelumnya contoh
body {
    padding: 10px;
}

.intro {
    padding: inherit;
}
!!maka intro akan mengikuti padding body

#Color
1.foreground color 
-kita bisa menggunakan color name blue
-kita bisa menggunakan hexcode #32dd4
-kita bisa menggunakan RGB value rgb(129, 68, 243)
-kita bisa menggunakan rgba(83, 55, 134,0.5) a itu adalah alpha dimana bisa memudarkan warna dari 0-1 bisa menggunakan . contoh 0.5
-kita bisa menggunakan hsl(hue, saturation, lightness) hue(0-360) saturation dan lightness (0%-100%)
-kita bisa menggunakan hsla(hue, saturation, lightness, alpha) hue(0-360) saturation dan lightness (0%-100%) alpha(0-1) bisa menggunakan . contoh 0.6

#TEXT
1.font-family
2.font-size px dan % yg sering dipakai
3.font-weight ini bisa mengubah ketebalan tulisan
4.font-style ini bisa mengubah gaya tulisan contoh nya italic
5.text-decoration digunakan untuk menambahkan dekorasi seperti garis bawah atau garis tengah pada teks
6.text-transform digunakan untuk membuat teks menjadi huruf besar semua atau kecil semua
7.text-align digunakan untuk merapihkan teks seperti rata tengah rata kiri maupun rata kanan
8.letter-spacing digunakan untukk mengubah jarak dalam teks
9.line-height digunakan untuk mengatur tinggi baris
10.text-shadow bisa membuuat shadow contoh (kanan,bawah,ketebalan(px))
11.word-spacing digunakan untuk membuat jarak atar kata pakai em
12.letter-spacing digunakan untuk membuat jarak antar huruf pakai em
12. .tautan:hover terus menambahkan warna maka saat mouse di arahkan ke link tersebut warna nya akan berubah
13. .tautan:activate terus menambah warna saat kita click maka warna nya akan berubah
14. .tautan:visited terus menambah warna maka saat kita mengunjungi halaman tersebut terus kembali lagi warna nya akan berubah

#BOX
1. <style>
        /* Definisikan gaya untuk sebuah div dengan class "box" */
        .box {
            width: 200px; /* Lebar kotak */
            height: 100px; /* Tinggi kotak */
            background-color: #3498db; /* Warna latar belakang */
            color: white; /* Warna teks */
            padding: 20px; /* Ruang dalam kotak (padding) */
            border: 2px solid #2980b9; /* Border dengan ketebalan 2px */
            margin: 20px; /* Ruang di sekitar kotak (margin) */
            text-align: center; /* Pusatkan teks secara horizontal */
            line-height: 100px; /* Atur tinggi baris untuk pusatkan teks secara vertikal */
        }
    </style>
    Kami mendefinisikan sebuah gaya CSS dengan selector .box untuk mengubah tampilan elemen <div> yang memiliki class "box."
    Kami mengatur berbagai properti CSS, seperti lebar, tinggi, warna latar belakang, warna teks, padding, border, margin, dan lainnya, untuk membuat tampilan kotak yang kustom.
    Kami menggunakannya pada sebuah elemen <div> dengan class "box."

2.height, width, dan overflow digunakan untuk mengatur dimensi dan perilaku overflow (ketika konten melebihi ukuran yang ditentukan) dari elemen HTML
!!untuk overflow: 	visible (default): Konten yang melebihi batas elemen akan tampil di luar elemen.
    hidden: Konten yang melebihi batas elemen akan terpotong dan tidak terlihat.
    scroll: Jika konten melebihi batas elemen, scrollbars akan muncul, memungkinkan pengguna untuk menggulir ke bawah atau ke samping untuk melihat konten yang tidak terlihat.
    auto: Sama seperti "scroll," tetapi scrollbar hanya akan muncul jika kontennya melebihi batas elemen.
3.minimum dan maximum box bisa menggunakan
-min-width: 400px;
-max-width: 500px;
#BOX MODEL
1.Content yg di tengah isi content tersebut biasanya yg di atur width dan height nya
2.padding lapian kedua
3.border lapisan ketiga
4.margin lapisan keempat
#biasanya ini berhubungan dengan div

#BORDER
1.border-width fungsinya untuk ketebalan border
2.border-style funsinya untuk mengatur gaya
-solid (garis solid)
-dashed (garis putus-putus)
-dotted (garis titik-titik)
-double (garis ganda)
3.border-color bisa menggunakan name,hex dan rgb
4.gabungan border contohnya  border: 2px dashed red;
5.border pada setiap sisi contohnya:
  border-top: 2px solid blue; /* Border atas: 2px solid biru */
  border-right: 1px dashed green; /* Border kanan: 1px dashed hijau */
  border-bottom: 3px dotted orange; /* Border bawah: 3px dotted orange */
  border-left: 4px double purple;
6.border-width juga bisa berbeda tiap sisi contohnya:
-2 sisi contoh border-width: 1px 2px; /* Atas dan Bawah 1px, Kanan dan Kiri 2px */
-3 sisi contoh border-width: 1px 2px 3px; /* Atas 1px, Kanan 2px, Bawah 3px */
-4 sisi border-width: 1px 2px 3px 4px; /* Atas 1px, Kanan 2px, Bawah 3px, Kiri 4px */
!!catatan jika ingin di pisah tambahkan masih masing tataletaknya contoh
  border-top-width: 5px;
  border-top-style: solid;
  border-top-color: crimson; maka border atas saja

#PADDING
1.padding block bisa berbeda tiap sisi contohnya:
-normal padding: 20px; /* maka tiap sisi padding adalah 20px */
-2 sisi padding: 10px 20px; /* Padding atas dan bawah 10px, kanan dan kiri 20px */
-3 sisi padding: 10px 20px 30px; /* Padding atas 10px, kanan 20px, bawah 30px */
-4 sisi padding: 10px 20px 30px 40px; /* Atas 10px, Kanan 20px, Bawah 30px, Kiri 40px */
2.padding inline contohnya   padding-inline-start: 10px; /* Padding kiri dalam arah inline */
  			     padding-inline-end: 15px; /* Padding kanan dalam arah inline */

#MARGIN
1.Margin Block bisa berbeda tiap sisi contohnya: (cmiiw)
-normal margin: 20px; /* maka tiap sisi margin adalah 20px */
-2 sisi margin: 10px 20px; /* Margin atas dan bawah 10px, kanan dan kiri 20px */
-3 sisi margin: 10px 20px 30px; /* Margin atas 10px, kanan 20px, bawah 30px */
-4 sisi margin: 10px 20px 30px 40px; /* Atas 10px, Kanan 20px, Bawah 30px, Kiri 40px */
!!CATATAN MARGIN BISA MENGIKUTI AUTO MAKA AKAN PINDAH KE TENGAH
!!CATATAN KEDUA PADDING DAN MARGIN BOLEH DI PISAH CONTOH margin: 20px; maupun padding sama aja

#DISPLAY
1.inline tidak menghabiskan space
2.block sedangkan block menghabiskan semua space kenan sampai jadi baris baru
3.inline-block Ini memungkinkan elemen HTML untuk tetap berada dalam satu baris yang sama dengan elemen-elemen lain seperti display: inline;, tetapi juga memberi elemen ini kemampuan untuk memiliki lebar dan tinggi yang dapat Anda atur seperti elemen dengan display: block;
4.flex cara untuk mengatur elemen-elemen di dalam halaman web agar mereka bisa bekerja bersama dengan baik, terutama saat tampilan layar berubah-ubah, seperti saat digunakan di perangkat berbeda atau saat ukuran jendela browser diubah
   -display: flex;: Ini adalah properti yang digunakan untuk mengubah suatu elemen HTML menjadi "kontainer flex." Ini berarti elemen ini akan mengatur elemen-elemen anak di dalamnya menggunakan Flexbox.
   -flex-direction: Properti ini mengatur arah elemen-elemen dalam kontainer flex. Anda dapat mengaturnya menjadi "row" (horisontal), "column" (vertikal), "row-reverse," atau "column-reverse."
   -justify-content: Properti ini digunakan untuk mengatur cara elemen-elemen di sepanjang arah utama (misalnya, horizontal) ditempatkan dalam kontainer. Ini bisa membuat mereka berada di tengah, di sisi kiri, di sisi kanan, atau didistribusikan dengan cara tertentu.
   -align-items: Ini mengatur cara elemen-elemen ditempatkan dalam arah silang (misalnya, vertikal) dalam kontainer. Ini bisa membuat mereka sejajar di tengah, di atas, di bawah, atau di tempat lain.
   -flex-grow: Ini mengontrol seberapa besar elemen akan tumbuh dalam kontainer jika ada ruang ekstra.
   -flex-shrink: Ini mengontrol seberapa besar elemen akan menyusut jika tidak cukup ruang.
   -flex-basis: Ini adalah ukuran awal elemen sebelum pertimbangan pertumbuhan atau penyusutan.
   -flex-wrap: Properti ini mengatur apakah elemen-elemen akan melanjutkan ke baris atau kolom berikutnya jika ruang tidak cukup.

#LIST STYLE
1.digunakan untuk mengontrol tampilan dan gaya daftar (list) dalam elemen HTML seperti <ul> (daftar tak terurut) dan <ol> (daftar terurut)
2.list-style-type: Ini mengatur jenis tanda yang digunakan dalam daftar. Beberapa nilai umum termasuk:
   -none: Tidak ada tanda (daftar tanpa bullet atau angka).
   -disc: Tanda berbentuk bulatan (default untuk daftar tak terurut).
   -decimal: Angka Arab (default untuk daftar terurut).
   -square: Tanda berbentuk persegi.
   -circle: Tanda berbentuk lingkaran.
    Dan masih banyak lagi.
3.ist-style-image: Properti ini memungkinkan Anda mengganti tanda (bullet) dengan gambar kustom. Anda dapat mengatur URL gambar yang ingin digunakan sebagai tanda dalam daftar contoh:
   list-style-image:url('namafile");
4.list-style-position: Properti ini mengatur posisi tanda (bullet atau angka) dalam hubungannya dengan teks daftar. Dua nilai umum adalah:
    inside: Tanda berada di dalam kotak teks daftar.
    outside: Tanda berada di luar kotak teks daftar (default)

#TABLE
1.dapat mengubah gaya tabel, warna latar belakang, warna teks, batas, dan banyak aspek lainnya menggunakan CSS. Berikut adalah beberapa properti CSS yang umum digunakan untuk mengatur tampilan tabel:
2.border-collapse: Properti ini mengontrol bagaimana tepi (borders) dari sel-sel tabel bergabung. Nilai yang umum adalah collapse, yang membuat batas sel-sel bersatu, dan separate, yang memisahkan batas sel-sel contoh
table {
  border-collapse: collapse;
}
3.border: Anda dapat mengatur batas (border) untuk tabel atau sel-selnya. Ini mencakup tebal garis, jenis garis (contohnya solid, dashed, atau dotted), dan warna garis
table, th, td {
  border: 1px solid black;
}
4.padding: Anda dapat mengatur ruang antara isi sel dan tepinya menggunakan properti padding
td {
  padding: 10px;
}
5.caption-side: Mengatur posisi caption (judul tabel) jika digunakan
caption {
  caption-side: bottom;
}
6.border-radius: Anda bisa memberikan sudut bulat pada tabel atau sel-selnya
table {
  border-radius: 10px;
}

#FORM
Berikut adalah beberapa properti CSS yang umum digunakan untuk mengatur tampilan formulir:
1.box-shadow: Anda bisa menambahkan bayangan (shadow) untuk elemen formulir untuk memberikan efek kedalaman
input[type="text"] {
  box-shadow: 2px 2px 5px #888888;
}
2.cursor: Properti ini digunakan untuk mengubah ikon kursor saat diarahkan ke elemen formulir
button:hover {
  cursor: pointer;
}
3.activate ketika sudah clik maka warna nya akan berubah dan bahwa ini menandai sudah di click
#submit:acivate{
  color:red;
  background-color:blue;
}
4.font-weight: Digunakan untuk mengubah ketebalan huruf teks.
label {
  font-weight: bold;
}
5.box-decoration-break: Ini memengaruhi tampilan elemen yang dipecah antara halaman atau kolom (biasanya digunakan pada elemen textarea).
textarea {
  box-decoration-break: clone;
}
6.transition: Properti ini digunakan untuk mengatur efek perubahan tampilan ketika elemen formulir berinteraksi
button {
  transition: background-color 0.3s ease;
}
7.outline: Ini mengatur garis luar elemen formulir saat elemen tersebut dipilih.
input:focus {
  outline: 2px solid blue;
}

#IMAGE
Di bawah ini adalah beberapa properti CSS yang umum digunakan untuk mengubah tampilan gambar:
1.width dan height: Properti ini digunakan untuk mengatur lebar dan tinggi gambar
img {
  width: 300px;
  height: 200px;
}
2.margin dan padding: Anda dapat mengatur margin (jarak dari elemen-elemen lain) dan padding (jarak dari tepi gambar ke kontennya)
img {
  margin: 10px;
  padding: 5px;
}
3.box-shadow: Anda dapat menambahkan bayangan (shadow) untuk gambar untuk memberikan efek kedalaman
img {
  box-shadow: 4px 4px 6px #888888;
}
4.object-fit: Properti ini digunakan untuk mengontrol bagaimana gambar diatur dalam elemen yang mengandungnya. Nilai umum termasuk cover dan contain
img {
  object-fit: cover;
}
5.filter: Anda dapat mengubah tampilan gambar dengan mengatur efek seperti grayscale (keabuan), brightness (kecerahan), atau blur (kabur)
img {
  filter: grayscale(50%);
}
6.position: Anda dapat mengatur posisi gambar di dalam kontainernya dengan properti ini
img {
  position: absolute;
  top: 10px;
  left: 20px;
}
7.z-index: Ini mengontrol tumpukan (stacking order) elemen, berguna saat Anda memiliki beberapa elemen yang tumpang tindih.
img {
  z-index: 2;
}
8.border-radius: Properti ini mengubah sudut gambar menjadi bulat atau berbentuk lain
img {
  border-radius: 50%;
}
9.overflow: Anda dapat mengontrol bagaimana gambar ditampilkan jika ukurannya melebihi kontainer
img {
  overflow: hidden;
}
10.object-position: Properti ini mengatur posisi gambar dalam kontainer
img {
  object-position: center bottom;
}
11.background-image: Jika gambar digunakan sebagai latar belakang elemen, Anda dapat mengatur latar belakang dengan properti ini
    div {
      background-image: url('gambar-latar.jpg');
      background-size: cover;
    }
12.transform: Anda dapat memberikan efek transformasi, seperti rotasi atau skala, pada gambar.
img:hover {
  transform: rotate(20deg);
}


#RESPONSIVE
/* Gaya umum untuk layar berukuran kecil atau lebih besar */
body {
  font-size: 16px;
}

/* Media query untuk layar berukuran kecil (misalnya, ponsel) */
@media only screen and (max-width: 600px) {
  body {
    font-size: 14px;
  }
  /* Gaya tambahan untuk layar kecil di sini */
}

/* Media query untuk layar berukuran sedang (misalnya, tablet) */
@media only screen and (min-width: 601px) and (max-width: 1024px) {
  body {
    font-size: 18px;
  }
  /* Gaya tambahan untuk layar sedang di sini */
}

/* Media query untuk layar berukuran besar (misalnya, desktop) */
@media only screen and (min-width: 1025px) {
  body {
    font-size: 20px;
  }
  /* Gaya tambahan untuk layar besar di sini */
}

/* Media query untuk layar potrait (tegak) */
@media only screen and (orientation: portrait) {
  /* Gaya tambahan untuk layar potrait di sini */
}

/* Media query untuk layar landscape (miring) */
@media only screen and (orientation: landscape) {
  /* Gaya tambahan untuk layar landscape di sini */
}
