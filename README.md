# 📊 Analisis Penjualan Superstore: Perbandingan Penjualan Regional

> **Data-Driven Regional Sales Analysis menggunakan Python & Business Intelligence**

## 📌 Project Overview

Project ini bertujuan untuk menganalisis **kinerja penjualan Superstore berdasarkan wilayah (regional)** untuk memahami distribusi penjualan, performa produk, karakteristik pelanggan, serta hubungan antara **Sales dan Profit** di setiap wilayah.

Dengan menggunakan dataset Superstore, analisis dilakukan untuk mengidentifikasi **region dengan kontribusi terbesar, kategori produk yang paling diminati, state dengan performa tertinggi, serta segmen pelanggan yang paling berkontribusi terhadap penjualan**.

Hasil analisis kemudian divisualisasikan menggunakan **Tableau** untuk menghasilkan insight yang dapat mendukung pengambilan keputusan bisnis secara data-driven.

---

## 🎯 Problem Statement

Perusahaan perlu memahami bagaimana performa penjualan tersebar di berbagai wilayah untuk menentukan strategi pertumbuhan yang lebih efektif.

Perbedaan karakteristik pelanggan, produk, dan tingkat profitabilitas antar wilayah dapat menyebabkan strategi yang berhasil di satu region belum tentu memberikan hasil yang sama di region lainnya.

Oleh karena itu, analisis ini dilakukan untuk membantu perusahaan:

1. Mengidentifikasi wilayah dengan performa penjualan tertinggi dan terendah.
2. Mengevaluasi kategori dan sub-category produk di setiap wilayah.
3. Memahami segmen pelanggan yang memberikan kontribusi terbesar.
4. Membandingkan performa **Sales dan Profit** antar region.
5. Menentukan area yang membutuhkan strategi pemasaran dan penjualan tambahan.
6. Mengidentifikasi strategi dari region berkinerja tinggi yang dapat dijadikan benchmark.

---

## ❓ Business Questions

Analisis ini berfokus pada beberapa pertanyaan bisnis utama:

1. **Region mana yang memberikan kontribusi penjualan terbesar?**
2. **State mana yang menjadi penggerak utama penjualan pada setiap region?**
3. **Kategori produk apa yang paling diminati di masing-masing region?**
4. **Sub-category apa yang memberikan kontribusi penjualan terbesar?**
5. **Segmen pelanggan mana yang memberikan kontribusi terbesar terhadap penjualan?**
6. **Apakah tingginya Sales selalu diikuti oleh Profit yang tinggi?**
7. **Region mana yang memiliki peluang untuk ditingkatkan?**

---

## 📊 Dataset

Dataset yang digunakan adalah **Superstore Dataset** yang bersumber dari Kaggle dengan:

| Dataset Information | Detail |
|---|---:|
| Total Rows | **9,994** |
| Total Columns | **21** |
| Data Type | Transactional Sales Data |
| Source | Kaggle – Superstore Dataset |

### 🔑 Key Variables

| Variable | Description |
|---|---|
| `Region` | Wilayah geografis pelanggan |
| `State` | Negara bagian tempat transaksi |
| `City` | Kota pelanggan |
| `Category` | Kategori utama produk |
| `Sub-Category` | Sub-kategori produk |
| `Segment` | Segmen pelanggan |
| `Sales` | Nilai penjualan |
| `Profit` | Keuntungan dari transaksi |
| `Order Date` | Tanggal pemesanan |
| `Ship Date` | Tanggal pengiriman |

---

## 🧹 Data Preparation

Sebelum dilakukan analisis, beberapa tahap data preparation dilakukan untuk memastikan data dapat digunakan dengan baik.

### Proses yang dilakukan:

1. Mengecek missing values.
2. Mengecek data duplikat.
3. Mengubah tipe data tanggal dari string menjadi `datetime`.
4. Memastikan tipe data numerik sesuai untuk kebutuhan analisis.
5. Melakukan pengecekan kualitas data.
6. Menyiapkan dataset untuk kebutuhan visualisasi dan dashboard.

### Data Quality

Hasil pengecekan menunjukkan bahwa:

- ✅ Tidak ditemukan missing values.
- ✅ Tidak ditemukan data duplikat.
- ✅ Data transaksi dapat digunakan untuk analisis setelah penyesuaian tipe data.
- ✅ Ditemukan outlier namun tidak dilakukan penanganan dikeranakan kondisi yang wajar dan valid

