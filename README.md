Langsung ke **Phase 4: Data Structure**. Kita mulai dari **Part 15**. Di sini kita belajar cara mengelola banyak data dalam satu "wadah".

---

# 📦 Part 15: Array Basic (Koleksi Data)

### 🧩 Analogi: "Lemari Laci"

* **Variabel Biasa**: Ibarat menaruh satu kaus kaki di atas meja. Kalau punya 10 kaus kaki, kamu butuh 10 meja. Berantakan!
* **Array**: Ibarat satu **Lemari Laci**. Kamu bisa menyimpan semua kaus kaki di satu lemari yang sama. Setiap laci punya **Nomor (Index)**. Kalau mau ambil kaus kaki, kamu tinggal sebut nomor lacinya.
* **Penting**: Di dunia coding, nomor laci (index) selalu dimulai dari **0**, bukan 1.

---

### 📚 Teori: Struktur List di JavaScript

Array adalah tipe data yang digunakan untuk menyimpan daftar nilai (list) dalam satu variabel.
1.  **Index**: Posisi elemen dalam array (dimulai dari 0).
2.  **Length**: Jumlah total barang yang ada di dalam array.
3.  **Square Brackets `[]`**: Simbol untuk membungkus isi array.



---

### 🛠️ Praktek: Membuat "Gudang Tools"

Buka `script.js` kamu dan buat daftar tools cybersecurity kamu sendiri:

```javascript
// --- 1. MEMBUAT ARRAY ---
const toolsCyber = ["Nmap", "SQLMap", "Metasploit", "Wireshark"];

// --- 2. MENGAKSES DATA (Memanggil nomor index) ---
console.log(toolsCyber[0]); // Output: Nmap
console.log(toolsCyber[2]); // Output: Metasploit

// --- 3. MENGUBAH DATA ---
toolsCyber[1] = "BurpSuite"; // SQLMap diganti jadi BurpSuite
console.log(toolsCyber);

// --- 4. CEK JUMLAH DATA ---
console.log(`Total tools yang dimiliki: ${toolsCyber.length}`);

// --- 5. DATA CAMPURAN ---
const user = ["Syaifan", 20, true]; // Bisa string, number, & boolean sekaligus
```

---

### 🔍 Kenapa Ini Penting?

Bayangkan kamu membuat marketplace **Koneka**. Tidak mungkin kamu membuat variabel `produk1`, `produk2`, sampai `produk1000`. Dengan Array, kamu cukup buat satu variabel `const daftarProduk = [...]` dan semua data tersimpan rapi di sana.

---

### 💡 Tantangan Part 15

1.  Buat array `mySkills` berisi 3 bahasa pemrograman yang kamu kuasai/pelajari.
2.  Tampilkan bahasa pemrograman kedua (index 1) di console.
3.  Ubah isi bahasa pemrograman ketiga (index 2) menjadi "JavaScript Expert".
4.  Tampilkan panjang array tersebut menggunakan `.length`.

---

**Sudah aman di GitHub? Kabari kalau mau lanjut ke Part 16: Array Methods (Cara nambah/hapus isi laci secara otomatis).** 🚀

---

Langsung ke **Part 16**. Kalau di Part 15 kita baru bikin "Lemari Laci", sekarang kita belajar cara jadi **Manajer Gudang** yang bisa nambah dan hapus isi laci secara otomatis.

---

# 🔧 Part 16: Array Methods (Push, Pop, Shift, Unshift)

### 🧩 Analogi: "Antrean Kereta Api"

Bayangkan sebuah gerbong kereta:
* **`push()`**: Menambah gerbong baru di **paling belakang**.
* **`pop()`**: Melepas gerbong **paling belakang** (karena rusak atau tidak dipakai).
* **`unshift()`**: Menambah gerbong baru di **paling depan**.
* **`shift()`**: Melepas gerbong **paling depan**.

---

### 📚 Teori: Perintah Manipulasi Data

Array di JavaScript punya "fungsi bawaan" yang memudahkan kita mengelola data secara dinamis tanpa harus menghitung index manual.



1.  **`.push(item)`**: Memasukkan data ke urutan terakhir.
2.  **`.pop()`**: Menghapus data terakhir.
3.  **`.unshift(item)`**: Memasukkan data ke urutan pertama (index 0).
4.  **`.shift()`**: Menghapus data pertama.
5.  **`.indexOf(item)`**: Mencari nomor index dari suatu data tertentu.

---

### 🛠️ Praktek: Kelola Tim Cybersecurity

Buka `script.js` kamu. Mari kita kelola daftar anggota tim:

