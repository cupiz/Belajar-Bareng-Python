# Sesi 2 : Struktur Python

[TOC]





### Pengantar

Kita akan melihat bagaimana menggunakan struktur data untuk menyimpan tipe data yang lebih kompleks yang membantu memodelkan data aktual dan merepresentasikannya di dunia nyata.

Dalam bahasa pemrograman, struktur data mengacu pada objek yang dapat menampung beberapa data bersama-sama, yang berarti mereka digunakan untuk menyimpan kumpulan data terkait.

Misalnya, kita dapat menggunakan daftar untuk menyimpan item yang harus dilakukan untuk hari itu. Berikut ini adalah contoh untuk menunjukkan kepada kita bagaimana daftar dikodekan:

```
todo = ["ambil cucian", "beli bahan makanan", "bayar tagihan listrik"]
```

Kita juga dapat menggunakan objek kamus untuk menyimpan informasi yang lebih kompleks seperti detail pelanggan dari mail list. Berikut ini contoh cuplikan kode :

```
User = {
    "nama_pertama": "Iqbal",
    "nama_terakhir": "Ahdagita",
    "usia": 23,
    "email": "spfindo@gmail.com"
}
```

Ada empat jenis struktur data di Python : **list, tuple, dictionary**, dan **set**.

Struktur data ini menentukan hubungan antara data dan operasi yang dapat dilakukan pada data. Cara mengatur dan menyimpan data yang dapat diakses secara efisien dalam berbagai keadaan.





### Kekuatan List

List adalah jenis wadah di Python yang digunakan untuk menyimpan beberapa kumpulan data pada waktu yang sama. List Python sering dibandingkan dengan array dalam bahasa pemrograman lain, tetapi list melakukan lebih banyak lagi.



![](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/1.png)



List di Python ditulis dalam tanda kurung siku, **[  ]**. Setiap elemen dalam list memiliki **position** dan **index** yang berbeda. Unsur-unsur dalam list memiliki urutan yang terbatas. Seperti bahasa pemrograman lainnya, indeks item pertama dari list adalah 0, dan item kedua memiliki indeks 1, dan seterusnya. Ini berkaitan dengan bagaimana list diimplementasikan pada tingkat pemrograman yang lebih rendah.





#### Latihan 21 :  Mencoba Python List

Dalam latihan ini, kita akan belajar bagaimana bekerja dengan List Python dengan membuat kode dan membuat List dan menambahkan item. Misalnya, kita harus menggunakan list untuk menyimpan item yang ada di keranjang belanja :

1. Buka Notebook Jupyter baru.

2. Sekarang masukkan potongan kode berikut:

  ```
  belanja = ["roti", "susu", "telur"]
  print(belanja)
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  ['roti', 'susu', 'telur']
  ```

  Kita membuat list yang disebut belanja dan menambahkan item ke list kita (roti, susu, dan telur).
  Karena list adalah jenis iterable di Python, kita dapat menggunakan **for** loop untuk mengulang semua elemen di dalam list.

3. Sekarang, masukkan dan jalankan kode for loop dan amati hasilnya:

  ```
  for item in belanja:
  	print(item)
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  roti
  susu
  telur
  ```

4. Sekarang gunakan jenis data campuran di dalam konten list dan masukkan kode berikut di sel baru:

   ```
   mixed = [365, "hari", True]
   print(mixed)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   [365, 'hari', True]
   ```

   Tetapi kita mungkin bertanya-tanya, dalam hal ini, bukankah seharusnya kita diizinkan menyimpan list di dalam list ? Mari kita lihat di bagian selanjutnya. Ini juga dikenal sebagai **nested list (bersarang)**, yang dapat digunakan untuk merepresentasikan struktur data yang kompleks.





#### Matriks di Nested List

Sebagian besar data yang kita simpan di dunia nyata berbentuk tabel data, yaitu baris dan kolom, bukan dalam bentuk daftar datar satu dimensi. Tabel semacam itu disebut matriks atau array dua dimensi. Python (dan sebagian besar bahasa pemrograman lainnya) tidak menyediakan struktur tabel di luar kotak. Bahasa pemrograman tidak menyediakan struktur tabel karena ini bukan peran bahasa untuk melakukannya. Struktur tabel hanyalah cara untuk menyajikan data.

Yang dapat kita lakukan adalah menampilkan struktur tabel yang ditunjukkan dibawah menggunakan list; Misalnya jika kita ingin menyimpan pesanan buah berikut menggunakan list :

```
+------+--------+-------+
| Apel | Pisang | Jeruk |
+------+--------+-------+
| 5    | 8      | 9     |
+------+--------+-------+
| 7    | 2      | 2     |
+------+--------+-------+
```

Secara matematis, kita dapat menyajikan informasi yang ditunjukkan di atas menggunakan matriks 2 x 3 (2 baris kali 3 kolom). Matriks ini akan terlihat seperti ini :

![2](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/2.png)

Sekarang kita akan melihat bagaimana kita dapat menyimpan matriks ini sebagai nested list dalam latihan berikut.





#### Latihan 22: Menggunakan Nested List untuk Menyimpan Data dari Matriks

Dalam latihan ini, kita akan melihat cara kerja dengan nested list, menyimpan nilai di dalamnya, dan mengaksesnya menggunakan sejumlah metode :

1. Buka notebook Jupyter baru.

2. Masukkan kode berikut di sel baru :

   ```
   m = [[1, 2, 3], [4, 5, 6]]
   ```

