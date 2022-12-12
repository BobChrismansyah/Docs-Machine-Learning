### Naive Bayes

#### Pengertian

**Naive Bayes** adalah salah satu algoritma klasifikasi yang paling sederhana dan paling cepat. Algoritma ini berdasarkan pada teorema Bayes dengan asumsi independensi antar variabel. Algoritma ini sangat cepat karena hanya melakukan perhitungan pada data yang ada saja, tidak memerlukan proses training. Algoritma ini sangat cocok untuk digunakan pada data yang memiliki banyak atribut, karena algoritma ini tidak memerlukan proses training.

Keunggulan NB adalah efektif dan cepat sehingga NB bisa digunakan pada aplikasi _spam filtering_ dan deteksi anomali di jaringan komputer.

#### Cara Kerja NB

NB adalah sekumpulan algoritma klasifikasi yuang dibangun berdasarkan **Teori Bayes** (Thomas Bayes, seorang ahli matematika dari Inggris di abad ke-18). Prinsipnya adalah menghitung seberapa tinggi kemubgkinan satu example dalam suatu observasi untuk masuk ke dalam suatu kelas, dengan memanfaatkan _training dataset_ untuk menghitung kemungkinan setiap kelas berdasarkan nilai-nilai _feature_ di dalamnya.

Dalam Statistik  teori ini dipakai untuk menjelaskan _**conditional probability**_, yaitu kemungkinan munculnya suatu kejadian A bila suatu kejadian B muncul, karena kejadian A bergantung pada kejadian B maka disebut _conditional_ atau bersyarat.

Sebagai contoh membuat model prediksi SMS termasuk pesan sampah atau bukan. Dalam kasus ini, _feature_ yang digunakan adalah kata-kata yang ada di dalam SMS. Dengan menggunakan teori Bayes, kita bisa menghitung kemungkinan SMS termasuk pesan sampah atau bukan dengan menghitung kemungkinan setiap kata-kata yang ada di dalam SMS termasuk pesan sampah atau bukan. Pesan sampah kebanyakan berisi kata "kredit" katakanlah jumlahnya 10% dari seluruh pesan SMS, lalu ditulis sebagai P("kredit") = 0,1. Lalu dari pengamatan sebelumnya diperoleh misalnya 30% dari seluruh pesan adalah pesan sampah, sehinggga ditulis P(sampah) = 0,3.
Apabila keduanya digabungkan maka _conditional propability_ dapat dihitung nilainya, yang menunjukkan kemungkinan SMS dianggap sampah jika mengandung kata "kredit". Secara matematis dapat ditulis sebagai berikut:

$P(sampah|"kredit") = \frac{P("kredit"|sampah)P(sampah)}{P("kredit")}$

Apabila _posterior propability melampaui suatu ambang batas_, maka SMS dianggap sampah. Misalnya ambang batasnya adalah 0,5, maka SMS dianggap sampah apabila $P(sampah|"kredit") > 0,5$.

#### Membuat Model NB

Langkah pertama dalam membuat model NB adalah mengubah data yang ada menjadi suatu tabel frekuensi

||Berisi Kata Kredit|||
|---|---|---|---|
|Pesan SMS|Ada|Tidak Ada|Jumlah|
|Sampah|8|22|30|
|Bukan Sampah|2|68|30|
|Jumlah|10|90|100|

Selanjutnya membuat **tabel kemungkinan** berdasarkan tabel frekuensi untuk mengukur **likehood** atau kemungkinan kemunculan kata "Kredit"

||Berisi Kata Kredit||||
|---|---|---|---|---|
|Pesan SMS|Ada|Tidak Ada|Jumlah|Kemungkinan|
|Sampah|8/30=0,27|22/30=0,73|30|0,3|
|Bukan Sampah|2/70=0,03|68/70=0,97|70|0.7
|Kemungkinan|10/100=0,1|90/100=0,9|||

P("Kredit"|Sampah) = 0,27

P(Sampah) = 0,3

Kemungkinan kata "kredit" muncul di sluruh pesan SMS yaitu 

P("kredit") = 0,1

Dengan menggunakan _posterior probability_ maka dapat dihitung nilai kemungkinan SMS dianggap sampah jika mengandung kata "kredit" yaitu P(Sampah|"kredit") = 0,27 * 0,3 / 0,1 = 0,81

Nilainya _posterior probability_ yang tinggi sehingga bisa menentukan pesan apapun yang berisi kata "kredit" adalah pasti pesan sampah.

##### Rumus Conditional Probability

Secara matematis:

$P(A|B) = \frac{P(B|A)P(A)}{P(B)} = \frac{P(B \cap A)}{P(B)}$

Dengan:
>P(A) : kemungkinan A terjadi
>P(A|B) : kemungkinan A terjadi jika B terjadi
>P(B) : kemungkinan B terjadi
>P(B|A) : kemungkinan B terjadi jika A terjadi
>P(B ∩ A) : kemungkinan B dan A terjadi

Scikit-learn menyediakan pilihan untuk membuat model NB dengan menggunakan metode Gaussian, Multinomial dan Bernoulli. Metode Gaussian digunakan untuk data yang berupa angka, sedangkan metode Multinomial digunakan untuk data yang berupa kata-kata dan metode Bernoulli digunakan untuk data yang berupa kata-kata yang bernilai 0 atau 1.

##### kelebihan dan kekurangan

Kelebihan NB adalah mudah untuk diimplementasikan dan memiliki performa yang baik. Namun, NB memiliki kekurangan yaitu tidak dapat mengklasifikasikan data yang tidak terdapat dalam data latih. Selain itu, NB juga tidak dapat mengklasifikasikan data yang memiliki nilai yang sama.