```javascript
// 1. Array Awal
let teamCyber = ["Bima", "Bagus", "Deo"];
console.log("Tim Awal:", teamCyber);

// 2. Tambah Anggota di Belakang (Push)
teamCyber.push("Deni"); 
console.log("Setelah Push:", teamCyber); // ["Bima", "Bagus", "Deo", "Deni"]

// 3. Tambah Anggota di Depan (Unshift)
teamCyber.unshift("Syaifan"); 
console.log("Setelah Unshift:", teamCyber); // ["Syaifan", "Bima", ... ]

// 4. Hapus Anggota Terakhir (Pop)
teamCyber.pop(); 
console.log("Setelah Pop:", teamCyber); // Deni dihapus

// 5. Cari Posisi Anggota (IndexOf)
let posisiBagus = teamCyber.indexOf("Bagus");
console.log(`Bagus ada di index ke: ${posisiBagus}`);
```

---

### 🔍 Kenapa Ini Penting?

Dalam aplikasi nyata seperti **WhatsApp**, saat ada pesan baru masuk, aplikasi menggunakan `.unshift()` untuk memasukkan pesan tersebut ke urutan paling atas daftar percakapanmu. Tanpa *methods* ini, kita harus repot menggeser semua index data secara manual.

---

### 💡 Tantangan Part 16

1.  Buat array `wishlist` berisi 3 barang impianmu.
2.  Gunakan `.push()` untuk menambah 1 barang lagi.
3.  Gunakan `.shift()` untuk menghapus barang pertama (anggap barang itu sudah kamu beli).
4.  Gunakan `.indexOf()` untuk mencari tahu barang tertentu ada di index berapa.
5.  Tampilkan panjang array terakhir menggunakan `.length`.

---

**Udah beres di-copas ke GitHub? Kabari kalau mau lanjut ke Part 17: Array Iteration (Map & Filter) buat ngolah ribuan data sekaligus.** 🚀

---

Langsung ke **Part 17**. Ini bagian paling "sakti" buat ngolah data. Kalau di Part 16 kita nambah/hapus satu per satu, di sini kita bakal memproses **ribuan data sekaligus** cuma pakai satu baris kode.

---

# 🕵️ Part 17: Array Iteration (Map & Filter)

### 🧩 Analogi: "Mesin Fotocopy & Saringan Kopi"

* **`.map()` (Mesin Fotocopy)**: Ibarat kamu punya 10 lembar kertas kosong, lalu kamu masukkan ke mesin fotocopy untuk dicetak gambar yang sama. Hasilnya? Kamu punya 10 lembar kertas **baru** yang sudah ada gambarnya. (Mengubah semua data jadi bentuk baru).
* **`.filter()` (Saringan Kopi)**: Ibarat kamu menyeduh kopi. Ampasnya tertinggal di saringan, hanya air kopinya yang lolos ke gelas. (Mengambil data yang cuma memenuhi syarat saja).

---

### 📚 Teori: Memproses Data Secara Massal

JavaScript modern jarang pakai `for` loop biasa buat Array. Kita lebih sering pakai dua metode ini:



1.  **`.map()`**: Membuat array baru dengan cara memproses setiap elemen dari array lama. Array asli tidak berubah.
2.  **`.filter()`**: Membuat array baru yang isinya hanya elemen-elemen yang lolos seleksi (syarat tertentu).

---

### 🛠️ Praktek: Update Harga & Saring Skor

Buka `script.js` kamu. Mari kita coba simulasi menaikkan harga dan menyaring angka:

```javascript
// 1. CONTOH .MAP() (Update Harga)
const hargaDollar = [10, 20, 30, 40];
// Kita ubah ke Rupiah (Asumsi 1$ = 15.000)
const hargaRupiah = hargaDollar.map(harga => harga * 15000);

console.log("Harga dalam Rupiah:", hargaRupiah); 
// Hasil: [150000, 300000, 450000, 600000]

// 2. CONTOH .FILTER() (Saring Data)
const skorUjian = [70, 45, 90, 80, 55, 100];
// Ambil yang lulus saja (skor >= 75)
const lulus = skorUjian.filter(skor => skor >= 75);

console.log("Daftar Skor Lulus:", lulus); 
// Hasil: [90, 80, 100]
```

---

### 🔍 Kenapa Ini Penting?

Bayangkan kamu bangun aplikasi **Marketplace**. Kamu punya 1.000 produk.
* User mau lihat produk yang harganya di bawah Rp50.000? Pakai **`.filter()`**.
* Kamu mau kasih diskon 50% buat semua produk? Pakai **`.map()`**.
Semuanya selesai sekejap tanpa perlu tulis `for` loop yang panjang dan ribet.