3. Sekarang **print** list **m**:

   ```
   print(m[1][1])
   ```

   Kita sekarang dapat mengakses elemen menggunakan notasi variabel [baris] [kolom].
   Kita akan mendapatkan keluaran berikut :

   ```
   5
   ```

   Ini mencetak nilai baris 2, kolom 2, yaitu 5 (ingat, kita menggunakan offset indeks berbasis nol).

4. Sekarang, akses setiap elemen dalam matriks nested list dengan mempertahankan indeks referensinya dengan dua variabel, **i** dan **j** :

   ```
   for i in range(len(m)):
   	for j in range(len(m[i])):
   		print(m[i][j])
   ```

   Kode sebelumnya menggunakan **for** loop untuk mengulang dua kali. Di loop luar (**i**), kita mengulang setiap baris dalam matriks **m**, dan di loop dalam (**j**), kita mengulang setiap kolom dalam baris. Akhirnya, kita **print** elemen di posisi yang sesuai.

   Kita akan mendapatkan keluaran berikut :

   ```
   1
   2
   3
   4
   5
   6
   ```

5. Gunakan dua **for..in** loop untuk mencetak semua elemen dalam matriks:

   ```
   for row in m:
   	for col in row:
   		print(col)
   ```

   Perulangan **for** pada kode yang digunakan pada langkah 4 mengulang baris dan kolom. Jenis notasi ini tidak mengharuskan kita memiliki pengetahuan sebelumnya tentang dimensi matriks.

   Kita akan mendapatkan keluaran berikut :

   ```
   1
   2
   3
   4
   5
   6
   ```

Di akhir latihan ini, kita mengetahui cara kerja nested list yang disimpan sebagai matriks. Kita juga harus mengetahui berbagai cara mengakses nilai dari nested list. Dalam Kegiatan 6, Menggunakan Nested List untuk Menyimpan Data Karyawan, kita akan menerapkan konsep yang telah kita pelajari tentang list dan nested list untuk menyimpan data karyawan.





#### Kegiatan 6 : Menggunakan Nested List untuk Menyimpan Data Karyawan

Kita akan menyimpan data tabel menggunakan nested list. Bayangkan ini : Kita saat ini bekerja di sebuah perusahaan IT dan diberi daftar karyawan berikut. Kita diminta oleh manajer untuk menggunakan Python untuk menyimpan data ini untuk penggunaan perusahaan lebih lanjut.

Tujuan dari kegiatan ini adalah menggunakan nested list untuk menyimpan data dan mencetaknya saat kita membutuhkannya.
Data yang diberikan kepada kita oleh perusahaan ditampilkan dibawah :

![3](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/3.png)

Ikuti langkah-langkah berikut untuk menyelesaikan kegiatan ini:
1. Buka Notebook Jupyter baru.

2. Buat list dan tetapkan ke **employees**.

3. Buat tiga nested list di **employees** untuk menyimpan informasi masing-masing karyawan.

4. Cetak variabel **employees**.

5. Cetak detail semua karyawan dalam format yang rapi.

6. Cetak hanya detail Lisa Crawford.
    Dengan mencetak detail dalam format yang rapi, kita akan mendapatkan hasil sebagai berikut :

  ![4](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/4.png)





### Operasi Matriks

Kita akan terus melihat cara menggunakan nested list untuk beberapa operasi matriks dasar. Pertama, kita melihat cara menambahkan dua matriks dengan Python. Penambahan matriks mengharuskan kedua matriks memiliki dimensi yang sama; hasilnya juga akan memiliki dimensi yang sama.

Dalam Latihan 23, Menerapkan Operasi Matriks (Penjumlahan dan Pengurangan), kita akan menggunakan data matriks berikut, **X** dan **Y**, dalam gambar di bawah :

![5](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/5.png)





#### Latihan 23, Menerapkan Operasi Matriks (Penjumlahan dan Pengurangan)

Dalam latihan ini kita akan menambah dan mengurangi matriks X dan Y menggunakan Python.
Langkah-langkah berikut akan memungkinkan kita menyelesaikan latihan:

1. Buka Notebook Jupyter baru.

2. Buat dua nested list, X dan Y, untuk menyimpan nilai :

   ```
   X = [[1,2,3],[4,5,6],[7,8,9]]
   Y = [[10,11,12],[13,14,15],[16,17,18]]
   ```

3. Inisialisasi matriks nol 3 x 3 yang disebut **result** sebagai placeholder :

   ```
   # Inisialisasi result placeholder
   result = [[0,0,0],
       [0,0,0],
       [0,0,0]]
   ```

4. Sekarang, terapkan algoritma dengan melakukan iterasi melalui sel dan kolom matriks:

   ```
   # mengulangi baris
   for i in range(len(X)):
   # mengulangi kolom
   	for j in range(len(X[0])):
   		result[i][j] = X[i][j] + Y[i][j]
   
   print(result)
   ```

   Kita akan menggunakan metode nested list. Seperti yang kita pelajari di bagian sebelumnya, kita terlebih dahulu mengiterasi baris dalam matriks **X**, lalu mengiterasi kolom. Kita tidak perlu mengulang matriks **Y** lagi karena kedua matriks memiliki dimensi yang sama. Hasil dari baris tertentu (dilambangkan dengan **i**) dan kolom tertentu (dilambangkan dengan **j**) sama dengan jumlah baris dan kolom masing-masing dalam matriks **X** dan **Y**.

   Kita akan mendapatkan keluaran berikut :

   ```
   [[11, 13, 15], [17, 19, 21], [23, 25, 27]]
   ```

