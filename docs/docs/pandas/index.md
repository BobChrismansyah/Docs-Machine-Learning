Dasar-Dasar Pandas
=================
Langkah pertama yang harus dilakukan yaitu mengimpor library pandas:

```python
    import pandas as pd
```

Untuk mempermudah, kita akan menggunakan pd sebagai alias dari pandas.
Konspep pandas yaitu menyimpan data yang disebut **Series** dan **DataFrame**. Series adalah kolom tunggal, sedangkan DataFrame adalah tabel yang terdiri dari beberapa kolom atau series.

#### Series:

|  |mangga  |
|:-|:-|
|0  |1  |
|1  |2  |
|2  |3  |

```python
    mangga = pd.Series([1, 2, 3])
```

Pandas akan otomatis membuat index untuk series, jika tidak ingin menggunakan index default, kita bisa menambahkan parameter index:

```python
    mangga = pd.Series([1, 2, 3], index=['a', 'b', 'c'])
```

Index tidak harus berupa angka numerik, bisa kita ganti dengan string.

#### Dataframe

DataFrame tidak jauh beda dengan array NumPy yaitu berupa tabel dua dimensi dengan baris dan kolom.

Cara membuat DataFrame adalah dengan menggunakan dictionary:

```python
df1 = pd.DataFrame({3,0,9}), columns=['apel'], index=[1,2,3])
```

|  |apel  |
|:-|:-|
|1  |3  |
|2  |0  |
|3  |9  |

Untuk DataFrame dengan dua kolom, kita bisa menggunakan dictionary dengan dua key:

```python
dict1= {'apel': [3, 0, 9], 
        'jeruk': [1, 4, 2]}
df1 = pd.DataFrame(dict1)
```

|  |apel  |jeruk  |
|:-|:-|:-|
|0  |3  |1  |
|1  |0  |4  |
|2  |9  |2  |

Setelah DataFrame terbentuk kita bebas memanipulasinya.

1. Menghitung jumlah data dengan fungsi ==count()== dan juga menghitung jumlah keseluruhan semua nilai ==sum()==

    
    >```python
    >df1.count()
    >```
    >
    >Output
    >```jupyter
    >apel     3
    >jeruk    3
    >dtype: int64
    >```

    >```python
    >df1.sum()
    >```
    >
    >Output
    >```jupyter
    >apel     12
    >jeruk    7
    >dtype: int64
    >```

2. Menghitung rata-rata dengan fungsi ==mean()==
   
    >```python
    >df1.mean()
    >```
    >
    >Output
    >```jupyter
    >apel     4.000000
    >jeruk    2.333333
    >dtype: float64
    >```

3. Memapilkan statistik singkat tentang dataset seperti jumlah data, angka rata-rata, angka minimal, angka maksimum, _standart devation_, dan sebagainya

    >```python
    >df1.describe()
    >```
    >
    >Output
    >```jupyter
    >         apple       jeruk
    >count	3.000000	3.000000
    >mean	4.000000	2.333333
    >std   	4.582576	1.527525
    >min   	0.000000	1.000000
    >25%   	1.500000	1.500000
    >50%   	3.000000	2.000000
    >75%   	6.000000	3.000000
    >max   	9.000000	4.000000
    >```

#### Mengambil Subset dari DataFrame
Untuk mengambil subset dari Dataframe dalam Python dapat menggunakan operator indeks dan slicing.

Contoh mengguanakn slicing (potong data) untuk mengambil baris 0 hingga 2.

```python
df.loc[start:end]    # untuk baris, berdasarkan label
df.iloc[start:end]    # untuk baris, berdasarkan posisi indeks
```

>```python
>df1.loc[0:2]
>```
>output
>```jupyter
>   apel  jeruk
>0     3      1
>1     0      4
>2     9      2
>```
