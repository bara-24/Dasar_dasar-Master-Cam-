# CNC-Dasar_rasyd
Tugas Trasformasi Digital ; Muhammad Rasyd Prayogi NIM 2024006013
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animasi Dasar Gerakan CNC</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
        }
        .cnc-machine {
            position: relative;
            width: 400px;
            height: 300px;
            margin: 50px auto;
            border: 2px solid #333;
            background-color: #ddd;
        }
        .table {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 50px;
            background-color: #888;
        }
        .spindle {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #f00;
            border-radius: 50%;
            top: 100px;
            left: 50px;
            animation: move-spindle 5s infinite linear;
        }
        .workpiece {
            position: absolute;
            bottom: 50px;
            left: 150px;
            width: 100px;
            height: 50px;
            background-color: #0f0;
        }
        @keyframes move-spindle {
            0% { left: 50px; top: 100px; }
            25% { left: 300px; top: 100px; }
            50% { left: 300px; top: 200px; }
            75% { left: 50px; top: 200px; }
            100% { left: 50px; top: 100px; }
        }
        .circular-move {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #00f;
            border-radius: 50%;
            top: 150px;
            left: 190px;
            animation: circular 4s infinite linear;
        }
        @keyframes circular {
            0% { transform: rotate(0deg) translateX(50px) rotate(0deg); }
            100% { transform: rotate(360deg) translateX(50px) rotate(-360deg); }
        }
    </style>
</head>
<body>
    <p><strong>Pengantar:</strong> Selamat datang di animasi dasar gerakan CNC. Animasi ini dirancang untuk membantu pemahaman tentang bagaimana mesin CNC bergerak dalam proses manufaktur.</p>
    <h1>Animasi Dasar Gerakan CNC</h1>
    <p>Animasi ini menunjukkan gerakan linier spindle (merah) dan gerakan melingkar (biru) pada mesin CNC sederhana.</p>
    <div class="cnc-machine">
        <div class="spindle"></div>
        <div class="circular-move"></div>
        <div class="workpiece"></div>
        <div class="table"></div>
    </div>
    <p>Gerakan linier: Spindle bergerak horizontal dan vertikal.</p>
    <p>Gerakan melingkar: Elemen biru berputar mengelilingi titik pusat.</p>
    <p><strong>Penutup:</strong> Terima kasih telah melihat animasi ini. Untuk pembelajaran lebih lanjut, lihat materi dasar CNC di file terkait.</p>
</body>
</html>

# Materi Dasar CNC (Computer Numerical Control)

## Pengantar
Computer Numerical Control (CNC) adalah teknologi yang menggunakan komputer untuk mengontrol mesin perkakas secara otomatis. CNC memungkinkan presisi tinggi dalam proses manufaktur, seperti pemotongan, penggilingan, dan pemborosan bahan.

## Apa Itu CNC?
CNC adalah sistem di mana mesin dikendalikan oleh program komputer yang berisi instruksi numerik. Program ini diterjemahkan menjadi gerakan mesin untuk menghasilkan produk sesuai desain.

### Keuntungan CNC:
- Presisi tinggi
- Efisiensi waktu
- Reproduksi yang konsisten
- Mengurangi kesalahan manusia

## Komponen Utama Mesin CNC
1. **Komputer/Kontroler**: Mengelola program dan mengirim sinyal ke mesin.
2. **Mesin Perkakas**: Bagian fisik seperti spindle, meja kerja, dan motor.
3. **Drive dan Motor**: Menggerakkan sumbu (X, Y, Z).
4. **Sensor dan Feedback**: Memantau posisi dan kecepatan.
5. **Software**: Untuk membuat dan mensimulasikan program CNC.

## Bahasa Pemrograman CNC: G-Code
G-Code adalah bahasa standar untuk memprogram mesin CNC. Kode-kode dimulai dengan huruf G (Gerakan) atau M (Miscellaneous).

### Contoh Kode Dasar:
- `G00`: Gerakan cepat (rapid move)
- `G01`: Gerakan linier (linear move)
- `G02/G03`: Gerakan melingkar (circular move)
- `M03`: Mulai spindle
- `M05`: Stop spindle

### Contoh Program Sederhana:
```
G21 ; Unit dalam mm
G90 ; Mode absolut
G00 X0 Y0 Z10 ; Posisi awal
M03 S1000 ; Start spindle 1000 RPM
G01 Z-5 F100 ; Turun ke kedalaman 5mm dengan feed 100mm/min
G01 X50 Y0 ; Gerak ke X50
G01 X50 Y50 ; Gerak ke Y50
G01 X0 Y50 ; Gerak ke X0
G01 X0 Y0 ; Kembali ke awal
G00 Z10 ; Naik
M05 ; Stop spindle
M30 ; End program
```

## Proses Kerja CNC
1. Desain model menggunakan CAD (Computer-Aided Design).
2. Konversi ke CAM (Computer-Aided Manufacturing) untuk menghasilkan G-Code.
3. Simulasi program untuk memastikan keamanan.
4. Jalankan pada mesin CNC.
5. Inspeksi dan finishing.

## Kesimpulan
CNC adalah fondasi manufaktur modern. Memahami dasar-dasar ini penting untuk memulai dalam bidang teknik mesin. Untuk pembelajaran lebih lanjut, praktik dengan simulator CNC atau mesin sederhana direkomendasikan.

## Referensi
- Buku: "CNC Programming Handbook" oleh Peter Smid
- Situs: cnc.com atau haascnc.com