5. Kita juga dapat melakukan pengurangan menggunakan dua matriks menggunakan algoritma yang sama dengan operator yang berbeda. Ide di balik ini persis sama dengan langkah 3, kecuali kita melakukan pengurangan. Kita dapat menerapkan kode berikut untuk mencoba pengurangan matriks :

   ```
   X = [[10,11,12],[13,14,15],[16,17,18]]
   Y = [[1,2,3],[4,5,6],[7,8,9]]
   
   result = [[0,0,0],
       [0,0,0],
       [0,0,0]]
   
   for i in range(len(X)):
   	for j in range(len(X[0])):
   		result[i][j] = X[i][j] - Y[i][j]
   
   print(result)
   ```

   Kita akan mendapatkan keluaran berikut :

   ```
   [[9, 9, 9], [9, 9, 9], [9, 9, 9]]
   ```





#### Operasi Perkalian Matriks

Kita dapat melihat cara menggunakan nested list untuk melakukan perkalian matriks untuk dua matriks yang ditunjukkan pada gambar dibawah :

![5a](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/5a.png)

Untuk operasi perkalian matriks, jumlah kolom pada matriks pertama (X) harus sama dengan jumlah baris pada matriks kedua (Y). Hasilnya akan memiliki jumlah baris yang sama dengan matriks pertama dan jumlah kolom yang sama dengan matriks kedua. Dalam hal ini, hasil matriks adalah matriks 3 x 4.





#### Latihan 24: Menerapkan Operasi Matriks (Perkalian)

Dalam latihan ini, tujuan akhir kita adalah mengalikan dua matriks, **X** dan **Y**, dan mendapatkan nilai keluaran. Langkah-langkah berikut akan memungkinkan kita menyelesaikan latihan:
1. Buka notebook Jupyter baru.

2. Buat dua nested list, **X** dan **Y**, untuk menyimpan nilai matriks **X** dan **Y ** :

   ```
   X = [[1, 2], [4, 5], [3, 6]]
   Y = [[1,2,3,4],[5,6,7,8]]
   ```

3. Buat placeholder matriks-nol untuk menyimpan hasil :

   ```
   result = [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]
   ```

4. Implementasikan algoritma perkalian matriks untuk menghitung hasil :

   ```
   # iterasi baris X
   for i in range(len(X)):
   
       # iterasi kolom Y
       for j in range(len(Y[0])):
   
   		# iterasi baris Y
           for k in range(len(Y)):
           	result[i][j] += X[i][k] * Y[k][j]
   ```

   Kita mungkin telah memperhatikan bahwa algoritma ini sedikit berbeda dari yang kita gunakan di Latihan 23, Menerapkan Operasi Matriks (Penjumlahan dan Pengurangan), langkah 3. Ini karena kita perlu mengulang baris dari matriks kedua, **Y**, sebagai matriks memiliki bentuk yang berbeda, seperti yang disebutkan dalam potongan kode sebelumnya.

5. Sekarang, **print** hasil akhirnya :

   ```
   for r in result:
   	print(r)
   ```

   Kita akan mendapatkan keluaran/ouput sebagai berikut :

   ```
   [11, 14, 17, 20]
   [29, 38, 47, 56]
   [33, 42, 51, 60]
   ```





### Metode List

Seperti yang telah dibahas sebelumnya, karena list adalah jenis urutan, list mendukung semua operasi dan metode urutan.

List adalah salah satu struktur data terbaik untuk digunakan. Python menyediakan sekumpulan metode list yang memudahkan kita menyimpan dan mengambil nilai untuk memelihara, memperbarui, dan mengekstrak data. Operasi umum ini adalah apa yang dilakukan pemrogram Python, termasuk **slicing**, sorting, **appending**, **searching**, **inserting**, dan **removing** data.

Cara terbaik untuk memahami hal ini adalah dengan melihat mereka di tempat kerja. Kita akan mempelajari tentang metode list praktis ini dalam latihan berikut.





#### Latihan 25: Operasi List Dasar

Dalam latihan ini, kita akan menggunakan fungsi dasar list untuk memeriksa ukuran list, menggabungkan list dan juga menduplikat list. Ikuti langkah ini :

1. Buka notebook Jupyter baru.

2. Ketikkan kode berikut

  ```
  belanja = ["roti", "susu", "telur"]
  ```

3. Panjang list ditemukan menggunakan fungsi **len**.

  ```
  print(len(belanja))
  ```

  Kita akan mendapatkan keluaran/ouput sebagai berikut :

  ```
  3
  ```

4. Sekarang gabungkan dua list menggunakan operator **+ ** :

   ```
   list1 = [1,2,3]
   list2 = [4,5,6]
   final_list = list1 + list2
   print(final_list)
   ```

   Kita akan mendapatkan keluaran/ouput sebagai berikut :

   ```
   [1, 2, 3, 4, 5, 6]
   ```

   Seperti yang kita lihat di output, list juga mendukung banyak operasi string, salah satunya adalah penggabungan, yang menggabungkan dua atau lebih list bersama.

5. Sekarang gunakan operator *****, yang dapat digunakan untuk pengulangan dalam list untuk menggkitakan elemen :

   ```
   list3 = ['oi']
   print(list3*3)
   ```

   Ini akan mengulangi kata 'oi' tiga kali, memberi kita output berikut :

   ```
   ['oi', 'oi', 'oi']
   ```





#### Mengakses Item dari List

Sama seperti bahasa pemrograman lainnya, dengan Python, kita dapat menggunakan metode pengindeks untuk mengakses elemen dalam list. Kita harus menyelesaikan latihan berikut dengan melanjutkan dengan notebook Jupyter sebelumnya.





