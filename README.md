# Menyelesaikan Permasalahan Human Resource
---
## Business Understanding
Jaya-Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Walaupun telah menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitas dalam mengelola karyawan. Hal ini berimbas tingginya *attrition rate* (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%. 

### Permasalahan Bisnis
1. Apa faktor utama yang menyebabkan tingginya Attrition di perusahaan Jaya-Jaya Maju
2. Apakah terdapat perbedaan tingkat Attrition berdasarkan tingkat JobLevel karyawan?
3. Bagaimana pola karakteristik karyawan yang memiliki risiko tinggi untuk keluar dari perusahaan?

### Cakupan Proyek
Proyek ini mencakup:
1. **Data Understanding:** Menmahami data untuk melihat pola awal attrition karyawan.
2. **Data Cleaning & Preparation:** Membersihkan dan memproses data
3. **Exploratory Analysis:** Menganalisis hubungan variabel seperti job role, income, overtime, dan satisfaction terhadap attrition.
4. **Modeling:** Mengembangkan model untuk memprediksi attrition.
5. **Dashboard:** Menyajikan insight dalam bentuk visual interaktif untuk HR.
6. **Business Insight:** Menarik kesimpulan dari hasil analisis dan memberikan rekomendasi retensi karyawan.

### Persiapan
**Sumber data:** [Employee Data](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee 'Dicoding Github - Employee Data')
**Setup environment:**
- Install library yang dipakai
```
pip install -r requirements. txt
```
- Buka prediction.py dan tulis nama file yang akan diprediksi
```
data_to_predict = pd.read_csv('YOUR FILE') 
```
- Jalankan prediction.py
```
python prediction.py
```

## Business Dashboard
Dashboard ini dibuat untuk untuk memberikan gambaran cepat kepada tim HR mengenai faktor-faktor utama yang memengaruhi attrition karyawan. Dengan visualisasi data yang ringkas, dashboard ini membantu mengubah data HR menjadi insight yang mudah dipahami untuk pengambilan keputusan.
[Link Dashboard](https://datastudio.google.com/reporting/f180bcae-2704-4dbd-a35c-ff465ccf20cf)
[Dashboard](evitamyna_dicoding-dashboard.jpg)

## Conclusion

---

## Conclusion 
Berdasarkan analisis data, diperoleh beberapa kesimpulan, yaitu
1. Faktor-Faktor Penyebab Attrition
    - Faktor Pekerjaan
      - Karyawan yang lembur memiliki risiko keluar paling tinggi
      - Job role terteentu memiliki Attrition lebih tinggi
      - Frekuensi business travel juga meningkatkan risiko
    - Faktor Karier & Kompensasi
      - Karyawan dengan Job Level, gaji, dan stock option yang rendah lebih rentan keluar
    - Faktor Pengalaman Kerja
      - Karyawan dengan masa kerja dan lama kerja dengan manager rendah lebih mudah keluar
    - Faktor Psikologis
      - Kepuasan kerja, lingkungan, relasi, dan work life balance yang rendah meningkatkan attrition

2. Perbedaan Attrition berdasarkan JobLevel
    - JobLevel 1 memiliki attrition tertinggi
    - Semakin tinggi level jabatan maka attrition semakin rendah, sehingga Entry-level employees paling rentan keluar

3. Pola karyawan high-risk untuk keluar:
    - Usia muda
    - Belum menikah
    - Job level rendah
    - Gaji lebih rendah
    - Sering lembur
    - Jarak rumah jauh
    - Sering pindah kerja sebelumnya
    - Masa kerja pendek
    - Kepuasan kerja dan work life balance rendah

4. Model Terbaik
   Model terbaik yang digunakan adalah Logistic Regression, dengan metrik performa sebagai berikut:
    - ROC AUC: 0.85 
    - Accuracy: 0,70
    - Precision: 0,37
    - Recall: 0,85
    - F1-Score: 0,51
   Hal ini menunjukkan bahwa model mampu mengidentifikasi sebagian besar kasus attrition, yang sangat penting dalam konteks bisnis untuk melakukan tindakan pencegahan lebih awal.


### Rekomendasi Action Items
1. **Kurangi Overtime:** Mengurangi jam kerja lembur untuk menekan tingkat kelelahan (burnout) karyawan yang dapat meningkatkan risiko resign.
2. **Perbaiki Work Life Balance:** Meningkatkan keseimbangan antara pekerjaan dan kehidupan pribadi agar karyawan lebih nyaman dan bertahan lebih lama di perusahaan.
3. **Fokus Retensi di Karyawan Baru:** Memberikan perhatian lebih pada karyawan dengan masa kerja awal melalui onboarding dan pendampingan agar tidak mudah keluar di masa adaptasi.
4. **Perjelas Jalur Karier dan Promosi:** Menyediakan sistem karier yang jelas dan transparan agar karyawan memiliki motivasi untuk berkembang dan tidak merasa stagnan.
