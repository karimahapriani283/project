# Project

# Healthcare Patient Visit Analysis (SQL)  

## 📌 Deskripsi 
Proyek Proyek ini bertujuan untuk menganalisis data kunjungan pasien guna mendapatkan wawasan mengenai demografi pasien, tren diagnosis (ICD Codes), frekuensi kunjungan (utilisasi), dan prosedur medis yang paling sering dilakukan.  
Analisis ini sangat berguna bagi manajemen rumah sakit untuk memahami pola kesehatan pasien dan mengoptimalkan layanan kesehatan.  

## 🛡️ Catatan Keamanan Data (Data Privacy) 
Demi menjaga kerahasiaan informasi medis dan mematuhi etika data: 
1. **Anonimisasi:** Semua identitas pribadi seperti Nama, Alamat, dan No. HP telah dihapus dari dataset.
2. **Masking:** `patient_id` telah disamarkan dan tidak merepresentasikan nomor rekam medis asli.
3. **Transformasi:** Tanggal lahir digunakan hanya untuk menghitung rentang usia (*age grouping*) guna keperluan analisis statistik.  

## 📊 Analisis yang Dilakukan 
Dalam proyek ini, saya melakukan beberapa tahapan analisis menggunakan SQL: 
- **Step 1: Demografi Pasien**   - Membersihkan format tanggal lahir dari teks menjadi format `DATE`.   - Mengelompokkan pasien berdasarkan rentang usia (0-17, 18-39, 40-64, 65+).
- **Step 2: Tren Diagnosis (ICD Code)**   - Mengidentifikasi 10 diagnosis tertinggi.   - Melakukan *breakdown* diagnosis berdasarkan jenis kelamin dan kelompok usia.
  - **Step 3: Utilisasi Kunjungan**   - Menghitung rata-rata kunjungan per pasien.   - Mengidentifikasi "High Utilizers" (pasien dengan kunjungan ≥ 4 kali) untuk manajemen perawatan kronis.
  - **Step 4: Analisis Prosedur (CPT Code)**   - Peringkat prosedur medis yang paling sering dilakukan.  

## 🛠️ Alat & Bahasa 
- **Bahasa:** SQL (MySQL)
- **Konsep SQL:** `CASE Statements`, `Aggregate Functions (COUNT, SUM, AVG)`, `Subqueries`, `String to Date Conversion`, `HAVING Clause`.  

## 📁 Cara Menggunakan 
Cukup salin query dari file `analysis_query.sql` dan jalankan pada database yang memiliki skema tabel `patient_visits`.
