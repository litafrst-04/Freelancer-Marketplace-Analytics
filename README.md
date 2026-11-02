# Freelancer Marketplace Analytics: Profiling Talenta & Kepuasan Klien

## 📌 Project Overview
Proyek ini bertujuan untuk menganalisis data profil 1.000 freelancer global guna memahami distribusi keahlian utama (*Primary Skill*), struktur tarif per jam berdasarkan pengalaman kerja, serta faktor-faktor yang memengaruhi tingkat kepuasan klien (*Client Satisfaction*). Analisis ini difokuskan untuk memetakan talenta terbaik di berbagai negara, mengevaluasi konsistensi performa melalui sistem penilaian (*Rating*), serta menyaring status keaktifan pekerja lepas guna memberikan rekomendasi strategis bagi platform marketplace.

## 🛠️ Tools Used
* **Microsoft Excel**: Data Quality Assessment (Data Profiling & Cleaning), Pivot Tables, Pivot Charts, Slicers, dan Interactive Marketplace Dashboard.

## 📋 Scope of Work & Data Lifecycle

### 1. Pemeriksaan Data (Data Profiling)
Melakukan audit menyeluruh terhadap struktur dataset awal untuk mendeteksi anomali kualitas data. Tahap ini mengidentifikasi berbagai masalah seperti:
* Inkonsistensi penulisan jenis kelamin (variasi `f`, `FEMALE`, `m`, `male`).
* Nilai kosong (*missing values*) pada kolom numerik penting seperti Usia (*Age*), Pengalaman (*Years of Experience*), Tarif (*Hourly Rate*), Rating, hingga status keaktifan (`Is_Active`).
* Variasi format mata uang pada kolom tarif (angka murni, teks "USD", dan simbol "$").
* Keanekaragaman format status keaktifan talenta yang bercampur menjadi satu (`0`, `1`, `N`, `TRUE`, `FALSE`, `Y`, `yes`, `no`).

### 2. Pembersihan Data (Data Cleaning)
Melakukan standarisasi dan transformasi data secara sistematis, yang meliputi:
* **Standarisasi Kategori:** Menyamakan penulisan atribut kategori seperti jenis kelamin dan format keaktifan platform.
* **Pembersihan Format Tarif:** Membersihkan teks "USD" dan simbol mata uang menjadi format angka numerik murni agar dapat dihitung secara akurat.
* **Penanganan Data Kosong (Missing Values):**
  * *Age* & *Years of Experience*: Mengisi sel kosong menggunakan nilai Median masing-masing kolom (41 tahun untuk usia dan 9 tahun untuk pengalaman) agar distribusi data tetap seimbang.
  * *Hourly Rate (USD)*: Diisi menggunakan nilai median ($50/jam) untuk menjaga kestabilan tren pendapatan.
  * *Rating & Client Satisfaction*: Mengisi data kosong dengan penanda khusus (seperti "No Rating") untuk kategori data yang belum memiliki ulasan sistem.
  * *Is_Active*: Diisi dengan kategori "Unspecified" untuk menjaga objektivitas dan menghindari bias klaim keaktifan platform.

### 3. Eksplorasi Data (Data Exploration)
Menggunakan *Pivot Tables* untuk menganalisis ringkasan statistik dasar, meliputi:
* Penghitungan rata-rata tarif per jam berdasarkan keahlian utama (*Primary Skill*).
* Pemetaan sebaran rating pekerja lepas dan wilayah negara dengan tingkat kepuasan klien tertinggi.
* Analisis hubungan antara masa kerja (*Years of Experience*) dengan struktur penawaran tarif per jam.

### 4. Visualisasi Data & Interactive Dashboard
Menerjemahkan hasil analisis ke dalam bentuk visual yang interaktif menggunakan *Pivot Charts* dan *Slicers* (Filter Negara dan Gender). Dashboard ini menyajikan metrik penting seperti Total Talenta (1.000), Rata-Rata Tarif ($51.29), dan Persentase Kepuasan Klien (79.27%) secara dinamis.

## ❓ Business Questions & Insights
* **Q1:** Keahlian (*Primary Skill*) apa saja yang memiliki nilai komersial atau rata-rata tarif per jam tertinggi di dalam platform?
  * *Insight:* Bidang Cybersecurity dan Web Development mendominasi sebagai keahlian premium dengan tarif tertinggi berkisar antara $53.00 – $54.00 per jam.
* **Q2:** Apakah status keaktifan freelancer berpengaruh langsung terhadap tingkat kepuasan klien (*Client Satisfaction*)?
  * *Insight:* Pekerja lepas yang terverifikasi aktif (`TRUE`) berhasil mencetak tingkat kepuasan klien tertinggi mencapai 80.20%.
* **Q3:** Apakah lamanya pengalaman kerja otomatis menjamin tarif per jam yang lebih tinggi?
  * *Insight:* Tren tarif bersifat fluktuatif; lonjakan tarif tertinggi justru berpusat pada talenta dengan masa kerja tertentu (seperti 26 dan 39 tahun), membuktikan bahwa portofolio dan keahlian lebih dihargai di pasar global dibanding sekadar faktor masa kerja.

## 📁 Project Files
* `Freelancer_Marketplace_Portfolio.xlsx` - File utama Excel yang mencakup Laporan Kualitas Data (*Data Quality Report*), tahapan *Cleaning*, *Pivot Tables*, hingga *Interactive Marketplace Dashboard*.