#### Latihan 26: Mengakses Item dari List Daftar Belanja

Dalam latihan ini, kita akan bekerja dengan list dan mendapatkan pemahaman tentang bagaimana kita dapat mengakses item dari list. Langkah-langkah berikut akan memungkinkan kita menyelesaikan latihan:

1. Buka Notebook Jupyter baru.

2. Masukkan kode berikut di sel baru:

  ```
  belanja = ["roti", "susu", "telur"]
  print(belanja[1])
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  susu
  ```

  Seperti yang kita lihat, kita telah mencetak nilai **susu** dari list **belanja** yang memiliki ekstensi indeks 1, sebagai daftar dimulai dari 0.

3. Sekarang, akses elemen **susu** dan ganti dengan **pisang**:

  ```
  belanja[1] = "pisang"
  print(belanja)
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  ['roti', 'pisang', 'telur']
  ```

4. Ketik kode berikut di sel baru dan amati hasilnya:

  ```
  print(belanja[-1])
  ```

  Kita harus mendapatkan keluaran berikut:

  ```
  telur
  ```

  Outputnya akan mencetak **telur** - item terakhir.

  Apa yang telah kita pelajari sejauh ini lebih merupakan cara tradisional untuk mengakses elemen. List Python juga mendukung pengindeksan umum yang kuat, yang disebut **slicing**. Ia menggunakan notasi **:** dalam format **list[i:j]**, di mana **i** adalah elemen awal, dan **j** adalah elemen terakhir.

5. Masukkan kode berikut untuk mencoba jenis pemotongan yang berbeda:

  ```
  print(belanja[0:2])
  ```

  Ini mencetak elemen pertama dan kedua, menghasilkan keluaran sebagai berikut:

  ```
  ['roti', 'pisang']
  ```

  Sekarang, untuk mencetak dari awal daftar ke elemen ketiga

  ```
  print(belanja[:3])
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  ['roti', 'pisang', 'telur']
  ```

  Begitu pula untuk mencetak dari kedua elemen list hingga akhir

  ```
  print(belanja[1:])
  ```

  Kita akan mendapatkan keluaran berikut:

  ```
  ['pisang', 'telur']
  ```





#### Menambahkan Item ke List

Di bagian sebelumnya dan Latihan 26, Mengakses Item dari List Daftar Belanja, kita telah mempelajari cara mengakses item dari list. List sangat bermanfaat dan digunakan secara luas dalam banyak situasi. Namun, kita sering kali tidak mengetahui data yang ingin disimpan pengguna sebelumnya, tetapi hanya setelah program berjalan. Di sini, kita akan melihat berbagai metode untuk menambahkan item dan memasukkan item ke dalam list.





#### Latihan 27: Menambahkan Item ke List Belanja Kita

Metode **append** adalah cara termudah untuk menambahkan elemen baru ke akhir daftar. Kita akan menggunakan metode ini dalam latihan ini untuk menambahkan item ke daftar belanja kita. Langkah-langkah berikut akan memungkinkan kita menyelesaikan latihan :

1. Di sel baru, ketik kode berikut untuk menambahkan elemen baru, apel, ke akhir list menggunakan metode append :

   ```
   belanja = ["roti", "susu", "telur"]
   belanja.append("apel")
   print(belanja)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ['roti', 'susu', 'telur', 'apel']
   ```

   Metode append biasanya digunakan saat kita membuat list tanpa mengetahui jumlah total elemennya. Kita akan mulai dengan list kosong dan terus menambahkan item untuk membangun list.

2. Sekarang buat list kosong, **belanja**, dan terus tambahkan item satu per satu ke list kosong ini :

   ```
   belanja = [ ]
   belanja.append('roti')
   belanja.append('susu')
   belanja.append('telur')
   belanja.append('apel')
   print(belanja)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ['roti', 'susu', 'telur', 'apel']
   ```

   Dengan cara ini, kita memulai dengan menginisialisasi list kosong, dan kita memperluas list secara dinamis. Hasil akhirnya persis sama dengan list dari kode sebelumnya. Ini berbeda dari beberapa bahasa pemrograman yang membutuhkan ukuran array untuk diperbaiki pada tahap deklarasi.

3. Sekarang gunakan metode **insert** untuk menambahkan elemen ke list belanja :

   ```
   belanja.insert(2, 'daging')
   print(belanja)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ['roti', 'susu', 'daging', 'telur', 'apel']
   ```

   Saat kita membuat kode di langkah 3, kita menemukan cara lain untuk menambahkan elemen ke list, menggunakan metode **insert**. Metode **insert** membutuhkan indeks posisi untuk menunjukkan di mana elemen baru harus ditempatkan. Indeks posisi adalah angka berbasis nol yang menunjukkan posisi dalam list. Kita dapat menggunakan kode berikut untuk memasukkan item, **daging**, di posisi ketiga.

   Kita dapat melihat bahwa **daging** dimasukkan di posisi ketiga dan menggeser setiap item lainnya satu posisi ke kanan.

Setelah menyelesaikan latihan ini, kita sekarang dapat menambahkan elemen ke list kita, yaitu belanja. Ini terbukti sangat berguna ketika kita mendapatkan data dari pelanggan atau klien, memungkinkan kita menggunakan metode yang telah kita sebutkan dan menambahkan item ke daftar kita.





### Dictionary Keys dan Values

Python Dictionary (Kamus) adalah koleksi yang tidak berurutan. Kamus ditulis dengan tanda kurung kurawal, dan memiliki keys (kunci) dan **values** (nilai).

