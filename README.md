# UAS-COMPUTER-VISION

##🔍 Indonesian License Plate Recognition — Data Sheet nya

Proyek ini merupakan tugas UAS yang bertujuan untuk melakukan inferensi OCR (Optical Character Recognition) pada gambar plat nomor kendaraan Indonesia, menggunakan model Visual Language Model (VLM) dari LLM Studio. Evaluasi dilakukan menggunakan metrik **CER (Character Error Rate)**.

---

## 📁 Struktur Folder
UAS/
├── test/
│ ├── image/ ← gambar plat nomor (.jpg)
│ └── label/ ← label ground truth (.txt)
├── generate_ground_truth.py
├── main.py
├── ground_truth.csv ← hasil generate dari label
├── results.csv ← hasil akhir evaluasi
└── README.md


---

## 🚀 Langkah Eksekusi

### 1. Salin Dataset
- Ambil folder `test` dari dataset **"Indonesian License Plate Recognition"** yang diberikan dosen.
- Folder `test` berisi:
  - `image/` → gambar plat nomor
  - `label/` → label dalam bentuk file `.txt`
- Salin seluruh folder ke dalam direktori `UAS/`.

### 2. Generate Ground Truth
Jalankan script berikut untuk mengubah label `.txt` menjadi file `ground_truth.csv`:

```bash
python generate_ground_truth.py


---

setelah itu 

### 3. Load Model di LLM Studio
load model di LLM Studio dengan model path sesuai dengan yang kita gunakan kalo saya "llava-v1.6-34b"
Buka terminal LLM Studio.

Jalankan:
lms ls

kalo indikasi udah ke loade
lanjut hubungkan ke API port nya
keetik di promp
lms start server

setelah terhubung succes

---

### 4. Jalankan Program Utama
jalankan di prompt 
python main.py
Program ini akan:

Membaca semua gambar dari folder test/image
Mengirimkan ke LLM Studio untuk prediksi teks
Menghitung nilai CER terhadap label ground truth
Menyimpan hasil ke results.csv

### 5. Output file Result

Kolom-kolom:
filename → nama file gambar
ground_truth → label sebenarnya dari file .txt
prediction → hasil prediksi dari LLM
CER → tingkat kesalahan (semakin kecil semakin baik)

 
