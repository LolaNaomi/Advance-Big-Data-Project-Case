# 🚖 NYC Green Taxi Data Analysis

## 📖 Deskripsi
Proyek ini menganalisis data perjalanan taksi hijau (Green Taxi) di New York City dari bulan Januari hingga Juli 2024. Analisis ini bertujuan untuk memahami pola permintaan, lokasi penjemputan dan pengantaran, serta mengidentifikasi jam-jam sibuk berdasarkan data yang tersedia. Proyek ini menggunakan data dari **TLC Trip Record Data** dan visualisasi dalam bentuk heatmap serta grafik tren.

**Apa itu Green Taxi di New York City?**
![image](https://github.com/user-attachments/assets/3b78a8ed-ee59-4e90-86bf-569e0ae0d2be)
Gambar Wilayah Pickup Passenger Green Taxi | Sumber: [Astoria Loves Those Green Taxis](https://weheartastoria.com/2014/06/astoria-loves-those-green-taxis/)

  Pada musim panas tahun 2013, Kota New York membuat program untuk mengurangi kesenjangan layanan taksi di wilayah yang jarang dikunjungi di NYC — Harlem, Queens, Bronx, dan Brooklyn (serta bagian utara Manhattan di atas East 96th Street dan West 110th Street). Program baru ini meluncurkan Green Taxi di NYC yang secara resmi dikenal sebagai Boro Taxis.
Namun, taksi hijau boleh masuk Manhattan untuk menurunkan penumpang, tetapi tidak boleh mengambil penumpang di jalan di daerah pusat Manhattan (di bawah batasan East 96th Street dan West 110th Street). Penumpang di Manhattan di luar batas ini bisa dijemput. Jadi, meskipun taksi hijau dapat melewati Manhattan atau menurunkan penumpang di sana, aturan utamanya adalah mereka tidak diperbolehkan mengambil penumpang di pusat Manhattan dari East 96th Street ke bawah.

## 📊 Dataset
- ** 🌍 Sumber Data**: TLC Trip Record Data
  (TLC : https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page | zone coordinates of NYC Yellow Taxi Trip Records: https://www.kaggle.com/datasets/yzhoukaggle/zone-coordinates-of-nyc-yellow-taxi-trip-records?select=taxi_zone_lookup_coordinates.csv)
- **Periode**: Januari – Juli 2024

## 🔄 Proses Preprocessing
![image](https://github.com/user-attachments/assets/73d6b088-803f-4d28-829b-7d2fcdf23a20)
1. **Penghapusan Kolom yang Tidak Relevan**: Menghapus kolom seperti `ehail_fee`, `store_and_fwd_flag`.
2. **Penanganan Nilai yang Tidak Valid**: Menghapus baris dengan nilai `0` atau `NaN` pada kolom tertentu seperti `passenger_count`, `trip_distance`, dan `fare_amount`.
3. **Penggabungan Data**: Melakukan merge antara dataset perjalanan dan dataset koordinat zona untuk mendapatkan informasi lokasi yang lebih lengkap.
4. **Kolom Tambahan**: Menambah kolom seperti `ID_Trip`, `RatecodeID_catg`, `payment_type_catg` dan `hour`, `minute`, `second` berdasarkan waktu penjemputan.
