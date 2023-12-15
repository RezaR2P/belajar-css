**Flexbox Overview:**

Flexbox adalah modul CSS yang menyediakan cara efektif untuk menyusun, mengsejajarkan, dan mendistribusikan jarak antar item di dalam sebuah container, terlepas dari ukuran dinamis atau tidak diketahui.

**Terminologi Flexbox:**

- **Main Axis dan Cross Axis:**
  - **Main Axis:** Sumbu utama dari container yang menentukan urutan penempatan item secara horizontal atau vertikal.
  - **Cross Axis:** Sumbu yang tegak lurus terhadap main axis.

- **Main-Start dan Main-End:**
  - **Main-Start:** Posisi awal items yang disimpan dalam container pada main axis.
  - **Main-End:** Posisi akhir items yang disimpan dalam container pada main axis.

- **Main Size:**
  - Ukuran (width/height) dari container yang menentukan dimensi relatif dari items terhadap main size.

**Container (Parent) Properties:**

```css
.container {
  display: flex; 
  flex-direction: row | row-reverse | column | column-reverse;
  flex-wrap: nowrap | wrap | wrap-reverse;
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
  align-items: stretch | flex-start | flex-end | center | baseline;
  align-content: stretch | flex-start | flex-end | center | space-between | space-around;
}
```

**Item (Child) Properties:**

```css
.item {
  order: <integer>;
  flex-grow: <number>;
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

**Penjelasan Singkat:**

- `display: flex;` membuat elemen parent menjadi flex container, dan elemen di dalamnya dapat berprilaku flex.
- `flex-direction` menentukan arah utama dari kontainer flex.
- `flex-wrap` menentukan apakah elemen-elemen dapat melipat ke baris/kolom berikutnya.
- `justify-content` mengatur posisi horizontal elemen-elemen dalam kontainer.
- `align-items` mengatur posisi vertikal elemen-elemen dalam kontainer.
- `align-content` mengatur distribusi elemen-elemen di sepanjang sumbu lintang jika ada lebih dari satu baris elemen.
- `order` mengatur urutan tampilan elemen dalam kontainer.
- `flex-grow` menentukan sejauh mana elemen dapat tumbuh relatif terhadap elemen-elemen lain.
- `align-self` mengatur penempatan elemen individual dalam kontainer flex pada sumbu lintang.

Contoh Penggunaan:

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.item {
  order: 2;
  flex-grow: 1;
  align-self: flex-end;
}
```

Dengan membaca dokumentasi ini, Anda dapat dengan lebih mudah memahami dan menggunakan fitur-fitur Flexbox untuk merancang tata letak yang responsif dan dinamis.