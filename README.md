# SBYDEV_BABAK1_spartans_AdvanceHealthReport_ITB
SPARTANS: Health Risk Prediction &amp; Prevention Analysis
<div align="center">
  <img src="https://i.ibb.co/b3F3S3C/health-logo.png" alt="Health Analytics Logo" width="150"/>
  <h1>Analisis Faktor Risiko Penyakit Kronis</h1>
  <p>
    Sebuah analisis data eksploratif untuk mengidentifikasi faktor risiko utama penyakit Jantung, Diabetes, dan Hipertensi dari data rekam medis pasien. Proyek ini bertujuan untuk memberikan rekomendasi strategis bagi program deteksi dini yang lebih efektif.
  </p>
</div>

---

### <p align="center">Tech Stack yang Digunakan</p>
<p align="center">
  <a href="https://www.python.org" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/>
  </a>
  <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original-wordmark.svg" alt="pandas" width="40" height="40"/>
  </a>
  <a href="https://numpy.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" alt="numpy" width="40" height="40"/>
  </a>
  <a href="https://matplotlib.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/matplotlib/matplotlib-original.svg" alt="matplotlib" width="40" height="40"/>
  </a>
  <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer">
    <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/>
  </a>
  <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer">
    <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit-learn" width="40" height="40"/>
  </a>
  <a href="https://ydata-profiling.ydata.ai/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/ydataai/ydata-profiling/master/docs/src/assets/logo_light.svg" alt="ydata-profiling" width="40" height="40"/>
  </a>
</p>

---

## 🎯 Latar Belakang Masalah

Penyakit tidak menular seperti jantung, diabetes, dan hipertensi menjadi beban utama bagi sistem kesehatan modern. Biaya penanganan yang tinggi dan penurunan kualitas hidup menuntut pendekatan preventif. Analisis data rekam medis pasien dapat mengungkap pola tersembunyi yang krusial untuk deteksi dini dan intervensi yang efektif. Proyek ini bertujuan untuk mengidentifikasi faktor-faktor paling signifikan yang berkontribusi terhadap ketiga diagnosa tersebut.

## ❓ Pertanyaan Analitis Kunci

1.  **Demografi**: Bagaimana distribusi usia dan jenis kelamin pada pasien yang terdiagnosis?
2.  **Gaya Hidup**: Apakah ada korelasi kuat antara merokok dan aktivitas fisik dengan diagnosa penyakit?
3.  **Indikator Medis**: Seberapa besar pengaruh kolesterol dan riwayat penyakit keluarga terhadap kemungkinan diagnosa?

## 🛠️ Tahapan Proyek

### 1. Data Processing & Preprocessing

Langkah awal adalah membersihkan dan mempersiapkan data agar siap untuk dianalisis.
- **Standardisasi Nilai**: Menyamakan format data kategorikal (misal: "Laki-laki" & "Pria" menjadi `1`).
- **Encoding**: Mengubah data kategorikal (seperti `Jenis_Kelamin`, `Cholesterol`, `Merokok`) menjadi format numerik untuk pemrosesan.
- **Konversi Tipe Data**: Mengubah kolom `Tanggal_Pemeriksaan` menjadi format *datetime* dan memisahkan `Tekanan_Darah` menjadi kolom *systolic* dan *diastolic* sebelum dikategorikan.
- **Mengatasi Nilai Kosong**: Mengisi data yang hilang (`NaN`) pada fitur-fitur kunci menggunakan `KNNImputer` untuk menjaga distribusi data.

### 2. Exploratory Data Analysis (EDA)

Analisis dilakukan untuk memahami karakteristik dan menemukan pola dalam data.
- **Analisis Univariate**: Melihat distribusi setiap variabel. Ditemukan bahwa mayoritas pasien berada di rentang usia 40-80 tahun, dan diagnosa paling umum adalah "Sehat", diikuti oleh "Hipertensi".
- **Analisis Bivariate**: Mencari hubungan antar dua variabel, seperti antara status merokok dengan diagnosa penyakit jantung.
- **Analisis Multivariat**: Menggunakan `ydata-profiling` untuk menghasilkan laporan komprehensif, termasuk heatmap korelasi antar semua variabel numerik untuk melihat kekuatan hubungan antar variabel.

### 3. Visualisasi dan Hasil Rekomendasi

Visualisasi kunci dibuat untuk menyoroti temuan paling penting. Salah satunya adalah visualisasi di bawah ini yang menunjukkan hubungan antara diagnosa penyakit dengan tingkat kolesterol.

<div align="center">
  <img src="https://i.ibb.co/3kXpYvC/diagnosa-vs-kolesterol.png" alt="Diagnosa vs Kolesterol" />
  <p><i>Grafik ini menunjukkan bahwa pasien dengan diagnosa Penyakit Jantung, Hipertensi, dan Diabetes cenderung memiliki tingkat kolesterol tinggi.</i></p>
</div>

## 💡 Rekomendasi Strategis

Berdasarkan analisis yang telah dilakukan, berikut adalah 3 rekomendasi yang dapat ditindaklanjuti:

1.  **Prioritaskan Skrining Hipertensi untuk Usia 40+**.
    - **Alasan**: Hipertensi adalah kondisi paling umum kedua setelah "Sehat", dengan konsentrasi pasien di usia paruh baya ke atas.
    - **Tindakan**: Mengadakan program pemeriksaan tekanan darah gratis atau bersubsidi yang menargetkan populasi usia di atas 40 tahun.

2.  **Kampanye Anti-Merokok dengan Fokus Risiko Penyakit Jantung**.
    - **Alasan**: Analisis menunjukkan adanya asosiasi yang jelas antara status merokok dengan diagnosa Penyakit Jantung.
    - **Tindakan**: Membuat materi kampanye yang spesifik menampilkan data visual hubungan merokok dengan risiko penyakit jantung.

3.  **Edukasi Kolesterol sebagai Faktor Risiko Lintas-Penyakit**.
    - **Alasan**: Visualisasi menunjukkan pasien dengan Penyakit Jantung, Hipertensi, dan Diabetes cenderung memiliki distribusi kolesterol pada level 'tinggi'.
    - **Tindakan**: Mengembangkan program edukasi "Kenali Kolesterolmu" sebagai bagian dari manajemen risiko bagi penderita hipertensi dan diabetes.

## 🚀 Cara Menjalankan Proyek Ini

1.  **Clone repository ini:**
    ```bash
    git clone [URL-REPOSITORY-ANDA]
    ```
2.  **Install dependencies yang dibutuhkan:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn ydata-profiling
    ```
3.  **Jalankan Jupyter Notebook atau script Python:**
    Pastikan file `kesehatan.csv` berada di direktori yang sama.

4.  **Lihat hasil laporan EDA:**
    Buka file `laporan_eda.html` yang dihasilkan di browser kamu.
