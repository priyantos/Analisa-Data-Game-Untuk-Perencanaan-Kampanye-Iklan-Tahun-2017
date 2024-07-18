# Analisa-Data-Game-Untuk-Perencanaan-Kampanye-Iklan-Tahun-2017
**Pendahuluan <a id='intro'></a>**

Sebagai Karyawan Data Analyst di Toko Online "ICE" yang menjual video game dari seluruh dunia. Data terkait ulasan pengguna dan ahli game, genre, platform (misalnya, Xbox atau PlayStation), dan data historis penjualan game tersedia dari open source. Disini kita perlu mengidentifikasi pola-pola yang menentukan apakah suatu game bisa dikatakan berhasil atau tidak. Dengan begitu, kita bisa menemukan game yang paling potensial dan merencanakan kampanye iklannya.
Saat ini kita punya data dari tahun 2016, dataset ini memuat singkatan ESRB. ESRB merupakan singkatan dari Entertainment Software Rating Board, yaitu sebuah organisasi regulator mandiri yang mengevaluasi konten game dan memberikan rating usia seperti Remaja atau Dewasa.

**Tujuan:**

* Mengidentifikasi pola-pola yang menentukan keberhasilan suatu game dan merencanakan kampanye iklan berdasarkan data ulasan pengguna, ahli game, genre, platform, data penjualan historis, dan rating usia ESRB pada game yang tersedia. 

* Menganalisis Tren Penjualan: Tujuan utama proyek ini adalah untuk menganalisis tren penjualan video game di berbagai wilayah, termasuk Amerika Utara, Eropa, dan Jepang. Kami akan mencoba memahami bagaimana preferensi pasar berbeda-beda di seluruh dunia.

* Menentukan Faktor Kesuksesan Game: Kami akan mencoba mengidentifikasi faktor-faktor yang berkontribusi terhadap kesuksesan suatu game, baik dari segi penjualan maupun ulasan. Ini termasuk memeriksa hubungan antara skor ulasan kritikus, skor ulasan pengguna, genre, platform, dan rating ESRB dengan penjualan game.

* Merencanakan Kampanye Iklan: Melalui pemahaman yang kami peroleh dari analisis data, kami akan merencanakan kampanye iklan yang lebih efektif untuk game-game yang memiliki potensi tinggi. Hal ini akan membantu toko online "Ice" dalam meningkatkan penjualan dan memaksimalkan keuntungan.

Berikut rincian yang akan kita lewati:

*Tahapan yang Dilakukan**

**Langkah 1: Insialisasi**

- Memanggil data library yang dibutuhkan

**Langkah 2: Memuat Dataset**

- Melakukan analisis dataset pada file path berikut:
   - `/datasets/games.csv`.
   
**Langkah 3: Mempersiapkan Data**

* Ganti nama kolom (pakai huruf kecil semua).
* Konversikan data ke tipe data yang dibutuhkan.
* Deskripsikan kolom-kolom mana saja yang tipe datanya kamu ubah dan jelaskan alasannya.
* Jika diperlukan, tentukan bagaimana kamu akan menangani nilai yang hilang:
    - Jelaskan alasan kenapa kamu mengisi nilai yang hilang seperti itu atau alasan kenapa kamu membiarkannya tetap kosong.
    - Kalau menurut kamu, kenapa nilai-nilai tersebut hilang? Berikan kemungkinan alasannya, ya.
    - Perhatikan singkatan TBD (to be determined atau dalam bahasa Indonesia, "akan ditentukan"). Tentukan bagaimana kamu akan mengatasi kasus-kasus seperti itu.
* Hitung total penjualan (jumlah penjualan di semua wilayah) untuk tiap game dan masukkan nilai-nilai ini ke dalam kolom terpisah.

**Langkah 4: Menganalisa Data**

* Lihat berapa banyak game yang dirilis pada tahun yang berbeda. Apakah data di setiap periode signifikan?
* Lihat bagaimana penjualan bervariasi dari satu platform ke platform lainnya. Pilih platform dengan total penjualan terbesar dan buat distribusinya berdasarkan data per tahun. Cari platform yang dahulu populer, tetapi sekarang tidak memiliki penjualan apa pun. Berapa lama biasanya waktu yang dibutuhkan platform baru untuk muncul dan platform lama untuk memudar popularitasnya?
* Tentukan periode waktu pengambilan data. Untuk melakukannya, lihat jawabanmu di pertanyaan sebelumnya. Data yang kamu ambil seharusnya memungkinkan kamu untuk membangun model bagi tahun 2017.
* Kerjakan saja data yang menurutmu relevan. Abaikan data untuk tahun-tahun sebelumnya.
* Platform mana saja yang memiliki penjualan terbanyak? Platform mana saja yang tumbuh atau menyusut? Pilih beberapa platform yang berpotensi menghasilkan keuntungan.
* Buat sebuah boxplot untuk penjualan global semua game yang dikelompokkan berdasarkan platform. Apakah perbedaan penjualannya signifikan? Bagaimana dengan penjualan rata-rata pada berbagai platform? Deskripsikan penemuanmu.
* Lihat bagaimana ulasan pengguna dan para profesional memengaruhi penjualan pada salah satu platform populer (yang kamu pilih). Buat sebuah scatter plot dan hitung korelasi antara ulasan dan penjualan. Kemudian, tarik kesimpulannya.
* Dengan mengingat kesimpulanmu, bandingkan penjualan game yang sama di platform lain.
* Amati distribusi umum game berdasarkan genre. Apa yang bisa kita simpulkan terkait genre yang paling menguntungkan? Bisakah kamu melakukan generalisasi terkait genre dengan penjualan yang tinggi dan rendah?

**Langkah 5: Lakukan Pemrofilan Pengguna Untuk Masing-masing Wilayah**

Untuk setiap wilayah (NA, EU, JP), tentukan :
* 5 platform teratas. Jelaskan variasi pangsa pasar dari satu wilayah ke wilayah lainnya.
* 5 genre teratas. Jelaskan perbedaannya.
* Apakah rating ESRB memengaruhi penjualan di masing-masing wilayah?

**Langkah 6: Uji Hipotesis-hipotesis Berikut:** 

* Rata-rata rating pengguna platform Xbox One dan PC adalah sama.
* Rata-rata rating pengguna genre Action dan Sports berbeda.

Tentukan nilai ambang batas alpha.

Jelaskan:
* Bagaimana kamu merumuskan hipotesis nol dan hipotesis alternatif
* Berapa tingkat signifikansi yang kamu pilih untuk menguji hipotesis dan jelaskan alasanmu memilih angka tersebut

**Langkah 7: Tuliskan Kesimpulan Umumnya**

**Deskripsi Data**

**Tabel `Games`:**
- Name — (nama)
- Platform
- Year_of_Release — (tahun rilis) 
- Genre
- NA_sales — (penjualan di Amerika Utara dalam satuan juta USD)
- EU_sales — (penjualan di Eropa dalam satuan juta USD)
- JP_sales — (penjualan di Jepang dalam satuan juta USD)
- Other_sales — (penjualan di negara lainnya dalam satuan juta USD)
- Critic_Score — (skor ulasan dari kritikus, maksimal 100)
- User_Score — (skor ulasan dari pengguna, maksimal 10)
- Rating — (ESRB)
