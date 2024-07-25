# Overview

- Sebuah perusahaan di Indonesia ingin mengetahui efektifitas sebuah iklan yang mereka tayangkan, hal ini penting bagi perusahaan agar dapat mengetahui seberapa besar ketercapainnya iklan yang dipasarkan sehingga dapat menarik customers untuk melihat iklan.
- Dengan mengolah data historical advertisement serta menemukan insight serta pola yang terjadi, maka dapat membantu perusahaan dalam menentukan target marketing, fokus case ini adalah membuat model machine learning classification yang berfungsi menentukan target customers yang tepat.

## 1. Univariate Analysis

![img 1](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/univ.JPG)

**Interpretasi Univariate Analysis.**
- User yang lebih tua dan memiliki pendapatan area yang lebih rendah cenderung lebih sering mengklik iklan.
- User yang lebih muda dan memiliki pendapatan area yang lebih tinggi cenderung tidak mengklik iklan.
- User yang mengklik iklan menghabiskan lebih sedikit waktu di internet dan di situs tersebut dibandingkan dengan mereka yang tidak mengklik iklan.


## 2. Bivariate Analysis

![img 2](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/biv.JPG)

**Interpretasi Bivariate Analysis.**
- Pengguna yang mengklik iklan cenderung memiliki penggunaan internet harian yang lebih rendah. Ini menunjukkan bahwa meskipun mereka tidak menghabiskan banyak waktu di internet, mereka lebih responsif terhadap iklan.
- Hari-hari tertentu seperti awal bulan (1 & 3) menunjukkan peningkatan klik, namun pada tanggal akhir bulan cenderung menurun.
- Pengguna lebih aktif mengklik iklan pada waktu-waktu tertentu dalam sehari, misalnya saat mereka baru bangun (jam 9) atau saat mereka bersantai di rumah (jam 18 dan jam 00) dan sedikit mengklik iklan di jam-jam produktif.

## 3. Multivariate Analysis

![img 3](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/multi.JPG)

**Interpretasi:**
- Pengguna yang Lebih Muda cenderung menghabiskan lebih banyak waktu di internet dan di situs Serta cenderung berasal dari daerah dengan pendapatan yang lebih tinggi.
- Pengguna yang Lebih Tua cenderung menghabiskan lebih sedikit waktu di internet dan di situs Serta cenderung berasal dari daerah dengan pendapatan yang lebih rendah.
- Pengguna dengan penggunaan internet harian yang lebih tinggi cenderung menghabiskan lebih banyak waktu di situs dan berasal dari daerah dengan pendapatan yang lebih tinggi.
- Pengguna yang menghabiskan lebih banyak waktu di situs cenderung menghabiskan lebih banyak waktu di internet dan berasal dari daerah dengan pendapatan yang lebih tinggi.

# Data Modeling 

![img 4](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/model%20ML.JPG)

![img 5](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/cm.JPG)

