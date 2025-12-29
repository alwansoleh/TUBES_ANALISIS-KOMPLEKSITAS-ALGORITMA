# ANALISIS KOMPLEKSITAS ALGORITMA: Bubble Sort (Iteratif) vs Merge Sort (Rekursif)

> **Tugas Besar Analisis Kompleksitas Algoritma**
> [cite_start]Studi Kasus: Perbandingan Efisiensi Pengurutan Data [cite: 1, 2]

## Tim Pengembang
Project ini disusun oleh:
1. [cite_start]**Andi Muhammad Abid Jaya** (103132400014) 
2. [cite_start]**Abdullah Ahmad Izzah** (103132430024) 
3. [cite_start]**Nur Tsalits Alwan Mubarok** (103132400039) 

---

## Gambaran Proyek
[cite_start]Penelitian ini bertujuan untuk menganalisis perbandingan kompleksitas waktu (**Time Complexity**) antara dua algoritma pengurutan dengan pendekatan yang berbeda[cite: 5]:
1.  [cite_start]**Bubble Sort** (Iteratif): Algoritma sederhana dengan kompleksitas $O(n^2)$[cite: 6, 34].
2.  [cite_start]**Merge Sort** (Rekursif): Algoritma *Divide & Conquer* dengan kompleksitas $O(n \log n)$[cite: 6, 35].

[cite_start]Kami melakukan pengujian empiris menggunakan Python dengan variasi ukuran input ($n$): `10, 20, 100, 1.000, hingga 10.000` data acak.

## Hasil Eksperimen
Berdasarkan pengujian yang telah dilakukan, berikut adalah data waktu eksekusi (dalam milidetik):

| Ukuran Data ($n$) | Merge Sort (Rekursif) | Bubble Sort (Iteratif) |
| :--- | :--- | :--- |
| **10** | 0.016 ms | 0.012 ms |
| **20** | 0.020 ms | 0.017 ms |
| **100** | 0.112 ms | 0.402 ms |
| **1.000** | 3.299 ms | 98.455 ms |
| **10.000** | **23.16 ms** | **7.494,96 ms** |

[cite_start]*(Data diambil dari hasil running program pada laporan tugas besar)* 

### Analisis Data
1.  **Pada Data Kecil ($n \le 20$):**
    Bubble Sort sedikit lebih cepat dibandingkan Merge Sort (0.012 ms vs 0.016 ms). Hal ini wajar karena Merge Sort memiliki *overhead* dari pemanggilan fungsi rekursif.
2.  **Pada Data Besar ($n = 10.000$):**
    Terjadi ledakan perbedaan waktu yang sangat signifikan.
    * **Bubble Sort** memakan waktu hingga **~7,5 detik**.
    * **Merge Sort** hanya butuh **~0,02 detik**.
    * Ini membuktikan teori bahwa pertumbuhan waktu Bubble Sort bersifat kuadratik ($n^2$), sedangkan Merge Sort jauh lebih efisien dan stabil[cite: 36, 35].

## 📝 Kesimpulan
* [cite_start]**Bubble Sort (Iteratif)** memiliki kompleksitas $O(n^2)$, sehingga **kurang efisien** dan tidak direkomendasikan untuk pengurutan data dalam skala besar[cite: 34].
* [cite_start]**Merge Sort (Rekursif)** terbukti memiliki kompleksitas $O(n \log n)$ yang **lebih efisien dan stabil** terhadap pertambahan jumlah data[cite: 35].
* [cite_start]Untuk aplikasi dunia nyata dengan data besar, **Merge Sort** adalah pilihan yang jauh lebih baik dibandingkan Bubble Sort[cite: 37].
* 
[cite_start]*Referensi Teori: GeeksforGeeks & Big-O Cheat Sheet* [cite: 39, 40]
