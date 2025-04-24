# Text Classification untuk Deteksi Depresi

## Pendahuluan
Proyek ini bertujuan untuk mengembangkan model klasifikasi teks yang dapat mendeteksi depresi berdasarkan input teks yang diberikan. Dengan menggunakan teknik pemrosesan bahasa alami (NLP) dan algoritma pembelajaran mesin, proyek ini bertujuan untuk memberikan wawasan tentang bagaimana teks dapat dianalisis untuk mengidentifikasi tanda-tanda depresi.

## Dataset
Sumber dataset: https://drive.google.com/uc?id=1ogkVzRs9HptE5nY1dyiQUnB4DsBlFswS

Dataset yang digunakan dalam proyek ini diambil dari sumber online dan terdiri dari dua kolom:
- **clean_text**: Teks yang telah dibersihkan dan diproses.
- **is_depression**: Label biner yang menunjukkan apakah teks tersebut mengindikasikan depresi (1) atau tidak (0).

## Proses Pengolahan Data
1. **Pembersihan Teks**: Teks dibersihkan dari karakter yang tidak relevan dan diubah menjadi huruf kecil.
2. **Penghapusan Stopwords**: Kata-kata umum yang tidak memberikan makna signifikan dihapus.
3. **Lematisasi**: Kata-kata diubah menjadi bentuk dasarnya untuk mengurangi variasi kata.

## Metode
1. **Pra-pemrosesan Data**:
   - Unduh sumber daya NLTK yang diperlukan.
   - Bersihkan data teks dengan menghapus karakter khusus dan kata-kata yang tidak penting.
   - Terapkan lemmatization untuk mengurangi kata-kata ke bentuk dasarnya.

2. **Ekstraksi Fitur**:
   - Gunakan TF-IDF (Term Frequency-Inverse Document Frequency) untuk mengubah data teks menjadi format numerik yang sesuai untuk machine learning.

3. **Pelatihan Model**:
   - Bagi dataset menjadi set pelatihan (66%) dan set pengujian (34%).
   - Latih classifier Support Vector Machine (SVM) pada data pelatihan.

4. **Evaluasi Model**:
   - Evaluasi model menggunakan precision, recall, dan AUROC (Area Under the Receiver Operating Characteristic Curve).
   - Visualisasikan hasil menggunakan matriks kebingungan.

## Hasil
Setelah pelatihan, model dievaluasi menggunakan metrik berikut:
- **Precision**: 0.9756
- **Recall**: 0.9399
- **AUROC**: 0.9915
