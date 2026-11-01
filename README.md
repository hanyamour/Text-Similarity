# Text Similarity

## Deskripsi
Exercise 6 merupakan implementasi Text Similarity pada dataset artikel Quanta Physics. Latihan ini bertujuan untuk mengukur tingkat kemiripan antara query pencarian dengan kumpulan artikel menggunakan dua metode, yaitu Cosine Similarity dan Jaccard Similarity.

## Dataset
Dataset yang digunakan merupakan hasil preprocessing dan feature engineering dari latihan sebelumnya.
- Jumlah data: 775 artikel
- Sumber data: Quanta Physics
- Kolom teks yang digunakan: `Processed_text`

## Metode yang Digunakan
### 1. Cosine Similarity
- Menggunakan TF-IDF Vectorization.
- Mengubah teks menjadi representasi numerik menggunakan `TfidfVectorizer`.
- Menghitung tingkat kemiripan menggunakan `cosine_similarity`.
- Mengambil 10 artikel dengan nilai similarity tertinggi.

### 2. Jaccard Similarity
- Menggunakan Binary Count Vectorization.
- Mengubah teks menjadi representasi biner menggunakan `CountVectorizer(binary=True)`.
- Menghitung kemiripan menggunakan metrik Jaccard.
- Mengambil 10 artikel dengan nilai similarity tertinggi.

## Query Pencarian
Query yang digunakan dalam kedua metode:
`quantum physics space time gravity black hole`
Query yang sama digunakan agar hasil dari kedua metode dapat dibandingkan.

## Hasil dan Analisis

Kedua metode menghasilkan artikel The Physicist Who’s Challenging the Quantum Orthodoxy sebagai artikel dengan tingkat kemiripan tertinggi terhadap query.
Cosine Similarity memperhitungkan bobot kata menggunakan TF-IDF, sedangkan Jaccard Similarity menghitung kesamaan berdasarkan keberadaan kata dalam dokumen dan query.
Dari hasil Top 10, terdapat 7 artikel yang sama pada kedua metode. Meskipun demikian, urutan artikel dan nilai similarity yang dihasilkan berbeda karena kedua metode menggunakan pendekatan perhitungan yang berbeda.

## Tools dan Library
- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- SciPy

## Kesimpulan
Cosine Similarity dan Jaccard Similarity dapat digunakan untuk menemukan artikel yang relevan berdasarkan kemiripan teks. Namun, perbedaan cara perhitungan kedua metode menghasilkan nilai similarity dan urutan artikel yang berbeda.