Misalnya, lihat contoh berikut, di mana kita menyimpan detail seorang karyawan :

```
employee = {
    'name': "Jack Nelson",
    'age': 32,
    'department': "sales"
}
```

Kita mungkin telah memperhatikan kemiripan tertentu antara Kamus Python dan JSON. Meskipun kita dapat memuat JSON langsung ke Python, Kamus Python adalah struktur data lengkap yang menerapkan algoritmanya sendiri, dan JSON hanyalah string murni yang ditulis dalam format serupa.

Kamus Python adalah sesuatu yang mirip dengan pasangan key-value. Mereka hanya memetakan kunci ke nilai terkait, seperti yang ditunjukkan pada gambar dibawah :

![7](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/7.png)

Kamus itu seperti list. Keduanya berbagi properti berikut:
• Keduanya dapat digunakan untuk menyimpan nilai.
• Keduanya dapat diubah di tempat nya dan dapat tumbuh serta menyusut sesuai permintaan.
• Keduanya bisa nested : kamus bisa berisi kamus lain, list bisa berisi list lain, dan list bisa berisi kamus dan sebaliknya.

Perbedaan utama antara list dan kamus adalah bagaimana elemen diakses. Elemen list diakses oleh indeks posisinya, yaitu [0,1,2…] sedangkan elemen kamus diakses melalui kunci. Oleh karena itu, kamus adalah pilihan yang lebih baik untuk merepresentasikan koleksi, dan kunci mnemonik lebih cocok ketika item koleksi diberi label, misalnya, record database seperti gambar dibawah. Basis data di sini setara dengan list, dan list basis data berisi catatan yang dapat direpresentasikan menggunakan kamus. Di dalam setiap record, ada field untuk menyimpan nilai masing-masing, dan kamus dapat digunakan untuk menyimpan record dengan kunci unik yang dipetakan ke nilai :

![8](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/8.png)

Namun, ada beberapa aturan yang perlu kita ingat dengan kamus Python:
• Kunci harus unik - tidak ada kunci duplikat yang diperbolehkan.
• Kunci harus tetap - bisa berupa string, angka, atau tupel.
Kita akan mencoba dengan kamus dan menyimpan record dalam Latihan 28, Menggunakan Kamus untuk Menyimpan Record Film.





#### Latihan 28 : Menggunakan Kamus untuk Menyimpan Record Film

Dalam latihan ini, kita akan bekerja dengan kamus untuk menyimpan record film, dan kita juga akan mencoba dan mengakses informasi dalam kamus dengan menggunakan kunci. Langkah-langkah berikut akan memungkinkan kita menyelesaikan latihan:

1. Buka Notebook Jupyter.

2. Masukkan kode berikut di sel kosong :

   ```
   movie = {
       "title": "The Godfather",
       "director": "Francis Ford Coppola",
       "year": 1972,
       "rating": 9.2
   }
   ```

   Di sini, kita telah membuat kamus film dengan beberapa detail, seperti **title**, **director**, **year**, dan **rating**.

3. Akses informasi dari kamus dengan menggunakan tombol. Misalnya, kita dapat menggunakan **'year'** untuk mengetahui kapan film tersebut pertama kali dirilis :

   ```
   print(movie['year'])
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   1972
   ```

4. Sekarang perbarui nilai kamus :

   ```
   movie['rating'] = (movie['rating'] + 9.3)/2
   print(movie['rating'])
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   9.25
   ```

   Seperti yang kita lihat, nilai kamus juga dapat diperbarui di tempat.

5. Buat kamus **movie** dari awal dan kembangkan menggunakan penetapan nilai kunci :

   ```
   movie = {}
   movie['title'] = "The Godfather"
   movie['director'] = "Francis Ford Coppola"
   movie['year'] = 1972
   movie['rating'] = 9.2
   ```

   Seperti yang mungkin kita lihat, mirip dengan list, kamus fleksibel dalam hal ukuran.

6. Kita juga dapat menyimpan list di dalam kamus dan menyimpan kamus di dalam kamus itu :

   ```
   movie['actors'] = ['Marlon Brando', 'Al Pacino', 'James Caan']
   movie['other_details'] = {
       'runtime': 175,
       'language': 'English'
   }
   print(movie)
   ```

   Kita akan mendapatkan keluaran berikut :

![9](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/9.png)

Hingga saat ini, kita telah melihat betapa mudahnya menerapkan nested di list dan kamus. Dengan menggabungkan list dan kamus secara kreatif, kita dapat menyimpan informasi dunia nyata yang kompleks dan struktur model secara langsung dan mudah. Ini adalah salah satu manfaat utama Python.





#### Kegiatan 7 : Menyimpan Data Tabel Karyawan Perusahaan Menggunakan List dan Kamus

Ingat kumpulan data karyawan, yang sebelumnya kita simpan menggunakan nested list ? Sekarang setelah kita mempelajari tentang list dan kamus, kita akan melihat bagaimana kita dapat menyimpan dan mengakses data secara lebih efektif menggunakan dua tipe data ini - list dan kamus :

![10](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/10.png)

Ikuti langkah-langkah berikut untuk menyelesaikan aktivitas ini:
1. Buka notebook Jupyter (Kita dapat membuat yang baru atau menggunakan yang sudah ada).

2. Buat list bernama **employees**.

3. Buat tiga objek kamus di dalam **employees** untuk menyimpan informasi setiap karyawan.

4. Cetak variabel **employees**.

5. Cetak detail semua karyawan dalam format yang rapi.

