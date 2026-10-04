# ⚡ Simulation Running Text

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=200&section=header&text=Simulation%20Running%20Text&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=35" alt="Simulation Running Text Banner"/>
</p>

<p align="center">
  <strong>Simulasi teks berjalan berbasis rangkaian digital dan LED menggunakan Logisim-evolution.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Project-Sistem%20Digital-2563EB?style=for-the-badge" alt="Project"/>
  <img src="https://img.shields.io/badge/Logisim--evolution-2.13.8-FF6B35?style=for-the-badge" alt="Logisim"/>
  <img src="https://img.shields.io/badge/Hardware-LED%20Matrix-22C55E?style=for-the-badge" alt="LED Matrix"/>
  <img src="https://img.shields.io/badge/Status-Completed-16A34A?style=for-the-badge" alt="Status"/>
</p>

---

## 📖 About The Project

**Simulation Running Text** adalah proyek simulasi rangkaian digital untuk membuat tampilan **teks berjalan (running text)** menggunakan rangkaian logika digital dan LED.

Project ini dibuat sebagai bagian dari tugas mata kuliah **Sistem Digital** dan berfokus pada penerapan konsep:

* Digital Logic
* Logic Gates
* Clock / Timing
* LED Display
* Boolean Logic
* Sequential Logic
* Pattern Generation

Simulasi dibuat menggunakan **Logisim-evolution** sehingga rangkaian dapat dirancang, diuji, dan diamati tanpa membutuhkan perangkat keras fisik.

---

## ✨ Features

* 🖥️ Simulasi running text menggunakan LED
* ⏱️ Clock sebagai pengatur timing rangkaian
* 🔌 Implementasi logic gates
* 💡 LED sebagai media output
* 🔄 Pergerakan pola teks secara berurutan
* 🧩 Modular circuit menggunakan subcircuit
* 📊 Model pola LED menggunakan spreadsheet
* 🧪 Dapat diuji langsung melalui simulator

---

## 🧠 How It Works

Secara sederhana, sistem bekerja dengan alur:

```text
┌─────────┐
│  Clock  │
└────┬────┘
     │
     ▼
┌───────────────┐
│ Timing /      │
│ Control Logic │
└──────┬────────┘
       │
       ▼
┌───────────────┐
│ Logic Gates   │
│ AND / OR /... │
└──────┬────────┘
       │
       ▼
┌───────────────┐
│ Character /   │
│ LED Pattern   │
└──────┬────────┘
       │
       ▼
┌───────────────┐
│ LED Display   │
└──────┬────────┘
       │
       ▼
   RUNNING TEXT
```

### 🔹 1. Clock

Clock menghasilkan sinyal digital secara periodik yang digunakan sebagai dasar perubahan posisi teks.

### 🔹 2. Timing & Control

Sinyal clock diproses untuk menentukan kapan pola LED berubah.

### 🔹 3. Logic Gates

Beberapa gerbang logika digunakan untuk mengatur kombinasi sinyal yang akan diteruskan ke bagian output.

Komponen yang digunakan antara lain:

* AND Gate
* OR Gate
* NOT / Inverter
* Wiring
* Clock
* LED

### 🔹 4. LED Pattern

Setiap karakter direpresentasikan sebagai kombinasi LED **ON/OFF**.

Contoh sederhana:

```text
  █ █
 █   █
 █████
 █   █
 █   █
```

Kombinasi tersebut kemudian digeser secara bertahap untuk menghasilkan efek **running text**.

### 🔹 5. LED Display

Output akhir ditampilkan melalui LED sehingga pola karakter dapat diamati secara visual.

---

## 🛠️ Tools & Technologies

| Tool                    | Purpose                                              |
| ----------------------- | ---------------------------------------------------- |
| **Logisim-evolution**   | Merancang dan menjalankan simulasi rangkaian digital |
| **Excel**               | Membuat/model pola LED                               |
| **Digital Logic Gates** | Membentuk logika pengendali display                  |
| **LED**                 | Menampilkan output running text                      |
| **Git & GitHub**        | Version control dan penyimpanan project              |

---

## 📁 Repository Structure

