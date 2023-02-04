### Clustering

#### Pengertian 

Clustering dalam machine learning adalah teknik pembelajaran mesin yang membagi set data menjadi beberapa kelompok (cluster) berdasarkan kesamaan fitur atau atribut. Tujuannya adalah untuk menemukan struktur dan pola dalam data dengan membagi item data menjadi kelompok-kelompok (cluster) yang memiliki kesamaan atribut. Penerapan clustering bermanfaat dalanm  berbagai aplikasi seperti analisis pelanggan, sistem rekomedasi dan deteksi anomali.

Contohnya, jika kita memiliki data latih tentang pelanggan yang membeli produk-produk tertentu, clustering dapat digunakan untuk membagi pelanggan ke dalam kelompok berdasarkan preferensi belanja mereka. Setiap kelompok yang terbentuk mewakili subpopulasi pelanggan yang memiliki preferensi belanja yang serupa.

Ada beberapa algoritma clustering yang populer, seperti:

1. K-Means Clustering: K-Means adalah algoritma clustering yang paling populer. Algoritma ini membagi data menjadi k kelompok, dimana k adalah jumlah cluster yang diinginkan. Setiap cluster memiliki pusat yang disebut centroid. Data yang berdekatan dengan centroid akan dimasukkan ke dalam cluster yang sama. Algoritma ini akan mengulang iterasi sampai centroid tidak berubah lagi.
2. Hierarchical Clustering: Menggabungkan atau memisahkan cluster sampai tersisa satu cluster yang mencakup semua item data. Hierarchical clustering memiliki dua jenis, yaitu agglomerative dan divisive.
3. DBSCAN (Density-Based Spatial Clustering of Applications with Noise): Membentuk cluster bedasarkan densitas data. Data yang memiliki jumlah tetangga yang besar akan diklasifikasikan sebagai bagian cluster, sementara data yang jarang akan diidentifikasi sebagai noise.

Setiap algoritma clustering memiliki kelebihan dan kekurangan masing-masing, dan pemilihan algoritma tergantung pada karakteristik data dan tujuan pemodelan. Namun, pada dasarnya, semua algoritma clustering menggunakan suatu metrik untuk menentukan kesamaan antar item data dan menggunakan metrik tersebut untuk membagi item data ke dalam cluster.

Analoginya adalah membagi buah-buahan ke dalam beberapa keranjang berdasarkan jenisnya. Misalnya, kita memiliki keranjang buah-buahan yang berisi apel, pisang, dan anggur. Dalam hal ini, masing-masing jenis buah adalah sebuah cluster dan keranjang adalah representasi dari cluster. Proses clustering serupa dengan membagi buah-buahan ke dalam keranjang berdasarkan jenis buah, yang memiliki kesamaan atribut (seperti rasa, warna, dan tekstur).

Analogi ini menunjukkan bahwa clustering adalah proses pembagian item-item data ke dalam kelompok-kelompok yang memiliki kesamaan atribut. Proses ini dapat digunakan untuk memahami dan mengeksplorasi struktur internal dalam data.

#### Pengelompokan Data