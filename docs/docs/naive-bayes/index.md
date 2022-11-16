### Naive Bayes

#### Pengertian

**Naive Bayes** adalah salah satu algoritma klasifikasi yang paling sederhana dan paling cepat. Algoritma ini berdasarkan pada teorema Bayes dengan asumsi independensi antar variabel. Algoritma ini sangat cepat karena hanya melakukan perhitungan pada data yang ada saja, tidak memerlukan proses training. Algoritma ini sangat cocok untuk digunakan pada data yang memiliki banyak atribut, karena algoritma ini tidak memerlukan proses training.

Keunggulan NB adalah efektif dan cepat sehingga NB bisa digunakan pada aplikasi _spam filtering_ dan deteksi anomali di jaringan komputer.

#### Cara Kerja NB
NB adalah sekumpulan algoritma klasifikasi yuang dibangun berdasarkan **Teori Bayes** (Thomas Bayes, seorang ahli matematika dari Inggris di abad ke-18). Prinsipnya adalah menghitung seberapa tinggi kemubgkinan satu example dalam suatu observasi untuk masuk ke dalam suatu kelas, dengan memanfaatkan _training dataset_ untuk menghitung kemungkinan setiap kelas berdasarkan nilai-nilai _feature_ di dalamnya.

Dalam Statistik  teori ini dipakai untuk menjelaskan _**conditional probability**_, yaitu kemungkinan munculnya suatu kejadian A bila suatu kejadian B muncul, karena kejadian A bergantung pada kejadian B maka disebut _conditional_ atau bersyarat.

Sebagai contoh membuat model prediksi SMS termasuk pesan sampah atau bukan. Dalam kasus ini, _feature_ yang digunakan adalah kata-kata yang ada di dalam SMS. Dengan menggunakan teori Bayes, kita bisa menghitung kemungkinan SMS termasuk pesan sampah atau bukan dengan menghitung kemungkinan setiap kata-kata yang ada di dalam SMS termasuk pesan sampah atau bukan. Pesan sampah kebanyakan berisi kata "kredit" katakanlah jumlahnya 10% dari seluruh pesan SMS, lalu ditulis sebagai P("kredit") = 0,1. Lalu dari pengamatan sebelumnya diperoleh misalnya 30% dari seluruh pesan adalah pesan sampah, sehinggga ditulis P(sampah) = 0,3.
Apabila keduanya digabungkan maka _conditional propability_ dapat dihitung nilainya, yang menunjukkan kemungkinan SMS dianggap sampah jika mengandung kata "kredit". Secara matematis dapat ditulis sebagai berikut:

<br>

$P(sampah|"kredit) = \frac{P("kredit"|sampah)P(sampah)}{P("kredit")}$

<br>

Apabila _posterior propability melampaui suatu ambang batas_, maka SMS dianggap sampah. Misalnya ambang batasnya adalah 0,5, maka SMS dianggap sampah apabila $P(sampah|"kredit") > 0,5$.

#### Membuat Model NB

Langkah pertama dalam membuat model NB adalah mengubah data yang ada menjadi suatu tabel frekuensi

<style>
    th:first-child {
  opacity: 0;
}
</style>

<table>
    <thead>
        <tr>
            <th></th>
            <th colspan="2" >Berisi kata kredit</th>
            <th hidden ></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Pesan SMS</td>
            <td>Ada</td>
            <td>Tidak Ada</td>
            <td>Jumlah</td>   
        </tr>
        <tr>
            <td>Sampah</td>
            <td>8</td>
            <td>22</td>
            <td>30</td>
        </tr>
        <tr>
            <td>Bukan Sampah</td>
            <td>2</td>
            <td>68</td>
            <td>70</td>
        </tr>
        <tr>
            <td>Jumlah</td>
            <td>10</td>
            <td>90</td>
            <td>100</td>
        </tr>
    </tbody>
</table>