6. Cetak hanya detail **Sujan Patel**.
    Kita akan mendapatkan keluaran berikut:

  ```
  Name: Sujan Patel
  Age: 33
  Department : HR
  --------------------
  ```





#### Zipping dan Unzipping Kamus menggunakan zip()

Terkadang, kita memperoleh informasi dari beberapa list. Misalnya, kita mungkin memiliki list untuk menyimpan nama produk dan list lain hanya untuk menyimpan jumlah produk tersebut. Yang dapat kita lakukan adalah menggabungkan list menggunakan metode **zip()**.

Metode **zip()** memetakan indeks serupa dari beberapa penampung sehingga dapat digunakan hanya sebagai satu objek. Kita akan mencobanya pada latihan berikut.





#### Latihan 29 : Menggunakan Metode zip() untuk Memanipulasi Kamus

Dalam latihan ini, kita akan mengerjakan konsep kamus, tetapi kita akan berfokus untuk memanipulasinya dengan menggabungkan berbagai jenis struktur data. kita akan menggunakan metode **zip()** untuk memanipulasi kamus dengan list belanja. Langkah-langkah berikut akan membantu kita memahami metode **zip()** :

1. Buka Notebook Jupyter baru.

2. Sekarang buat sel baru dan ketik kode berikut:

   ```
   item = ['apel', 'jeruk', 'pisang']
   kuantitas = [5,3,2]
   ```

   Di sini, kita telah membuat list **item** dan list **kuantitas**. Selain itu, kita telah menetapkan nilai ke list ini.

3. Sekarang gunakan fungsi zip() untuk menggabungkan dua list menjadi sebuah list tuple :

   ```
   pesanan = zip(item, kuantitas)
   print(pesanan)
   ```

   Ini memberi kita objek **zip()** dengan output berikut:

   ```
   <zip object at 0x0000000005BF1088>
   ```

4. Masukkan kode berikut untuk mengubah objek zip itu menjadi list :

   ```
   pesanan = zip(item, kuantitas)
   print(list(pesanan))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   [('apel', 5), ('jeruk', 3), ('pisang', 2)]
   ```

5. Kita juga dapat membuat objek **zip** menjadi **tuple** :

   ```
   pesanan = zip(item, kuantitas)
   print(tuple(pesanan))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   (('apel', 5), ('jeruk', 3), ('pisang', 2))
   ```

6. Kita juga dapat membuat objek **zip** menjadi kamus :

   ```
   pesanan = zip(item, kuantitas)
   print(dict(pesanan))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   {'apel': 5, 'jeruk': 3, 'pisang': 2}
   ```

   Tahukah kita bahwa kita harus memanggil **pesanan = zip(item, kuantitas)** setiap saat? Dalam latihan ini, kita akan mengetahui bahwa objek **zip()** adalah iterator dan, oleh karena itu, setelah diubah menjadi list, tuple, atau kamus, itu dianggap sebagai iterasi penuh dan tidak akan dapat membuat values lagi.





### Metode Kamus

Sekarang kita telah belajar tentang kamus dan kapan kita harus menggunakan kamus. Sekarang kita akan melihat beberapa metode kamus lainnya. Untuk memulainya, kita harus mengikuti latihan dari sini dan seterusnya untuk mempelajari cara mengakses nilai dan operasi terkait lainnya dari kamus dengan Python.





#### Latihan 30: Mengakses Kamus Menggunakan Metode Kamus

Dalam latihan ini, kita akan belajar bagaimana mengakses kamus menggunakan metode kamus. Tujuan dari latihan ini adalah untuk mencetak nilai urutan terhadap item tersebut saat mengakses kamus dengan menggunakan metode kamus :

1. Buka Notebook Jupyter baru.

2. Masukkan kode berikut di sel baru:

   ```
   pesanan = {'apel': 5, 'jeruk': 3, 'pisang': 2}
   print(pesanan.values())
   print(list(pesanan.values()))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   dict_values([5, 3, 2])
   [5, 3, 2]
   ```

   Metode **values()** dalam kode ini mengembalikan objek yang dapat diulang. Untuk langsung menggunakan nilai, kita dapat menggabungkannya dalam list secara langsung.

3. Sekarang, dapatkan list kunci dalam kamus dengan menggunakan metode **keys()** :

   ```
   print(list(pesanan.keys()))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ['apel', 'jeruk', 'pisang']
   ```

4. Karena kita tidak dapat mengulang kamus secara langsung, kita terlebih dahulu mengonversinya menjadi list tuple menggunakan metode **items()**, kemudian mengulang list yang dihasilkan dan mengaksesnya. Ini disebutkan dalam cuplikan kode berikut :

   ```
   for tuple in list(pesanan.items()):
   	print(tuple)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ('apel', 5)
   ('jeruk', 3)
   ('pisang', 2)
   ```





### Tuples

Objek tuple mirip dengan list, tetapi tidak dapat diubah. Tuple adalah urutan yang tidak dapat diubah, yang berarti nilainya tidak dapat diubah setelah inisialisasi. Kita menggunakan tupel untuk merepresentasikan koleksi item tetap :

![11](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/11.png)

Misalnya, kita dapat menentukan weekdays menggunakan list, sebagai berikut :

```
weekdays_list = ['Monday', 'Tuesday',
'Wednesday','Thursday','Friday','Saturday', 'Sunday']
```

Namun, ini tidak menjamin bahwa nilai akan tetap tidak berubah selama masa pakainya karena list **bisa berubah**. Apa yang bisa kita lakukan adalah mendefinisikannya menggunakan tuple, seperti yang ditunjukkan pada kode berikut :