![img 6](https://github.com/M-Fatoni/Predict-Clicked-Ads-Customer-Classification-by-using-Machine-Learning/blob/main/img/feat_imp.JPG)

**Interpretasi Model:**
- Logistic Regression menjadi model dengan performa terbaik, diikuti oleh Random Forest dan SVM. Logistic Regression menunjukkan peningkatan signifikan dan Random Forest menunjukkan konsistensi kinerja yang tinggi baik tanpa normalisasi maupun setelah normalisasi.
- Model juga menunjukkan performa yang sangat baik dengan hanya satu FN dan sedikit FP. Model ini lebih seimbang dalam mengidentifikasi kelas positif dan negatif.
- Konsistensi Fitur Utama: Fitur seperti Daily Time Spent on Site, Daily Internet Usage, Area Income, dan Age muncul sebagai fitur penting di kedua model, menandakan bahwa faktor-faktor ini sangat relevan dalam memprediksi klik iklan.
- Pengaruh Kategori: Kategori tertentu seperti Finance muncul di kedua model, menunjukkan bahwa minat atau keterlibatan dalam bidang keuangan adalah indikator penting.
- Geografi dan Demografi: Faktor geografis seperti Island dan demografi seperti Gender dan Area Income memiliki peran signifikan, menunjukkan bahwa perilaku pengguna dapat berbeda berdasarkan lokasi dan karakteristik demografis.
- Pengaruh Waktu: Hari dan jam juga penting dalam model Random Forest, yang mungkin menunjukkan bahwa perilaku pengguna bisa berbeda tergantung pada waktu mereka mengakses internet.

# Business Recommendation & Simulation

### **Rekomendasi Bisnis:**

**1. Target Audience Optimization:**

**Pengguna yang Lebih Tua dan Pendapatan Area Lebih Rendah.**
- Strategi: Fokuskan iklan pada pengguna yang lebih tua dan dari daerah dengan pendapatan lebih rendah. Buat iklan yang relevan dengan kebutuhan dan minat mereka, seperti produk kesehatan, penawaran diskon, dan layanan yang sesuai dengan anggaran mereka.
- Platform dan Konten: Gunakan platform yang lebih sering diakses oleh kelompok usia ini, seperti Facebook atau email. Buat konten yang informatif dan mudah dimengerti.

**Pengguna yang Lebih Muda dan Pendapatan Area Lebih Tinggi.**
- Strategi: Untuk pengguna yang lebih muda dengan pendapatan area lebih tinggi, buat iklan yang menarik secara visual dan interaktif. Fokuskan pada produk premium dan teknologi terbaru.
- Platform dan Konten: Gunakan platform seperti Instagram, TikTok, dan YouTube untuk mencapai kelompok ini dengan konten dinamis dan interaktif, seperti video dan live streams.


**2. Timing and Frequency of Ads:**

**Waktu dan Hari yang Tepat.**
- Strategi: Jadwalkan iklan untuk tampil pada jam-jam dan hari-hari yang lebih banyak direspon oleh pengguna, seperti jam 9 pagi, jam 6 sore, dan tengah malam, serta di awal bulan.
- Optimasi: Tingkatkan frekuensi iklan pada waktu-waktu tersebut dan kurangi pada jam-jam produktif di mana klik iklan lebih sedikit.

**3. Content and Message Customization:**

**Daily Time Spent on Site and Daily Internet Usage**
- Strategi: Sesuaikan konten iklan dengan pola penggunaan internet. Untuk pengguna dengan penggunaan internet harian rendah, buat iklan yang langsung ke intinya dan menarik perhatian cepat. Untuk pengguna dengan penggunaan tinggi, buat iklan yang lebih informatif dan mendalam.
- Konten: Gunakan teknik storytelling untuk pengguna yang menghabiskan lebih banyak waktu di internet dan pastikan iklan singkat dan to-the-point untuk yang menghabiskan waktu lebih sedikit.

**4. Geographical and Demographic Segmentation:**

**Faktor Geografis dan Demografis.**
- Strategi: Sesuaikan iklan berdasarkan lokasi geografis dan demografi. Misalnya, buat kampanye iklan khusus untuk pengguna di pulau Jawa dan Kalimantan dengan konten yang relevan secara lokal.
- Personalization: Gunakan data demografis seperti gender dan income area untuk membuat iklan yang lebih personal dan relevan.

**5. Category-Specific Advertising:**

**Kategori Khusus**
- Strategi: Fokus pada kategori yang menunjukkan pengaruh besar seperti Finance, Furniture, House, Travel, dan Otomotif. Buat iklan yang menarik bagi pengguna yang tertarik dengan kategori ini.
- Konten: Buat kampanye yang menonjolkan fitur produk keuangan, perabotan, properti, perjalanan, dan otomotif, dengan penawaran dan promosi yang menarik.

### Simulasi Marketing

**Data Diketahui:**
- Jumlah User: 963
- Persentase yang Mengklik (berdasarkan data): 51%
- Persentase yang Tidak Mengklik (berdasarkan data): 49%
- Akurasi Model: 96%

**Asumsi:**
- Biaya Pemasaran per User: 2 dollar.
- Revenue_per_Conversion: 100 dollar.

**Conversion Rate:** 
- Skenario Tradisional: 51% pengguna mengklik. 
- Skenario Teroptimasi: Menggunakan akurasi model (96%) untuk menghitung konversi.



#### Simulasi Marketing (Skenario Tanpa Model ML):

**Total Pemasaran:** Biaya Pemasaran=963 x 2 = 1.926

**Total Conversion:**
- Conversion Rate Tradisional = 0.51
- Total Conversion = 963 x 0.51 = 491 

**Pendapatan** = 491 x 100 = 49.100

**Keuntungan** = 49.100 − 1.926 = 47.174

#### Simulasi Marketing (Skenario Dengan Model ML):

**Total Pemasaran:** Biaya Pemasaran=963 x 2 = 1.926

**Total Conversion:**
- Conversion Rate Tradisional = 0.96
- Total Conversion = 963 x 0.96 = 924,48 

**Pendapatan** = 924,48 x 100 = 92.448 

**Keuntungan** = 92.448 − 1.926 = 90.522

### Interpretasi Simulasi:
- Dengan mengadopsi strategi pemasaran yang dioptimalkan oleh machine learning, perusahaan dapat melihat peningkatan keuntungan yang substansial. Dalam simulasi ini, keuntungan meningkat dari 47.174 dollar menjadi 90.522 dollar, yang menunjukkan peningkatan hampir dua kali lipat.
- Berdasarkan hasil simulasi ini, sangat direkomendasikan untuk mengimplementasikan model machine learning dalam strategi pemasaran. Penggunaan data dan algoritma machine learning memungkinkan perusahaan untuk memaksimalkan efisiensi kampanye iklan, mengurangi biaya yang tidak perlu, dan secara signifikan meningkatkan pendapatan dan keuntungan.
