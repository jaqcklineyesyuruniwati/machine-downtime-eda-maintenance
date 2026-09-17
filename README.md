# ⚙️ Studi Kasus Mandiri 2: Eksplorasi Data Downtime Mesin Produksi

Proyek mandiri ini berfokus pada analisis kejadian waktu henti tak terjadwal (*downtime*) pada sepuluh unit mesin di departemen perawatan pabrik pengolahan logam (`machine_downtime.csv`). Tujuannya adalah mendeteksi mesin paling bermasalah, mengidentifikasi penyebab kegagalan dominan, serta mengevaluasi hubungan antara usia mesin dan durasi perbaikan.

---

## 📂 Alur Kerja Proyek & Langkah Analisis

1. **Memuat Dataset:** Mengimpor pustaka utama (`pandas`, `numpy`, `matplotlib`, `seaborn`) dan memuat dataset `machine_downtime.csv` untuk memeriksa dimensi serta sepuluh baris pertama.
2. **Inspeksi Struktur & Tipe Data:** Memeriksa tipe data setiap kolom menggunakan `df.info()` dan `df.dtypes` untuk memastikan kolom kategorik seperti `ID_Mesin`, `Penyebab_Downtime`, dan `Shift_Kejadian` terbaca dengan benar.
3. **Pembersihan Data (Data Cleaning):**
   * **Imputasi Missing Value:** Mengatasi nilai kosong pada kolom `Biaya_Perbaikan_Ribu_Rupiah` menggunakan nilai **median** agar tahan terhadap *outlier* kerusakan berat.
   * **Koreksi Data Tidak Logis:** Menangani *data entry error* berupa nilai negatif pada kolom `Usia_Mesin_Tahun` menggunakan fungsi nilai absolut (`.abs()`) untuk menyelamatkan baris data.
4. **Visualisasi Data & EDA:**
   * **Visualisasi 1 (Countplot):** Grafik batang frekuensi untuk mengidentifikasi penyebab utama downtime yang paling dominan di pabrik.
   * **Visualisasi 2 (Boxplot):** Membandingkan sebaran durasi *downtime* (`Durasi_Downtime_Menit`) di setiap unit mesin (`ID_Mesin`) untuk mendeteksi mesin paling kritis.
   * **Visualisasi 3 (Scatter Plot):** Menguji hubungan antara usia mesin (*Usia_Mesin_Tahun*) dan durasi perbaikan (*Durasi_Downtime_Menit*).

---

## 🛠️ Tech Stack
* **Python**
* **Pandas & NumPy** (Manipulasi & Pembersihan Data)
* **Matplotlib & Seaborn** (Visualisasi Statistik)

---

## 💡 Temuan Utama & Insight Bisnis
* **Penyebab Dominan:** Sebagian besar gangguan mesin di pabrik didominasi oleh masalah kerusakan mekanis dan elektrikal.
* **Mesin Kritis:** Mesin dengan ID tertentu (seperti M06) teridentifikasi sebagai unit paling kritis dengan durasi *downtime* tertinggi.
* **Korelasi Usia Mesin:** Terdapat korelasi positif di mana semakin tua usia mesin, durasi perbaikannya cenderung semakin lama.
* **Rekomendasi Manajemen:** Menerapkan strategi *preventive maintenance* berbasis usia mesin dan memperketat inspeksi pada komponen utama guna menekan waktu henti produksi.

---

## 🚀 Cara Menjalankan
1. Pastikan file dataset `machine_downtime.csv` berada dalam satu direktori dengan notebook.
2. Buka file `.ipynb` menggunakan **Jupyter Notebook** atau **Google Colab**.
3. Jalankan sel kode secara berurutan.