```text
Simulation-Running-Text/
│
├── 📄 HDP_Simulation_Running_Text.circ
│   └── Main Logisim-evolution circuit
│
├── 📊 HDP_Model_LED.xlsx
│   └── LED pattern / modeling
│
├── ⚙️ 1. logisim-win-2.7.1.exe
│   └── Logisim executable
│
└── 📖 README.md
    └── Project documentation
```

> **Note:** File `.circ` merupakan file utama untuk simulasi rangkaian.

---

## 🚀 Getting Started

### 1. Clone Repository

```bash
git clone https://github.com/herdiansyahdp/Simulation-Running-Text.git
```

Masuk ke folder project:

```bash
cd Simulation-Running-Text
```

### 2. Open the Circuit

Buka file:

```text
HDP_Simulation_Running_Text.circ
```

menggunakan **Logisim-evolution**.

### 3. Run Simulation

Setelah circuit terbuka:

1. Jalankan simulator.
2. Aktifkan clock.
3. Amati perubahan output LED.
4. Perhatikan pola karakter yang bergerak.
5. Uji perubahan clock/timing jika diperlukan.

---

## 🔬 Circuit Architecture

Project ini menggunakan pendekatan modular dengan beberapa bagian circuit/subcircuit.

Struktur utamanya dapat digambarkan sebagai:

```text
                 ┌─────────────┐
                 │    CLOCK    │
                 └──────┬──────┘
                        │
                        ▼
              ┌──────────────────┐
              │ Timing / Counter  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │  Control Logic   │
              │  AND / OR / NOT  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Character Pattern│
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │   LED DISPLAY    │
              └────────┬─────────┘
                       │
                       ▼
                 💡 OUTPUT
```

---

## 💡 LED Pattern Concept

Running text pada dasarnya dibangun dari kumpulan kondisi digital:

```text
1 = LED ON
0 = LED OFF
```

Contoh representasi sederhana:

```text
01010
10101
11111
10001
10001
```

Setiap kombinasi `0` dan `1` menentukan LED mana yang aktif.

Dengan mengubah posisi pola secara periodik menggunakan clock, karakter akan terlihat bergerak dari satu sisi ke sisi lainnya.

---

## 🎯 Learning Objectives

Melalui project ini, beberapa konsep Sistem Digital dapat dipraktikkan secara langsung:

* Memahami fungsi **logic gates**
* Memahami konsep **digital signal**
* Memahami penggunaan **clock**
* Membuat rangkaian digital secara modular
* Mengubah data menjadi pola LED
* Memahami hubungan antara input, proses, dan output
* Mengimplementasikan teori logika digital ke dalam simulasi

---

## 📚 Course Context

**Mata Kuliah:** Sistem Digital
**Project:** Simulation Running Text
**Platform:** Logisim-evolution
**Semester:** 2

Project ini dibuat sebagai media pembelajaran dan implementasi konsep rangkaian digital.

---

## 👨‍💻 Author

<p align="center">
  <strong>Herdiansyah Dwi Putra</strong>
</p>

<p align="center">
  Teknik Informatika
</p>

<p align="center">
  <a href="https://github.com/herdiansyahdp">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github" alt="GitHub"/>
  </a>
</p>

---

## 📌 Project Status

```text
████████████████████████████████████████ 100%
```

**Status:** ✅ Completed

---

## 📝 Notes

Project ini dibuat untuk kebutuhan pembelajaran mata kuliah **Sistem Digital**.

Pengembangan lebih lanjut dapat dilakukan dengan menambahkan:

* 🔤 Karakter/huruf yang lebih banyak
* ⏩ Pengaturan kecepatan running text
* 🔁 Pengaturan arah pergerakan teks
* 💡 LED matrix yang lebih besar
* 🎛️ Input untuk memilih teks
* 🔢 Counter dan register tambahan
* 🖥️ Implementasi ke perangkat keras nyata

---

## ⭐ Support

Jika project ini membantu atau menarik untuk dipelajari, jangan lupa memberikan **⭐ Star** pada repository.

<p align="center">
  <i>Built with digital logic, patience, and a lot of logic gates. ⚡</i>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:0f172a&height=100&section=footer" alt="Footer"/>
</p>