---

# 🔍 Key Insights

## 1.Penjualan Berdasarkan Region

Total penjualan Superstore mencapai:

> ###  **$2,297,200.86**
> **Profit Margin: 12.47%**

| Region | Sales |
|---|---:|
|  **West** | **$725,457.82** |
|  **East** | **$678,781.24** |
| Central | $501,239.89 |
| South | $391,721.90 |

**West** menjadi region dengan kontribusi penjualan terbesar, diikuti oleh **East**.

Kedua region tersebut dapat dianggap sebagai **tulang punggung penjualan perusahaan**, sehingga perlu dipertahankan sekaligus dikembangkan untuk mendukung pertumbuhan bisnis.

---

## 2.State sebagai Penggerak Regional

Performa regional sangat dipengaruhi oleh beberapa state utama.

### West
Penjualan terutama didorong oleh:

-  **California**
-  **Washington**

### East
Penjualan terutama didorong oleh:

-  **New York**
-  **Pennsylvania**

Hal ini menunjukkan bahwa analisis regional sebaiknya tidak berhenti pada level **Region**, tetapi juga perlu melihat kontribusi **State** untuk menemukan lokasi yang menjadi driver utama penjualan.

---

## 3.Penjualan Berdasarkan Category

**Technology** menjadi kategori dengan penjualan terbesar dan memiliki kontribusi kuat terutama dari **East dan West**.

Sementara itu:

-  **Technology** → kategori dengan kontribusi penjualan terbesar.
-  **Furniture** → menunjukkan performa yang kuat di West.
-  **Office Supplies** → memberikan kontribusi besar terutama di West dan East.

Temuan ini menunjukkan bahwa **preferensi produk dapat berbeda antar wilayah**, sehingga strategi inventory dan pemasaran sebaiknya mempertimbangkan karakteristik regional.

---

## 4.Segmentasi Pelanggan

Segmen **Consumer** memberikan kontribusi penjualan terbesar dibandingkan segmen lainnya.

Tiga kombinasi **Sub-Category × Segment** dengan penjualan tertinggi berasal dari Consumer:

| Segment | Sub-Category | Sales |
|---|---|---:|
| Consumer | Chairs | **$172,862.74** |
| Consumer | Phones | **$169,932.76** |
| Consumer | Storage | **$100,492.40** |

Hal ini menunjukkan bahwa **Consumer merupakan customer segment yang sangat penting** untuk dipertahankan dan dikembangkan.

---

# ⚠️ Additional Insight: Sales ≠ Profit

Salah satu temuan penting dari analisis adalah bahwa **tingginya Sales tidak selalu menghasilkan Profit yang lebih tinggi**.

### Central vs South

| Region | Sales | Profit |
|---|---:|---:|
| Central | **$501,239.89** | $39,706.36 |
| South | $391,721.90 | **$46,749.43** |

Meskipun **Central memiliki Sales yang lebih tinggi daripada South**, Profit yang dihasilkan justru lebih rendah.

Hal ini mengindikasikan adanya potensi masalah pada **profitability**, yang dapat berkaitan dengan:

- Strategi discount yang terlalu agresif.
- Cost atau operational expenses.
- Product mix.
- Harga jual dan margin produk.

> 💡 **Business takeaway:** Sales volume yang tinggi tidak selalu berarti performa bisnis yang lebih sehat. Oleh karena itu, evaluasi harus mempertimbangkan **Sales sekaligus Profit**.

---

# Conclusion

Analisis menunjukkan bahwa **West dan East merupakan kontributor utama penjualan Superstore**, dengan California, Washington, New York, dan Pennsylvania menjadi beberapa state penting yang mendorong performa regional.

Dari sisi produk, **Technology** menjadi kategori dengan kontribusi penjualan terbesar, sementara **Consumer** merupakan segmen pelanggan yang paling berkontribusi.

Namun, analisis juga menunjukkan bahwa **Sales yang tinggi tidak selalu menghasilkan Profit yang tinggi**, seperti yang terlihat pada perbandingan Central dan South.

Oleh karena itu, strategi bisnis tidak hanya perlu berfokus pada **peningkatan Sales**, tetapi juga pada **profitability, product mix, customer segmentation, pricing, dan regional strategy**.

