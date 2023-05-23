# 📖 Analisis Dataset E-commerce dan Prediksi Customer Lifetime Value (CLV)

Nama    : Adrian

Jurusan : S1 Data sains

## E-commerce

🏪Online retail merupakan bentuk e-commerce yang fokus pada penjualan produk secara langsung kepada konsumen akhir melalui platform online. Dalam online retail, perusahaan atau individu yang menjalankan bisnis tersebut menjual produk mereka melalui situs web atau aplikasi mobile yang memungkinkan konsumen untuk memilih, membeli, dan membayar produk secara elektronik.

| Atribut | Keterangan |
| --- | --- |
| InvoiceId | ID Transaksi |
| CustomerID | ID pelanggan |
| InvoiceNo | Nomor faktur |
| InvoiceDate | Tanggal faktur |
| UnitPrice | Harga per unit |
| Quantity | Jumlah barang |
| Country | Negara |

Berdasarkan data yang diberikan kita dapat bekerja untuk melakukan beberapa analisa, analisa yang dapat dilakukan adalah sebagai berikut
1. Analisa Tren Penjualan Secara Periodik
2. Membandingkan Daya Beli Tiap Negara
3. Analisa Item Yang Paling Banyak Dibeli
4. Analisa Item Yang Banyak Dibeli Tiap Negara
5. Analisa Harga Item
6. Analisa Item Yang Paling Banyak Dilakukan Refund
7. Analisa Negara Yang Paling Sering Melakukan Refund
8. Analisa Customer Yang Paling Sering Melakukan Refund
9. Analisa Frekuensi Pembelian Customer
10. Analisa Customer Yang Mendatangkan Revenue Paling Besar
11. Analisa Customer Yang Paling Sering Melakukan Pembelian Tiap Negara
12. Analisa Customer Yang Paling Sering Melakukan Pembelian Tiap Bulan
13. Analisa Customer Yang Paling Sering Melakukan Pembelian Tiap Tahun
14. Analisa Tren Periode Item Yang Dijual

## Customer Lifetime Value (CLTV)

$$
\text{{CLTV}} = \left(\frac{{\text{{Customer Value}}}}{{\text{{churn rate}}}}\right) \times \text{{profit margin}}
$$


**CLTV** merupakan ukuran penting dalam analisis pemasaran dan CRM untuk menilai nilai pelanggan secara keseluruhan selama periode waktu yang ditentukan. CLTV mengacu pada estimasi nilai finansial yang diharapkan yang akan diberikan oleh seorang pelanggan kepada bisnis selama masa hubungan mereka.

## Model Statistik

1. Geo Beta Fitter

    **Geo Beta Fitter** adalah metode pemodelan yang digunakan untuk memodelkan frekuensi pembelian pelanggan. Metode ini didasarkan pada distribusi statistik yang disebut "geometriko-beta" atau "geometric beta distribution". Geo Beta Fitter memperkirakan parameter distribusi ini berdasarkan data frekuensi transaksi yang diamati. Dengan menggunakan model ini, dapat diestimasi kemungkinan pelanggan melakukan pembelian berulang dalam periode waktu tertentu.

2. Gamma Gamma Fitter

    **Gamma Gamma Fitter** adalah metode pemodelan yang digunakan untuk memodelkan nilai (moneter) transaksi pelanggan. Metode ini didasarkan pada distribusi statistik yang disebut "gamma-gamma" atau "gamma-gamma distribution". Gamma Gamma Fitter digunakan untuk mengestimasi parameter distribusi ini berdasarkan data nilai transaksi yang diamati. Dengan menggunakan model ini, dapat diestimasi rata-rata nilai transaksi dan variasi nilai transaksi di antara pelanggan.

## Analisis RFM

RFM adalah singkatan dari Recency, Frequency, Monetary, yang merupakan konsep analisis yang digunakan untuk mengkategorikan dan memahami perilaku pelanggan berdasarkan tiga faktor utama: recency (keterkaitan waktu), frequency (frekuensi), dan monetary (nilai transaksi).

1. Recency (Keterkaitan Waktu):

    **Recency** mengacu pada seberapa baru atau baru terakhir kali pelanggan melakukan transaksi. Informasi ini digunakan untuk mengevaluasi seberapa dekat pelanggan dengan waktu saat ini atau berapa lama sejak transaksi terakhir mereka. Semakin baru transaksi terakhir, semakin tinggi skor recency.

2. Frequency (Frekuensi):

    **Frequency** mengacu pada seberapa sering pelanggan melakukan transaksi dalam periode waktu tertentu. Informasi ini memberikan gambaran tentang seberapa sering pelanggan berinteraksi dengan bisnis atau melakukan pembelian. Semakin sering pelanggan melakukan transaksi, semakin tinggi skor frequency.

3. Monetary (Nilai Transaksi):

    **Monetary** mengacu pada nilai total transaksi yang dilakukan oleh pelanggan selama periode waktu tertentu. Informasi ini digunakan untuk menilai seberapa besar kontribusi finansial dari pelanggan terhadap bisnis. Semakin tinggi nilai transaksi, semakin tinggi skor monetary.

