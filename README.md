# osintktp
Tool termux untuk melakukan validasi dan pencarian data NIK (Nomor Induk Kependudukan)

✨ Fitur Utama
-✅ Validasi NIK - Pengecekan struktur dan validitas NIK
-🔍 Single NIK Check - Pencarian data lengkap dari database
-📁 Batch Processing - Proses multiple NIK dari file teks
-📊 Analisis Data - Ekstraksi informasi dari NIK (provinsi, tanggal lahir, gender)
-💾 Save Results - Penyimpanan hasil dalam format JSON

🚀 Instalasi

Prasyarat
pip install requests colorama

Cara Menjalankan
python osintktp.py

🎯 Penggunaan
1. Cek Single NIK
   [1] Masukkan NIK: 3273012301010004
Tool akan:
-Validasi format NIK
-Query database online
-Tampilkan data lengkap (nama, alamat, usia, dll)

2. Validasi NIK
   [2] Masukkan NIK: 3273012301010004
Fitur ini mengecek:
-Panjang 16 digit
-Format angka
-Kode provinsi valid
-Logika tanggal lahir

3. Batch Process
   [3] Nama file: list_nik.txt
Format file list_nik.txt:
3273012301010004
3273012301010005
3273012301010006
(contoh)

📁 Struktur Data
Format NIK
AA BB CC DDEE FFFF G
│  │  │  ││   │    │
│  │  │  ││   │    └─ Nomor urut
│  │  │  ││   └─ Kode kecamatan
│  │  │  └└─── Tanggal lahir (DDEE)
│  │  └─ Kode kabupaten/kota
│  └─ Kode provinsi
└─ Kode wilayah
