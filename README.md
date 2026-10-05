# Lab3Web

## Praktikum 3: CSS Dasar

### Tujuan

Praktikum ini bertujuan untuk:

1. Memahami konsep dasar CSS.
2. Memahami aturan penulisan pada CSS.
3. Memahami selector sebagai pengontrol CSS.
4. Membuat pengaturan CSS pada HTML.

CSS digunakan untuk mengatur tampilan dan komponen pada halaman web agar lebih terstruktur dan seragam. Pada praktikum ini dipelajari CSS Internal, Inline CSS, CSS Eksternal, serta penggunaan ID Selector dan Class Selector.

---

## 1. Membuat Dokumen HTML

Pada langkah pertama dibuat dokumen HTML dengan nama:

`lab2_css_dasar.html`

Dokumen HTML berisi struktur dasar HTML seperti `<!DOCTYPE html>`, `<html>`, `<head>`, dan `<body>`.

Pada bagian body dibuat:

* Header dengan judul "CSS Internal dan Inline CSS".
* Navigasi menggunakan tag `<nav>`.
* Bagian `intro` menggunakan ID Selector.
* Paragraf yang berisi penjelasan pembelajaran HTML dan CSS.
* Tombol "Informasi selengkapnya" menggunakan Class Selector.

Kode utama yang digunakan:

```html
<header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>

<nav>
    <a href="lab2_css_dasar.html">CSS Dasar</a>
    <a href="lab2_css_eksternal.html">CSS Eksternal</a>
    <a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>

<div id="intro">
    <h1>Hello World</h1>

    <p>
        Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
        <b>Pemrograman Web</b> di
        <i>Universitas Pelita Bangsa</i>.
    </p>

    <a class="button btn-primary" href="#intro">
        Informasi selengkapnya.
    </a>
</div>
```

### Screenshot

Tambahkan screenshot hasil langkah ini di bawah:

```markdown
![Dokumen HTML](screenshot/01-html.png)
```

---

## 2. Mendeklarasikan CSS Internal

Pada langkah kedua ditambahkan CSS Internal menggunakan tag `<style>` yang diletakkan di dalam bagian `<head>`.

CSS Internal digunakan untuk mengatur tampilan halaman HTML tanpa membuat file CSS terpisah.

Kode CSS Internal yang digunakan:

```css
body {
    font-family: 'Open Sans', sans-serif;
}

header {
    min-height: 80px;
    border-bottom: 1px solid #77CCEF;
}

h1 {
    font-size: 24px;
    color: #0F189F;
    text-align: center;
    padding: 20px 10px;
}

h1 i {
    color: #6d6a6b;
}
```

CSS tersebut digunakan untuk mengatur jenis font, tinggi header, garis bawah header, ukuran heading, warna heading, posisi teks, padding, dan warna teks italic.

### Screenshot

```markdown
![CSS Internal](screenshot/02-internal.png)
```

---

## 3. Menambahkan Inline CSS

Pada langkah ketiga ditambahkan Inline CSS pada elemen paragraf.

Inline CSS ditulis langsung pada tag HTML menggunakan atribut `style`.

Kode yang digunakan:

```html
<p style="text-align: center; color: #ccd8e4;">
    Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
    <b>Pemrograman Web</b> di
    <i>Universitas Pelita Bangsa</i>.
    Pelajaran pertama yang kami dapat adalah membuat tampilan web
    sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.
</p>
```

CSS tersebut digunakan untuk membuat teks paragraf menjadi rata tengah dan memberikan warna pada teks.

### Screenshot

```markdown
![Inline CSS](screenshot/03-inline.png)
```

---

## 4. Membuat CSS Eksternal

Pada langkah keempat dibuat file CSS baru dengan nama:

`style_eksternal.css`

CSS eksternal digunakan untuk memisahkan aturan CSS dari dokumen HTML.

Kode CSS yang digunakan:

```css
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav .active,
nav a:hover {
    background: #0B6B3A;
}
```

File CSS tersebut kemudian dihubungkan dengan file HTML menggunakan tag `<link>`:

```html
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```

### Screenshot

```markdown
![CSS Eksternal](screenshot/04-eksternal.png)
```

---

## 5. Menambahkan CSS Selector

Pada langkah kelima ditambahkan CSS Selector menggunakan ID Selector dan Class Selector.

### ID Selector

ID Selector menggunakan tanda `#`.

Kode yang digunakan:

```css
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
```

Selector tersebut digunakan pada elemen:

```html
<div id="intro">
```

ID Selector digunakan untuk memberikan style pada elemen yang memiliki ID tertentu.

---

### Class Selector

Class Selector menggunakan tanda titik `.`.

Kode yang digunakan:

```css
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}

.btn-primary {
    background: #E42A42;
}
```

Selector tersebut digunakan pada elemen:

```html
<a class="button btn-primary" href="#intro">
    Informasi selengkapnya.
</a>
```

Satu elemen dapat memiliki lebih dari satu class, yaitu `button` dan `btn-primary`.

### Screenshot

```markdown
![CSS ID dan Class Selector](screenshot/05-selector.png)
```

---

## 6. Struktur File

Struktur file praktikum yang digunakan:

```text
Lab3Web/
│
├── lab2_css_dasar.html
├── style_eksternal.css
├── README.md
│
└── screenshot/
    ├── 01-html.png
    ├── 02-internal.png
    ├── 03-inline.png
    ├── 04-eksternal.png
    └── 05-selector.png
```

---

## 7. Kesimpulan

Pada Praktikum 3 dipelajari konsep dasar CSS dan cara penerapannya pada HTML.

CSS dapat ditulis dengan tiga cara, yaitu:

1. **Internal CSS**, yaitu CSS yang ditulis menggunakan tag `<style>` di dalam bagian `<head>`.
2. **Inline CSS**, yaitu CSS yang ditulis langsung pada atribut `style` sebuah elemen HTML.
3. **External CSS**, yaitu CSS yang ditulis pada file `.css` terpisah dan dihubungkan ke HTML menggunakan tag `<link>`.

Selain itu, dipelajari juga penggunaan **Element Selector, ID Selector, dan Class Selector** untuk mengatur tampilan elemen HTML.

---

## 8. Validasi CSS

Dokumen CSS divalidasi menggunakan CSS Validator dari W3C.

Website validasi:

https://jigsaw.w3.org/css-validator/

Screenshot hasil validasi:

```markdown
![Validasi CSS](screenshot/06-validasi.png)
```

---

## 9. Repository

Nama repository:

`Lab3Web`

Setelah semua praktikum selesai, file di-commit dan di-push ke repository GitHub.

Repository:

```text
[Tulis URL repository GitHub di sini]
```
