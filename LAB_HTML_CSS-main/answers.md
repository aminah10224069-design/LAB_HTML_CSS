# Jawaban Praktikum: Siti aminah (10224069)

## Bagian 1: Pemanasan
1. Selector: `nav a.active`, Pseudo-class: `:hover`, Property: `color`, Value: `red`, Deklarasi: `color: red;`
2. Block: `p`, `li`, `h2`. Inline: `span`, `a`, `strong`.
3. Paragraf A dan B (karena berada di dalam elemen `.box`).
4. Berwarna **merah** (`red`), karena ID selector (`#title`) memiliki nilai *specificity* paling tinggi.
5. Tag `<p>` dan `<strong>` tumpang tindih. Penulisan yang benar: `<p>Hello <strong>world</strong></p>`.

## Bagian 3: Prediksi Selector Golf
P1. (a) green, (b) orange, (c) blue.
P2. `#tech p` > `.club p` > `main section p` > `p`
Setelah diuji (hasil sebenarnya): Hasil pengujian sesuai dengan prediksi awal, nilai specificity ID selector paling dominan.

## Bagian 4: Box model
Q1 (content-box): Lebar = 300px + (16px * 2 padding) + (1px * 2 border) = **334px**.
Q2 (border-box): Lebar tetap **300px**, karena padding dan border dihitung di dalam lebar total kartu.
Pengecekan DevTools: Content: 300px, Padding: 16px, Border: 1px, Margin: 24px.

## Bagian 5: Tabel debug
| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|-------|-----|-----------|-------------------|
| 1 | 9 | Atribut `colour` salah ketik | `color: #2c3e50;` | DevTools menunjukkan property tidak valid |
| 2 | 14 | Tag penutup `</p>` kurang | Menambahkan `</p>` | Membaca kode & W3C Validator |
| 3 | 18 | `background-colour` salah | `background-color: #f0f0f0;` | DevTools mencoret property |
| 4 | 22 | Class selector kurang tanda titik | `.card` | Membaca kode CSS |
| 5 | 26 | Penulisan `font-size` salah | `font-size: 14px;` | Property tidak berefek di browser |
| 6 | 30 | Atribut `href` salah ketik `herf` | `href="#"` | Link tidak bisa diklik |
| 7 | 35 | ID selector pakai titik bukan `#` | `#footer` | Membaca kode |
| 8 | 40 | Tag `<img>` tanpa atribut `alt` | Menambahkan `alt="Deskripsi"` | W3C Validator |
| 9 | 45 | Tag `<div>` digunakan | Diganti ke tag semantik `<section>` | W3C Validator |

## Bagian 6: Tabel Code Review
| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|-------|---------|-----------------|----------------|
| 1 | 10 | Penggunaan `<div>` berlebihan | Tidak semantik untuk SEO dan accessibility | Diganti `<header>`, `<main>`, `<section>` |
| 2 | 15 | Penggunaan inline `style=""` | Memperburuk pemeliharaan kode | Dipindahkan ke file `style.css` |
| 3 | 20 | Lompatan heading dari `h1` ke `h4` | Merusak struktur hierarki dokumen | Diubah berurutan menjadi `h2` |
| 4 | 25 | Tag `<img>` tanpa `alt` | Mengganggu pembaca layar (*screen reader*) | Ditambahkan `alt` deskriptif |
| 5 | 30 | Tidak ada tag `<meta name="viewport">` | Tampilan tidak responsif di HP | Ditambahkan tag viewport di `<head>` |
| 6 | 35 | Syntax CSS tidak diakhiri `;` | Dapat merusak pembacaan rule berikutnya | Ditambahkan `;` di akhir baris |
| 7 | 40 | Penggunaan ID berulang | ID harus unik dalam satu dokumen | Diganti menjadi `class` |
| 8 | 45 | Tidak ada struktur `<table>` yang benar | Aksesibilitas data tabel kurang baik | Ditambahkan `<thead>` dan `<tbody>` |

## Bagian 7: Exit Ticket

1. **Jelaskan anatomi sebuah aturan CSS dengan kata-katamu sendiri:**
   Aturan CSS terdiri dari **Selector** (elemen HTML yang ingin dihias, contoh: `p` atau `.card`), diikuti **kurung kurawal `{}`**. Di dalam kurung kurawal terdapat **Property** (apa yang ingin diubah, contoh: `color`), titik dua `:`, **Value** (nilainya, contoh: `green`), dan diakhiri dengan **titik koma `;`**.

2. **Selector atau konsep apa dari hari ini yang masih membingungkan bagimu?**
   Penggunaan selector turunan yang kompleks seperti kombinasi `pseudo-class` atau spesifisitas (specificity) saat menentukan urutan prioritas warna/desain.

3. **Satu hal apa yang sekarang bisa kamu lakukan tanpa perlu mencarinya?**
   Menghubungkan file HTML ke file CSS menggunakan tag `<link rel="stylesheet" href="style.css">` serta membuat tampilan layout dasar berbentuk kartu (*card layout*).