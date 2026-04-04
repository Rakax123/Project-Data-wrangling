1. Ide Project:
    a. Judul project:
   
    Data Wrangling Untuk Analisis Perilaku Konsumen Brazil Terhadap Produk Yang Diperjualbelikan Di Perbelanjaan Daring Olist
   
    b. Latar belakang, manfaat, dan tujuan beserta referensinya:
    Mengetahui mengapa pelanggan membeli untuk mendapatkan wawasan (insight) mendalam tentang pelanggan guna mengambil keputusan bisnis yang lebih tepat sasaran dan efektif.
   
   Industri E-Commerce di Brazil memiliki tantangan unik mengingat luas wilayah geografis yang besar dan ketimpangan ekonomi antar negara bagian. Olist, sebagai salah satu platform e-commerce terbesar, menghubungkan penjual kecil dengan pembeli di seluruh negeri. Namun, kepuasan pelanggan seringkali dipengaruhi oleh faktor eksternal di luar kendali produk itu sendiri, seperti infrastruktur logistik dan daya beli ekonomi daerah.
    Proyek ini dilatarbelakangi oleh kebutuhan untuk memahami bagaimana variabel makro (seperti GDP daerah) dan kinerja logistik (durasi pengiriman) berinteraksi dalam membentuk persepsi dan kepuasan pelanggan. Data mentah yang tersebar di berbagai sumber (transaksi internal, data pemerintah, dan kalender nasional) memerlukan proses Data Wrangling yang komprehensif sebelum dapat dianalisis.

    C Sumber data yang digunakan berasal dari 3 sumber:
-    Data Internal: Brazilian E-Commerce Public Dataset by Olist (Sumber: Kaggle) Ini adalah data utama yang memuat seluruh aktivitas transaksi dan umpan balik pelanggan. order_id: ID unik untuk setiap transaksi. Ini adalah "kunci utama" untuk menghubungkan detail barang dan ulasan. customer_state: Lokasi negara bagian pembeli (contoh: SP, RJ, MG). Digunakan untuk analisis geografis dan penghubung ke data GDP. order_purchase_timestamp: Waktu pembelian. Digunakan untuk melihat tren penjualan (harian/bulanan) dan menghubungkan ke data Hari Libur. price & freight_value: Harga barang dan ongkos kirim. Digunakan untuk analisis nilai transaksi (Monetary) dan korelasi dengan jarak/ekonomi. review_score: Rating bintang (1-5). Variabel krusial untuk mengukur kepuasan pelanggan (Customer Satisfaction).
-  Data Eksternal 1: Regional Account of Brazil (GDP by State)
(Sumber: IBGE - Pemerintah Brazil) Ini adalah data makro-ekonomi untuk memberikan konteks pada lokasi pelanggan.
State (UF): Kode negara bagian (contoh: SP, RJ). Kolom ini di-join dengan customer_state dari dataset Olist.
GDP (PIB): Nilai Produk Domestik Bruto daerah tersebut.
Kuartil_GDP: (Fitur hasil olahan) Pengelompokan provinsi menjadi kategori "High GDP", "Medium GDP", dan "Low GDP" untuk melihat perbedaan daya beli antar wilayah.
-  Data Eksternal 2: Python Holidays Library (Brazil)
(Sumber: Python Library) Ini adalah data kalender untuk menganalisis faktor musiman (Seasonality).
Date: Tanggal merah. Kolom ini di-join dengan tanggal pada order_purchase_timestamp.
holiday_name: Nama hari libur (contoh: Christmas, Independence Day, Carnival).
is_holiday: (Fitur hasil olahan) Penanda biner (1 = Libur, 0 = Hari Biasa) untuk membandingkan apakah orang berbelanja lebih boros/hemat saat tanggal merah.

2. Proses Wrangling
    a. Teknik pengambilan dan integrasi data
    b. Data cleaning
    c. Data eksplorasi
    d. Data publishing (raw data, hasil proses wrangling, dan dokumentasi pipeline)