```
weekdays_tuple = ('Monday', 'Tuesday',
'Wednesday','Thursday','Friday','Saturday', 'Sunday')
```

Karena tupel tidak dapat diubah, kita dapat yakin bahwa nilainya konsisten di seluruh program dan tidak akan dimodifikasi secara tidak sengaja. Dalam Latihan 31, Menjelajahi Properti Tuple di List Belanja, kita akan menjelajahi properti berbeda yang disediakan oleh Developer Python.





#### Latihan 31 : Menjelajahi Properti Tuple di List Belanja

Dalam latihan ini, kita akan belajar tentang berbagai properti tupel:

1. Buka notebook Jupyter.

2. Ketik kode berikut di sel baru untuk menginisialisasi tupel baru, **t**:

   ```
   t = ('bread', 'milk', 'eggs')
   print(len(t))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   3
   ```

3. Sekarang, seperti yang disebutkan dalam catatan, masukkan baris kode berikut dan amati kesalahannya:

   ```
   t.append('apple')
   t[2] = 'apple'
   ```

   Kita akan mendapatkan keluaran berikut:

   ![12](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/12.png)

Satu-satunya cara untuk menyiasatinya adalah dengan membuat tupel baru dengan menggabungkan tupel yang ada dengan item baru lainnya.

4. Sekarang gunakan kode berikut untuk menambahkan dua item, **apple** dan **orange**, ke tupel kita, **t.** Ini akan memberi kita tupel baru. Perhatikan bahwa tupel yang ada tetap tidak berubah :

   ```
   print(t + ('apple', 'orange'))
   print(t)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   ('bread', 'milk', 'eggs', 'apple', 'orange')
   ('bread', 'milk', 'eggs')
   ```

5. Masukkan pernyataan berikut di sel baru dan amati hasilnya:

   ```
   t_mixed = 'apple', True, 3
   print(t_mixed)
   t_shopping = ('apple',3), ('orange',2), ('banana',5)
   print(t_shopping)
   ```

   Tuple juga mendukung tipe mixed dan nested, seperti list dan kamus. Kita juga dapat mendeklarasikan tupel tanpa menggunakan tanda kurung, seperti yang ditunjukkan pada kode yang kta masukkan pada Langkah 5.

   Kita akan mendapatkan keluaran berikut:

   ```
   ('apple', True, 3)
   (('apple',3), ('orange',2), ('banana',5))
   ```





### Survei Sets

Sejauh ini, di bab ini, kita telah membahas list, kamus, dan tupel. Kita sekarang dapat melihat set, yang merupakan tipe lain dari struktur data Python.

Set adalah tambahan yang relatif baru untuk jenis koleksi Python. Mereka adalah koleksi tak berurutan dari objek unik dan tak berubah yang mendukung operasi yang meniru teori himpunan matematika. Karena set tidak mengizinkan beberapa kemunculan dari elemen yang sama, mereka dapat digunakan untuk secara efektif mencegah nilai duplikat.

Satu set adalah kumpulan objek (disebut anggota atau elemen). Misalnya, kita dapat menentukan himpunan A sebagai bilangan genap antara 1 sampai 10, dan itu akan berisi {2,4,6,8,10}, dan himpunan B bisa berupa bilangan ganjil antara 1 sampai 10, dan itu akan berisi {1,3,5,7,9}. Dalam latihan berikut, kita akan mendapatkan set dengan Python:





#### Latihan 32 : Menggunakan Sets di Python

Dalam latihan ini, kita akan mendapatkan pemahaman tentang set dengan Python. Satu set adalah kumpulan objek :

1. Buka notebook Jupyter.

2. Inisialisasi satu set menggunakan kode berikut. Kita dapat mengirimkan daftar untuk menginisialisasi satu set:

   ```
   s1 = set([1,2,3,4,5,6])
   print(s1)
   s2 = set([1,2,2,3,4,4,5,6,6])
   print(s2)
   s3 = set([3,4,5,6,6,6,1,1,2])
   print(s3)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   {1, 2, 3, 4, 5, 6}
   {1, 2, 3, 4, 5, 6}
   {1, 2, 3, 4, 5, 6}
   ```

   Kita dapat melihat bahwa set unik dan tidak berurutan, jadi item duplikat dan nilai asli tidak disimpan.

3. Masukkan kode berikut di sel baru:

   ```
   s4 = {"apple", "orange", "banana"}
   print(s4)
   ```

   Kita juga dapat menginisialisasi set menggunakan tanda kurung kurawal secara langsung.
   Kita akan mendapatkan keluaran berikut :

   ```
   {'apple', 'orange', 'banana'}
   ```

4. Set bisa berubah. Ketik kode berikut dan lihat bagaimana kita menambahkan item baru, **pineapple**, ke set yang ada, s4:

   ```
   s4.add('pineapple')
   print(s4)
   ```

   Kita akan mendapatkan keluaran berikut :

   ```
   {'apple', 'orange', 'pineapple', 'banana'}
   ```





#### Operasi Set

Set mendukung operasi umum seperti unions dan intersectionsn. Operasi **union** mengembalikan satu set yang berisi semua elemen unik di set A dan B; operasi **intersect** mengembalikan satu set yang berisi elemen unik milik himpunan A dan juga milik himpunan B pada saat yang sama:

![13](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/13.png)



Gambar berikut mewakili operasi intersect:

![14](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi2/14.png)



Sekarang kita akan melihat bagaimana mengimplementasikan operasi set ini dengan Python dalam latihan berikut:





#### Latihan 33 : Menerapkan Operasi Set

Dalam latihan ini, kita akan menerapkan dan bekerja dengan operasi yang ditetapkan:
1. Buka notebook Jupyter baru.

2. Di sel baru, ketik kode berikut untuk menginisialisasi dua set baru:

   ```
   s5 = {1,2,3,4}
   s6 = {3,4,5,6}
   ```

3. Gunakan **|** operator atau metode **union** untuk operasi union :

   ```
   print(s5 | s6)
   print(s5.union(s6))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   {1, 2, 3, 4, 5, 6}
   {1, 2, 3, 4, 5, 6}
   ```

4. Sekarang gunakan operator **&** atau metode **intersection** untuk operasi intersection :

   ```
   print(s5 & s6)
   print(s5.intersection(s6))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   {3, 4}
   {3, 4}
   ```

5. Gunakan operator **-** atau metode **difference** untuk menemukan perbedaan antara dua set:

   ```
   print(s5 - s6)
   print(s5.difference(s6))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   {1, 2}
   {1, 2}
   ```

6. Sekarang masukkan operator **<=**  atau metode **issubset** untuk memeriksa apakah satu set adalah subset dari yang lain:

   ```
   print(s5 <= s6)
   print(s5.issubset(s6))
   s7 = {1,2,3}
   s8 = {1,2,3,4,5}
   print(s7 <= s8)
   print(s7.issubset(s8))
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   False
   False
   True
   True
   ```

   Dua pernyataan pertama akan mengembalikan **false** karena **s5** bukan bagian dari **s6**. Dua pernyataan terakhir akan mengembalikan **True** karena **s5** adalah bagian dari **s6**. Perhatikan bahwa operator **<=** adalah tes untuk subset. Subset yang tepat sama dengan subset umum, hanya saja set tersebut tidak boleh identik. Kita dapat mencobanya di sel baru dengan kode berikut.

7. Periksa apakah **s7** adalah subset formal dari **s8**, dan periksa apakah sebuah set dapat menjadi subset yang tepat dari dirinya sendiri dengan memasukkan kode berikut:

   ```
   print(s7 < s8)
   s9 = {1,2,3}
   s10 = {1,2,3}
   print(s9 < s10)
   print(s9 < s9)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   True
   False
   False
   ```

   Kita dapat melihat bahwa **s7** adalah subset yang tepat dari **s8** karena ada elemen lain di **s8** selain semua elemen **s7**. Tetapi **s9** bukanlah bagian dari **s10** karena keduanya identik. Oleh karena itu, sebuah himpunan bukanlah bagian dari dirinya sendiri.

8. Sekarang gunakan operator **>=** atau metode **issuperset** untuk memeriksa apakah satu set adalah superset dari set lainnya. Cobalah menggunakan kode berikut di sel lain:

   ```
   print(s8 >= s7)
   print(s8.issuperset(s7))
   print(s8 > s7)
   print(s8 > s8)
   ```

   Kita akan mendapatkan keluaran berikut:

   ```
   True
   True
   True
   False
   ```

   Tiga pernyataan pertama akan mengembalikan **True** karena **s8** adalah superset dari **s7** dan juga merupakan superset yang tepat dari **s7**. Pernyataan terakhir akan menghasilkan **false** karena tidak ada set yang bisa menjadi superset yang tepat untuk dirinya sendiri.





### Memilih Tipe Data

Sekarang, Kita telah mempelajari sebagian besar struktur data umum di Python. Salah satu tantangan yang mungkin kita hadapi adalah mengetahui kapan harus menggunakan berbagai tipe data.

Saat memilih jenis koleksi, sebaiknya pahami properti unik dari jenis tersebut. Misalnya, list bagi kita untuk menyimpan banyak objek dan mempertahankan urutan, kamus bagi kita untuk menyimpan pemetaan pasangan nilai kunci unik, tupel tidak dapat diubah, dan set hanya menyimpan elemen unik. Memilih tipe data yang tepat untuk kumpulan data tertentu dapat berarti peningkatan efisiensi atau keamanan.

Memilih tipe data yang salah untuk data kita akan menyebabkan hilangnya data, dalam banyak kasus hal itu menyebabkan efisiensi yang rendah saat menjalankan kode kita, dan dalam kasus terburuk, kita mungkin kehilangan data kita.





### Kesimpulan

Untuk meringkas, kita perlu ingat bahwa struktur data Python mencakup list, tupel, kamus, dan set. Python menyediakan struktur ini untuk memungkinkan kita membuat kode dengan lebih baik sebagai developer. Dalam sesi ini, kita telah membahas list, yang merupakan salah satu tipe data penting dalam Python yang menyimpan banyak objek, dan juga tipe data lainnya, seperti kamus, tupel, dan set. Masing-masing tipe data ini membantu kita menyimpan dan mengambil data secara efektif.

Struktur data adalah bagian penting dari semua bahasa pemrograman. Sebagian besar bahasa pemrograman hanya menyediakan tipe data dasar untuk menyimpan berbagai jenis angka, string, dan Boolean, seperti yang kita pelajari di sesi 1, Python Vital - Matematika, String, Kondisional, dan Loop. Mereka adalah bagian penting dari program apa pun. Dalam sesi ini, kita telah mempelajari cara memanfaatkan struktur data tingkat lanjut seperti nested list dan tipe data mixed, dan list dengan kamus - struktur yang bisa kita gunakan untuk menyimpan data kompleks.

Selanjutnya, kita akan belajar bagaimana menggunakan fungsi untuk menulis kode modular dan dapat dimengerti.