---

### 💡 Tantangan Part 17

1.  Buat array `tahunLahir` berisi 4 tahun (contoh: 2000, 2005, 1998, 2010).
2.  Gunakan `.map()` untuk menghasilkan array `umur` (Tahun sekarang - tahun lahir).
3.  Gunakan `.filter()` untuk mengambil umur yang sudah `>= 18` tahun saja.
4.  Tampilkan hasilnya di console!

---

**Sudah beres di-copas ke GitHub? Kabari kalau mau lanjut ke Part 18: Object (Biodata Detail) buat nutup Phase 4.** 🚀

---

Langsung ke **Part 18**, materi terakhir untuk menutup **Phase 4**. Di sini kita belajar cara menyimpan data yang jauh lebih detail dan terstruktur dibanding Array.

---

# 📑 Part 18: Object (Biodata Digital)

### 🧩 Analogi: "Smartphone"

* **Array**: Ibarat cuma daftar belanjaan (Susu, Telur, Kopi). Isinya cuma list saja.
* **Object**: Ibarat sebuah **Smartphone**. Smartphone adalah satu benda, tapi punya banyak keterangan detail:
    * **Merk**: Samsung
    * **Warna**: Hitam
    * **RAM**: 8GB
    * **Nyalakan()**: Ini adalah aksi (**Method**) yang bisa dilakukan si HP.
* Jadi, Object adalah kumpulan informasi detail tentang satu benda dalam satu wadah.

---

### 📚 Teori: Key & Value

Object menggunakan kurung kurawal `{}`. Di dalamnya ada pasangan **Key** (Label) dan **Value** (Isi).

1.  **Property**: Variabel di dalam object (seperti `nama`, `umur`).
2.  **Method**: Fungsi yang nempel di dalam object (seperti `sapa()`).
3.  **Dot Notation (`.`)**: Cara memanggil isi object dengan tanda titik.



---

### 🛠️ Praktek: Membuat Profil User

Buka `script.js` kamu. Mari kita buat object untuk profil kamu sendiri:

```javascript
// --- 1. MEMBUAT OBJECT ---
const userSyaifan = {
    nama: "Syaifan",
    prodi: "Informatika",
    semester: 4,
    isScout: true,
    skills: ["HTML", "CSS", "JS"], // Object bisa menampung Array!
    
    // --- 2. MEMBUAT METHOD (Aksi) ---
    sapa: function() {
        return `Halo, saya ${this.nama} dari prodi ${this.prodi}!`;
    }
};

// --- 3. MENGAKSES DATA (Dot Notation) ---
console.log(userSyaifan.nama);      // Output: Syaifan
console.log(userSyaifan.skills[2]);   // Output: JS (Akses array di dalam object)

// --- 4. MEMANGGIL METHOD ---
console.log(userSyaifan.sapa());

// --- 5. MENAMBAH PROPERTI BARU ---
userSyaifan.hobi = "Cyber Security";
console.log(userSyaifan.hobi);
```

---

### 🔍 Kenapa Ini Penting?

Dalam database asli (seperti di **Koneka App** nanti), data produk tidak mungkin cuma nama. Pasti ada `nama`, `harga`, `gambar`, dan `stok`. Semua itu dibungkus dalam satu **Object** supaya datanya rapi dan tidak tertukar dengan produk lain.

---

### 💡 Tantangan Part 18

1.  Buat object `laptop` dengan property `merk`, `processor`, dan `ram`.
2.  Tambahkan method `start` yang menampilkan pesan: `"Laptop [merk] sedang booting..."` di console.
3.  Ubah nilai `ram` menjadi lebih tinggi (upgrade RAM).
4.  Panggil method `start` dan tampilkan object finalnya di console.

---

### 🏆 Project 4: Simple E-Commerce Catalog (Finale Phase 4)

Gabungkan Array dan Object untuk membuat katalog produk sederhana.

```javascript
// Array of Objects
const catalog = [
    { nama: "Mouse Gaming", harga: 150000, kategori: "Aksesoris" },
    { nama: "Monitor 24 inch", harga: 1200000, kategori: "Monitor" },
    { nama: "Keyboard Mech", harga: 450000, kategori: "Aksesoris" }
];

// Filter barang yang harganya di bawah 500rb
const murah = catalog.filter(item => item.harga < 500000);

console.log("Daftar Barang Murah:", murah);
```

---

**Phase 4 Resmi SELESAI.** Beresin GitHub-mu, kabari kalau sudah siap masuk ke **Phase 5: The DOM** buat bikin tampilan website kamu berubah-ubah lewat JavaScript! 🏎️💨
