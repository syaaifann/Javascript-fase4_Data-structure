## 📦 Part 15: Array Basic (Koleksi Data)

Array adalah variabel sakti yang bisa menampung banyak nilai sekaligus dalam satu nama. Ini adalah pondasi utama dalam mengelola struktur data yang kompleks.

### 🧩 Analogi: "Lemari Laci"
Ibarat satu lemari besar dengan banyak laci bernomor. Kita tidak perlu banyak meja (variabel) untuk menaruh barang, cukup satu lemari (array) dan ingat nomor lacinya (**Index**).

---

### 💻 Praktek Kode

```javascript
// 1. Deklarasi Array
const toolsCyber = ["Nmap", "Metasploit", "BurpSuite", "Wireshark"];

// 2. Akses Data (Ingat! Index dimulai dari 0)
console.log(`Tool favorit: ${toolsCyber[0]}`); // Nmap

// 3. Update Data
toolsCyber[2] = "SQLMap"; 

// 4. Properti .length (Cek jumlah isi)
console.log(`Total tools: ${toolsCyber.length}`);
```

---

## 🔧 Part 16: Array Methods (Manipulasi Data)

Array Methods adalah fungsi bawaan JavaScript untuk mengolah isi Array secara otomatis. Ini membuat pengelolaan data menjadi jauh lebih dinamis dan efisien.

### 🧩 Analogi: "Antrean Kereta"
* **Push/Pop:** Menambah atau menghapus gerbong dari **Belakang**.
* **Unshift/Shift:** Menambah atau menghapus gerbong dari **Depan**.

---

### 💻 Praktek Kode

```javascript
let inventory = ["Laptop", "Mouse", "Keyboard"];

// Menambah di akhir
inventory.push("Monitor");

// Menghapus di akhir
inventory.pop();

// Menambah di awal
inventory.unshift("Webcam");

// Menghapus di awal
inventory.shift();

console.log("Isi Inventory Final:", inventory);
console.log("Posisi Mouse:", inventory.indexOf("Mouse"));
```
---

## 🕵️ Part 17: Array Iteration (Map & Filter)

Dua metode paling powerful untuk mengolah data massal di JavaScript. Keduanya menciptakan array baru tanpa merusak array aslinya.

### 🧩 Analogi Singkat
* **Map:** Mengubah semua data (seperti mesin fotocopy).
* **Filter:** Menyaring data (seperti saringan kopi).

---

### 💻 Praktek Kode

```javascript
const angka = [1, 2, 3, 4, 5, 6];

// 1. Mengalikan semua angka dengan 2
const kaliDua = angka.map(n => n * 2);

// 2. Mengambil angka yang lebih besar dari 3 saja
const angkaBesar = angka.filter(n => n > 3);

console.log("Hasil Map:", kaliDua);
console.log("Hasil Filter:", angkaBesar);
```

---

## 📑 Part 18: Object (Struktur Data Detail)

Object adalah tipe data yang memungkinkan kita menyimpan banyak data dalam satu variabel dengan label (Key) yang jelas. Ini adalah cara JavaScript merepresentasikan benda di dunia nyata.

### 🧩 Analogi: "Profil KTP"
Jika Array hanya daftar nama, maka Object adalah KTP yang berisi Nama, Alamat, Tanggal Lahir, dan Pekerjaan dalam satu kartu.

---

### 💻 Praktek Kode

```javascript
const laptop = {
    brand: "Asus",
    processor: "Intel i5",
    ram: "4GB",
    isSSD: true,
    
    start: function() {
        console.log("Laptop menyala... Welcome!");
    }
};

// Akses data
console.log(`Processor: ${laptop.processor}`);

// Panggil method
laptop.start();

// Update data
laptop.ram = "8GB";
```

---
