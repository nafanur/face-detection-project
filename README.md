# face-detection-project
## 4. Dari hasil nomor 3, algoritme apa yang lebih akurat? Apakah Haarcascade atau HOG?
KESIMPULAN ALGORITMA:
- Haarcascade: mendeteksi 10 wajah namun perlu menyesuaikan parameter scaleFactor, minNeighbors, minSize, klo tidak bisa false positive (bukan mendeteksi wajah / sasaran).
- HOG: mendeteksi 10 wajah, namun perlu menyesuaikan parameter unsample. Lebih stabil, lebih jarang false positive, cocok untuk wajah frontal.

HOG cenderung lebih akurat dalam:
1. Deteksi wajah frontal (menghadap kamera).
2. Stabilitas hasil (tidak mudah keliru mengenali objek bukan wajah).
3. Lebih jarang false positive, karena modelnya berbasis fitur orientasi dan machine learning.

Sedangkan: Haarcascade
1. Kecepatan deteksi tinggi
2. rentan terhadap deteksi ganda atau salah deteksi (misal mendeteksi bagian baju sebagai wajah).
3. Akurasinya sangat bergantung pada parameter tuning.

Algoritma yang disarankan yang bertujuan deteksi wajah dari berbagai arah (non-frontal) adalah CNN dlib.

Jadi, menurut saya, algoritme yang lebih akurat adalah HOG. Alasannya, pengaturannya jauh lebih sederhana karena hanya membutuhkan satu parameter saja yaitu unsample, sehingga proses penyesuaian menjadi lebih praktis. Berbeda dengan Haarcascade yang memerlukan penyesuaian tiga parameter sekaligus, yaitu scaleFactor, minNeighbors, dan minSize, sehingga lebih rumit. Selain itu, HOG sangat cocok digunakan pada gambar ini karena semua wajah menghadap ke depan (frontal), sesuai dengan karakteristik deteksi HOG.
