Proyek Deteksi Kucing dengan YOLOv8
Proyek ini adalah implementasi dari model Object Detection menggunakan arsitektur YOLOv8 untuk mendeteksi objek "Kucing" pada gambar. Proyek ini mencakup seluruh alur kerja machine learning, mulai dari pengumpulan data, anotasi, training, hingga evaluasi model.

(<-- Ganti dengan screenshot hasil prediksi terbaik Anda)

📖 Latar Belakang
Proyek ini dibuat sebagai bagian dari tugas Ujian Akhir Semester untuk mata kuliah Pengolahan Citra. Tujuannya adalah untuk memahami dan menerapkan konsep-konsep Computer Vision secara praktis, khususnya dalam bidang deteksi objek.

🛠️ Alur Kerja Proyek
Proses pengembangan model ini dibagi menjadi beberapa tahap utama:

Pengumpulan Data: Mengumpulkan lebih dari 500 gambar kucing dari berbagai sumber untuk membuat dataset yang beragam.

Anotasi Data: Menggunakan platform Roboflow untuk memberi label pada setiap gambar. Setiap kucing diberi kotak pembatas (bounding box) dengan kelas Kucing.

Preprocessing & Augmentasi: Dataset kemudian diproses dengan:

Preprocessing: Ukuran gambar diseragamkan menjadi 640x640 piksel.

Augmentasi: Data training diperbanyak 3x lipat dengan teknik seperti flip (horizontal) dan perubahan brightness untuk membuat model lebih tangguh.

Training Model: Model dilatih di lingkungan Google Colab dengan memanfaatkan GPU. Dua sesi training dilakukan untuk perbandingan:

Training pertama selama 50 epoch.

Training kedua selama 75 epoch.

Evaluasi: Performa model dievaluasi menggunakan metrik seperti mAP (mean Average Precision), Confusion Matrix, dan PR Curve untuk menganalisis akurasi dan jenis kesalahan yang dibuat.

🚀 Hasil dan Analisis
Setelah melakukan dua sesi training, diperoleh hasil sebagai berikut:

Training 50 Epoch: Menghasilkan model dengan performa puncak dan keseimbangan terbaik, dengan skor mAP@0.5 sebesar 0.876.

Training 75 Epoch: Model menjadi lebih sensitif dalam menemukan kucing (recall lebih tinggi), namun skor mAP sedikit menurun menjadi 0.851. Ini mengindikasikan model mulai mengalami sedikit overfitting.

Kesimpulan: Model yang dilatih selama 50 epoch terpilih sebagai model final karena memberikan performa akurasi keseluruhan yang paling optimal.

🔧 Teknologi yang Digunakan
Model: YOLOv8

Library Utama: Ultralytics, PyTorch

Platform Anotasi: Roboflow

Lingkungan Training: Google Colab