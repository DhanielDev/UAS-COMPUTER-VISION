# 🔍 Indonesian License Plate Recognition — UAS Computer Vision

<h1 align="center">
  <img src="assets/license_plate_ocr.png" width="200"/><br>
  Proyek UAS — OCR Plat Nomor 
</h1>

<h3 align="center">Integrasi Visual Language Model (VLM) dan Python untuk Inferensi Teks Otomatis</h3>

<p align="center">
  🎓 Proyek Ujian Akhir Semester UAS Komputer Vision oleh Dhaniel Beny Wardhana <br>
  🤖 Menggunakan LLM Studio & Model llava-v1.6-34b untuk mengenali plat nomor kendaraan <br>
  📊 Evaluasi dengan Character Error Rate (CER) secara otomatis
</p>

---

## 🧠 Deskripsi Singkat

Proyek ini bertujuan untuk melakukan inferensi **OCR (Optical Character Recognition)** pada gambar plat nomor kendaraan Indonesia menggunakan **Visual Language Model (VLM)** dari **LLM Studio**.

Evaluasi hasil prediksi dilakukan dengan menghitung **Character Error Rate (CER)**, sehingga dapat diketahui tingkat akurasi sistem secara objektif.

---

## 📁 Struktur Folder
```
UAS/
├── test/
│ ├── image/ # 📸 Gambar plat nomor (.jpg)
│ └── label/ # 📝 Label ground truth (.txt)
│
├── generate_ground_truth.py # ⚙️ Script untuk generate ground_truth.csv 
├── main.py # 🚀 Script utama untuk inferensi dan evaluasi LLM
├── ground_truth.csv # 📄 Data label hasil penggabungan dari .txt dan jpg tadi
└── results.csv # 📊 Hasil akhir: image,	ground_truth,	prediction,	CER_score

```
