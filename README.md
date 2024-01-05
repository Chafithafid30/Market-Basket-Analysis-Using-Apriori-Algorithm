# Data Mining: Market Basket Analysis with Apriori Algorithm
Analisis Keranjang Belanja (Market Basket Analysis atau MBA) adalah teknik data mining yang bertujuan untuk menemukan hubungan dan pola dalam satu set item yang sering dibeli bersama. Analisis ini sangat berguna dalam pengaturan ritel dan e-commerce untuk memahami perilaku pembelian pelanggan, meningkatkan strategi penjualan lintas, dan mengoptimalkan penempatan produk. Algoritma Apriori adalah algoritma yang banyak digunakan untuk melakukan analisis keranjang belanja.

## Penjelasan Detail:
### Market Basket Analysis
Market basket analysis adalah suatu metodologi untuk melakukan analisis buying habit konsumen dengan menemukan asosiasi antar beberapa item yang berbeda, yang diletakkan konsumen dalam shopping basket (keranjang belanja) yang dibeli pada suatu transaksi tertentu. Tujuan dari market basket analysis adalah untuk mengetahui produk-produk mana yang mungkin akan dibeli secara bersamaan

### Algoritma Apriori
Algoritma Apriori adalah suatu algoritma dasar yang diusulkan oleh Agrawal & Srikant pada tahun 1994 untuk penentuan frequent itemsets untuk aturan asosiasi boolean. Algoritma Apriori memberi kita sifat asosiatif dalam transaksi. Ini juga dikenal sebagai Aturan Asosiasi. Aturan asosiasi atau association rule adalah teknik untuk menemukan aturan asosiasi antara suatu kombinasi item. 


## Penjelasan langkah demi langkah tentang bagaimana algoritma Apriori bekerja dalam konteks Analisis Keranjang Belanja:
### 1. Data Transaksi:
• Mulailah dengan dataset yang berisi informasi transaksional, di mana setiap baris mewakili transaksi unik, dan kolom mewakili item yang dibeli.

### 2. Generasi Itemset:
• Identifikasi semua item individual dan hitung frekuensi mereka dalam dataset. Ini disebut sebagai 1-itemset.

### 3. Perhitungan Dukungan:
• Tetapkan ambang dukungan minimum. Dukungan adalah proporsi transaksi yang mengandung satu itemset tertentu. Dihitung sebagai jumlah transaksi yang mengandung itemset dibagi dengan total jumlah transaksi.
• Hapus itemset yang tidak memenuhi ambang dukungan minimum.

### 4. Generasi Kandidat:
• Gunakan itemset yang sering muncul dari langkah sebelumnya untuk menghasilkan itemset kandidat untuk level berikutnya. Misalnya, jika {A, B} dan {C, D} adalah 2-itemset yang sering muncul, maka itemset kandidat 3-itemset mungkin {A, B, C}.
• Potong itemset kandidat dengan memastikan bahwa semua subset mereka sering muncul. Langkah ini membantu mengurangi jumlah itemset kandidat dan meningkatkan efisiensi.

### 5. Perhitungan Dukungan untuk Itemset Kandidat:
• Hitung dukungan untuk setiap itemset kandidat dan hilangkan yang di bawah ambang dukungan minimum.

### 6. Ulangi Langkah 4-5:
• Ulangi proses generasi itemset kandidat, pemotongan, dan perhitungan dukungan sampai tidak ada lagi itemset yang sering muncul yang dapat dihasilkan.

### 7. Generasi Aturan Asosiasi:
• Gunakan itemset yang sering muncul untuk menghasilkan aturan asosiasi. Aturan asosiasi memiliki bentuk "Jika A, maka B," di mana A dan B adalah itemset.
• Hitung metrik seperti confidence dan lift untuk setiap aturan. Confidence mengukur kemungkinan bahwa jika A terjadi, maka B juga akan terjadi. Lift mengukur seberapa lebih mungkin B terjadi ketika A terjadi dibandingkan ketika B terjadi secara independen dari A.

### 8. Pemotongan Aturan:
• Terapkan filter atau ambang tambahan (misalnya, confidence minimum) untuk memilih hanya aturan yang paling menarik dan bermakna.

### 9. Interpretasi Hasil:
• Analisis dan interpretasikan aturan asosiasi yang dihasilkan untuk mendapatkan wawasan tentang perilaku pelanggan, hubungan produk, dan peluang penjualan lintas potensial.

## Kesimpulan:
Secara keseluruhan, algoritma Apriori membantu menemukan itemset yang sering muncul dan aturan asosiasi dari data transaksional, memberikan wawasan berharga bagi bisnis untuk mengoptimalkan strategi mereka. Penyesuaian ambang dukungan dan confidence memungkinkan keseimbangan antara menemukan pola yang bermakna dan menghindari asosiasi yang keliru.

Berdasarkan analisis dengan nilai min_support sebesar 0.01, adapun hasil beberapa aturan asosiasi yang menunjukkan item yang sering dibeli bersamaan antara lain:

1. Coffee dan Bread.
2. Medialuna dan Coffee.
3. Pastry dan Coffee.
4. Tea dan Coffee.

Aturan-aturan ini menunjukkan bahwa kombinasi produk-produk tersebut memiliki tingkat kejadian yang tinggi, dan pelanggan cenderung membeli item tersebut bersamaan. Ini dapat memberikan wawasan berharga untuk strategi pemasaran, penempatan produk di toko, atau penawaran bundel yang dapat meningkatkan penjualan dan kepuasan pelanggan. Karena Algoritma Apriori membantu mengidentifikasi aturan asosiasi yang dapat memberikan wawasan tentang kecenderungan pelanggan membeli produk bersamaan.