> **Key Takeaway:**  
>  *"The goal is not only to sell more, but to understand where, what, and to whom we sell — and whether those sales generate sustainable profit."*

---

# 💡 Business Recommendations

## 1. Prioritaskan West & East

West dan East dapat menjadi prioritas utama karena memberikan kontribusi penjualan terbesar.

Strategi yang dapat dilakukan:

- Mempertahankan ketersediaan produk dengan demand tinggi.
- Mengoptimalkan aktivitas marketing.
- Meningkatkan customer retention.
- Mengembangkan produk Technology dan Furniture sesuai kebutuhan regional.

---

## 2. Optimalkan Product Strategy

Perusahaan dapat menyesuaikan **product assortment** berdasarkan karakteristik masing-masing region.

Sebagai contoh:

- Technology dapat diprioritaskan pada region dengan demand tinggi.
- Furniture dapat dikembangkan lebih lanjut di West.
- Produk dengan performa rendah di region tertentu perlu dievaluasi kembali.

Untuk kategori dengan performa rendah, perusahaan dapat menguji:

**Pricing → Promotion → Product Mix → Inventory Strategy**

---

## 3. Evaluasi Discount & Profitability

Central membutuhkan perhatian khusus karena memiliki **Sales tinggi tetapi Profit relatif rendah** dibandingkan South.

Perusahaan dapat melakukan:

- Audit terhadap discount.
- Analisis profit margin berdasarkan kategori dan sub-category.
- Evaluasi produk dengan margin rendah.
- Membandingkan profitability antar state.
- Menentukan batas discount yang tetap menjaga margin.

---

## 4. Fokus pada Consumer Segment

Consumer merupakan segmen dengan kontribusi penjualan terbesar.

Strategi yang dapat diterapkan:

- Customer loyalty program.
- Personalized promotion.
- Cross-selling produk terkait.
- Bundling produk seperti **Phones, Chairs, dan Storage**.
- Customer segmentation berdasarkan purchase behavior.

---

## 5. Regional Benchmarking

Perusahaan dapat menggunakan region dan state dengan performa tinggi sebagai **benchmark**.

Contohnya:

> **California → identifikasi faktor keberhasilan → evaluasi kesesuaian dengan region lain → adaptasi strategi.**

Namun, strategi tidak harus diterapkan secara identik. Perusahaan perlu menyesuaikannya dengan **karakteristik pelanggan, produk, dan market masing-masing region**.

---

# 📈 Analytical Storytelling

Alur analisis project ini dibangun dari level **makro → mikro → business action**:

```text
Overall Sales Performance
          ↓
Regional Comparison
          ↓
State Performance
          ↓
Category & Sub-Category
          ↓
Customer Segment
          ↓
Sales vs Profit
          ↓
Business Insight
          ↓
Strategic Recommendation
```

Dengan alur tersebut, analisis tidak hanya menunjukkan **"berapa besar penjualan"**, tetapi juga menjawab:

> **Di mana penjualan terjadi → Apa yang dijual → Siapa yang membeli → Apakah penjualan tersebut profitable → Apa yang harus dilakukan perusahaan?**

---

# 🛠️ Tools & Technologies

###  Data Analysis
- **Python**
- **Pandas**
- **Jupyter Notebook**

###  Business Intelligence
- **Tableau**

###  Data Preparation
- Data Cleaning
- Data Transformation
- Exploratory Data Analysis (EDA)
- Data Visualization

---

# 📊 Dashboard & Presentation

Hasil analisis divisualisasikan menggunakan **Tableau / Power BI** dalam bentuk dashboard interaktif yang mencakup:

- Regional Sales Comparison
- Sales by State
- Sales by Category
- Sales by Sub-Category
- Customer Segment Analysis
- Sales & Profit Comparison

---

# 📁 Project Structure

```text
Superstore-Regional-Sales-Analysis/
│
├── 📂 dataset/
│   └── superstore.csv
│
├── 📂 notebook/
│   └── superstore_analysis.ipynb
│
├── 📂 dashboard/
│   └── superstore_dashboard.twbx
│
├── 📂 presentation/
│   └── superstore_regional_sales.pdf
│
└── README.md
```

---


##  Project Author

**Muhammad Alfi Syahputra**

📌 Data Analyst Portfolio Project  
📊 Python | Pandas | Tableau | Excel

---

⭐ **If you find this project useful, feel free to give this repository a star!**