Dalam analisis RFM, setiap faktor (recency, frequency, monetary) diberi skor atau kategori tertentu untuk setiap pelanggan, dan kombinasi skor ini digunakan untuk mengidentifikasi segmen pelanggan yang berbeda. Analisis RFM dapat membantu dalam pemahaman perilaku pelanggan, segmentasi pelanggan, penargetan pemasaran yang lebih efektif, serta pengembangan strategi retensi dan peningkatan nilai pelanggan.

Pada RFM juga customer dibagi dalam beberapa segmen, yaitu:

1. **Hibernanting**: Segmen ini mencakup pelanggan yang belum melakukan pembelian terakhir dan memiliki frekuensi pembelian yang rendah. Mereka mungkin memerlukan upaya yang ditargetkan untuk melibatkan kembali dan mengaktifkannya kembali.

2. **At Risk**: Pelanggan di segmen ini telah melakukan pembelian baru-baru ini tetapi berisiko mengalami churn karena frekuensi yang menurun. Penting untuk mengambil tindakan proaktif untuk mempertahankan dan melibatkan mereka kembali.

3. **Can't Loose**: Pelanggan ini telah melakukan pembelian baru-baru ini dan memiliki frekuensi pembelian yang tinggi. Mereka berharga dan harus diperlakukan sebagai pelanggan setia yang menghasilkan pendapatan yang konsisten.

4. **About To Sleep**: Pelanggan di segmen ini memiliki resensi sedang tetapi frekuensi pembeliannya rendah. Mereka berisiko menjadi tidak aktif, jadi upaya harus dilakukan untuk melibatkan mereka kembali dan mencegah mereka tergelincir ke dalam segmen 'hibernasi'.

5. **Need Attention**: Pelanggan ini memiliki keterkinian sedang dan membutuhkan perhatian. Perilaku mereka menunjukkan potensi penurunan keterlibatan, dan tindakan proaktif harus diambil untuk memenuhi kebutuhan mereka dan mempertahankannya.

6. **Loyal Customer**: Segmen ini terdiri dari pelanggan setia dengan keterkinian sedang dan frekuensi pembelian tinggi. Mereka berharga dan berkontribusi secara signifikan terhadap pendapatan bisnis.

7. **Promising**: These customers have a medium recency but low frequency. They show potential and should be nurtured to increase their engagement and loyalty.

8. **New Customer**: Segmen ini mewakili pelanggan baru yang melakukan pembelian pertama mereka baru-baru ini. Mereka membutuhkan perhatian dan upaya untuk mengubah mereka menjadi pelanggan setia.

9. **Potential Loyalist**: Pelanggan di segmen ini memiliki tingkat keterkinian sedang hingga tinggi dan frekuensi pembelian sedang. Mereka menunjukkan potensi untuk menjadi pelanggan setia, dan strategi harus diterapkan untuk memelihara loyalitas mereka.

10. **champion**: Pelanggan ini telah melakukan pembelian baru-baru ini dan memiliki frekuensi pembelian yang tinggi. Mereka adalah pelanggan setia dan berharga yang berkontribusi secara signifikan terhadap kesuksesan bisnis.
## Metode CRM

**CRM** adalah singkatan dari Customer Relationship Management, yang merupakan pendekatan bisnis dan strategi untuk mengelola dan memperkuat hubungan dengan pelanggan. CRM mencakup praktik, teknologi, dan proses yang dirancang untuk memahami, melayani, dan membangun kepercayaan dengan pelanggan.

Tujuan utama dari CRM adalah untuk meningkatkan pengalaman pelanggan, membangun loyalitas pelanggan, dan meningkatkan nilai pelanggan dalam jangka panjang. Ini melibatkan pengumpulan data pelanggan, analisis perilaku pelanggan, dan penerapan strategi pemasaran yang relevan untuk memenuhi kebutuhan dan harapan pelanggan.

## Tujuan Proyek
Tujuan utama dari proyek ini adalah melakukan analisa kepada tren item, kebiasaan customer, serta melakukan prediksi terhadap **CLTV** untuk **periode 3 bulan** setelah tanggal transaksi terakhir. Melalui Prediksi **CLTV** akan diterapkan metode **CRM** agar eningkatkan pengalaman pelanggan, membangun loyalitas pelanggan, dan meningkatkan nilai pelanggan dalam jangka panjang. Ini melibatkan pengumpulan data pelanggan, analisis perilaku pelanggan, dan penerapan strategi pemasaran yang relevan untuk memenuhi kebutuhan dan harapan pelanggan. 

## Setup Proyek

Untuk menjalankan proyek ini, ikuti langkah-langkah berikut:

Pastikan Anda memiliki Python 3.x dan semua library yang diperlukan yang tercantum dalam file **requirements.txt**. Unduh dataset e-commerce yang akan digunakan dan simpan di folder proyek dengan nama file **ecommerce_dataset.csv**. Jalankan notebook Jupyter atau lingkungan pengembangan Python pilihan.