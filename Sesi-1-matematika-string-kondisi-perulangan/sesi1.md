

## Sesi 1 : Matematika, String, Kondisi, dan Perulangan.

[TOC]

#### Angka : Operasi, Tipe, dan Variabel

Setelah kita menginstall Anaconda, yang termasuk dengan Python dan Jupyter Notebook. Sekarang saatnya menjalankan Jupyter Notebook.





**Cara menjalankan Jupyter Notebook**

Ikuti langkah berikut :

1. Buka Anaconda Navigator

2. Cari **Jupyter** Notebook di Anaconda Navigator dan klik Launch.

3. Jendela Windows baru akan mengarahkan ke Web Browser.

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\1.png" style="zoom:50%;" />







##### Python sebagai Kalkulator

Python adalah kalkulator yang powerful. Dengan memanfaatkan library **math**, **numpy**, dan **scipy**. Di sesi lain, kita akan mempelajari cara menggunakan library numpy dan scipy. Untuk saat ini, kita akan memperlajari sebagai kalkulator yang digunakan kebanyakan orang setiap hari.

**Penambahan**, **pengurangan**, **penggandaan**, **pembagian**, dan **eksponan** adalah operasi yang biasanya digunakan. Dalam ilmu komputer, operator **modulus** dan **integer division** juga sama pentingnya, jadi kita akan membahasnya di sini.

Operasi **modulus** adalah sisa hasil bagi dalam matematika. **Aritmatika modular** juga disebut **aritmatika jam**. Misalnya, dalam **mod5** yang merupakan modulus 5, kita menghitung 0,1,2,3,4,0,1,2,3,4,0,1 ... Seperti tangan sebuah jam.

Perbedaan antara pembagian dan pembagian integer bergantung pada bahasanya. Saat membagi integer 9 dengan integer 4, beberapa bahasa mengembalikannya dengan nilai 2, yang lainnya mengembalikan 2,25. Dalam kasus ini, Python akan mengembalikan 2.25.





###### Operasi Standar Matematika

Kita akan menggunakan operasi standar matematika dan simbol yang digunakan sebagai berikut :

![Operator Aritmatika](https://assets.kompasiana.com/items/album/2019/10/23/operatoraritmatika-5dafe87f097f3658401d7b83.jpg?t=o&v=700)
<div style="text-align:center">Sumber : Kompasiana</div>

Python menyediakan metode opsional dari library **math**, yaitu **math.pow()**, tetapi menggunakan simbol ** akan lebih mudah digunakan.





###### Operasi Matematika Dasar

Kita akan melakukan operasi matematika pada dua angka. Contoh berikut penggunaan angka 5 dan 2:

1. Kita menggunakan operator penjumlahan, **+** pada kode: 

   ```
   5 + 2
   ```

    

   Kita akan mendapatkan output sebagai berikut: 

   ```
   7 
   ```

   Kita bisa mencobanya di Jupyter, ketik kode pada kotak dan pilih klik **Run**. Contoh pada Jupyter :

   ![](D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\2.png)

2. Kita dapat melakukan pengurangan pada dua angka: 

   ```
   5 - 2
   ```

   Kita akan mendapatkan output sebagai berikut: 

   ```
   3
   ```

3. Menggunakan operator perkalian ***** untuk mengalikan dua bilangan sebagai berikut: 

   ```
   5 * 2 
   ```

   Kita akan mendapatkan output sebagai berikut: 

   ```
   10
   ```

4. Sekarang, menggunakan operator **/** dan amati outputnya: 

   ```
   5 / 2 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   2.5 
   ```

   Saat membagi dua angka, Python akan selalu mengembalikan nilai desimal.

5. Sekarang pembagian yang sama dapat dilakukan dengan menggunakan **//** operator, yang disebut pembagian integer. Perhatikan perubahan pada output: 

   ```
   5 // 2
   ```

   Kita akan mendapatkan output berikut: 

   ```
   2 
   ```

   Hasil dari pembagian integer adalah integer sebelum koma desimal atau tanpa koma.

6. Sekarang, dengan menggunakan operator eksponensial ****** , kita dapat melakukan eksponensial: 

   ```
   5 ** 2 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   25
   ```

7. Terakhir, menggunakan operator modulus dalam kode dan amati outputnya: 

   ```
   5 % 2
   ```

   Kita akan mendapatkan output berikut: 

   ```
   1
   ```

   Operator modulus dilakukan dengan menggunakan operator **%**. Mengembalikan sisanya angka pembagian angka pertama dan kedua.

   
   
   

###### Operator Berurut

Tanda kurung berarti dalam Python. Dalam halnya komputasi, Python selalu menghitung apa yang ada di dalam tanda kurung terlebih dahulu. Bahasa Python mengikuti urutan operasi yang sama seperti di dunia matematika.

Perhatikan operasi berikut :  **5 + 2 * -3**

Yang perlu diperhatikan adalah bahwa tanda negatif dan tanda pengurangan itu sama di Python. Mari kita lihat contoh berikut :

1. Python pertama kali akan mengalikan **2** dan **–3**, lalu menambahkan **5** :

  ```
  5 + 2 * -3
  ```

  Kita akan mendapatkan output berikut:

  ```
  –1
  ```

2. Jika tanda kurung ditempatkan di sekitar angka 5 dan 2, kita mendapatkan hasil yang berbeda:

  ```
  (5 + 2) * -3
  ```

  Kita akan mendapatkan output berikut:

  ```
  –21
  ```

Jika ragu, gunakan tanda kurung. Tanda kurung sangat membantu untuk operasi kompleks, dan tanda kurung tambahan tidak akan memengaruhi kode.



###### Latihan 1 : Mengenal Urutan Operasi

Tujuan dari latihan ini adalah mengasah operasi matematika dalam Python dan memahami urutan eksekusi matematika.

1. Kurangi **100** dengan **5 pangkat 3** dan bagi hasilnya dengan **5**:

  ```
  (100 - 5 ** 3) / 5
  ```

  Kita akan mendapatkan output berikut:

  ```
  –5.0
  ```

2. Tambahkan **6** ke sisa **15** dibagi **4**:

  ```
  6 + 15 % 4
  ```

  Kita akan mendapatkan output berikut:

  ```
  9
  ```

3. Tambahkan **2 pangkat 2** dengan pembagian bilangan bulat dari **24** dan **4**:

  ```
  2 ** 2 + 24 // 4
  ```

  Kita akan mendapatkan output berikut:

  ```
  10
  ```



###### Spasi dalam Python

Kita mungkin bertanya-tanya tentang spasi di antara angka dan simbol. Dalam Python, spasi setelah angka atau simbol tidak memiliki arti apa pun. Spasi dimaksudkan untuk meningkatkan keterbacaan. 

Jika kita mengembangkan kebiasaan baik sejak awal, itu akan membuat pembacaan dan debugging kode menjadi lebih mudah.



###### Tipe Angka : Integer dan Float

Sekarang kita akan membahas perbedaan antara integer dan float. Pertimbangkan 8 dan 8.0. Kita tahu bahwa 8 dan 8.0 setara secara matematis. Keduanya mewakili nomor yang sama, tetapi jenisnya berbeda. 8 adalah bilangan bulat, dan 8.0 adalah desimal atau float.

Integer dalam Python diklasifikasikan sebagai jenis **int**, kependekan dari integer. Bilangan bulat mencakup semua bilangan bulat positif dan negatif, termasuk 0. Contoh bilangan bulat meliputi 3, -2, 47, dan 10000.

Float sebaliknya, tipe Python yang direpresentasikan sebagai desimal. Semua bilangan rasional yang dinyatakan sebagai pecahan dapat direpresentasikan sebagai float. Contoh float : 3.0, -2.0, 47.45, dan 200.001.

Untuk mengetahui tipe data pada python, dapat menggunakan **type()** .



###### Latihan 2 : Integer dan Float

Tujuan dari latihan ini adalah untuk menentukan tipe data dan kemudian mengubah tipe tersebut di Python.

1. Mulailah dengan menentukan tipe data **6** secara eksplisit menggunakan kode berikut:

  ```
  type(6)
  ```

  Kita akan mendapatkan output berikut:

  ```
  int
  ```

2. Sekarang, masukkan **type(6.0)** di sel berikutnya :

  ```
  type(6.0)
  ```

  Kita akan mendapatkan output berikut:

  ```
  float
  ```

3. Sekarang, tambahkan **5** dengan **3.14**. Jenis penjumlahannya:

  ```
  5 + 3.14
  ```

  Kita akan mendapatkan output berikut:

  ```
  8.14
  ```

  Jelas dari output yang menggabungkan **int** dan **float** memberi kita tipe data **float**. Jika Python mengembalikan nilai 8, kita akan kehilangan informasi.  

  Namun, kita dapat mengubah tipe dengan menggunakan kata kunci tipe datanya.

4. Sekarang, ubah **7.999999999** menjadi **int**:

   ```
   int(7.999999999)
   ```

   Kita akan mendapatkan output berikut:

   ```
   7
   ```

5. Ubah **6** menjadi **float**: 

   ```
   float(6) 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   6.0
   ```



###### Jenis Bilangan Kompleks

Python menyertakan bilangan kompleks sebagai tipe data. Bilangan kompleks muncul saat mengambil akar kuadrat dari bilangan negatif. Tidak ada bilangan real yang akar kuadratnya -9, jadi kita katakan itu sama dengan 3i. Contoh lain dari bilangan kompleks adalah 2i + 3. Python menggunakan **j**, bukan **i**.

Kita dapat melihat potongan kode berikut untuk mempelajari cara bekerja dengan tipe bilangan kompleks.

Bagilah **2 + 3j** dengan **1 - 5j**, masukkan kedua operasi dalam tanda kurung:

```
(2 + 3j) / (1 - 5j) 
```

Kita akan mendapatkan output berikut: 

```
–0.5+0.5j 
```

Untuk informasi lebih lanjut tentang bilangan kompleks, bisa di cek ke [https://docs.python.org/3/library/cmath.html](https://docs.python.org/3/library/cmath.html) .



###### Error dalam Python

Dalam pemrograman,  tidak perlu ditakuti error. Error umum tidak hanya untuk pemula tetapi untuk semua developer. Untuk saat ini, jika kita mendapatkan error, kita bisa coba lagi. Error Python di Notebook Jupyter tidak akan merusak komputer kita atau menyebabkan masalah serius.



###### Variabel

Di Python, variabel adalah slot memori yang dapat menyimpan elemen jenis apa pun. Nama variabel dimaksudkan untuk menjadi sugestif, karena gagasan di balik variabel bahwa nilainya dapat bervariasi di seluruh program tertentu.



###### Variabel Khusus

Dalam Python, variabel diperkenalkan dengan cara yang sama seperti dalam matematika, dengan menggunakan tanda sama dengan. Namun, dalam sebagian besar bahasa pemrograman, x = 3.14 berarti bahwa nilai 3.14 di masukan ke variabel x. Namun, 3,14 = x akan menghasilkan error karena tidak mungkin untuk menetapkan variabel ke angka. 



###### Latihan 3 : Menetapkan Variabel

Tujuan dari latihan ini adalah untuk memberikan nilai pada variabel. Variabel dapat diberi nilai apa pun, seperti yang akan kita lihat dalam latihan ini.

1. Tetapkan x sama dengan angka **2** : 

   ```
   x = 2
   ```

   Kita menetapkan nilai 2 ke variabel x.

2. Tambahkan **1** ke variabel **x** :

  ```
  x + 1
  ```

  Kita akan mendapatkan output berikut:

  ```
  3
  ```

  Setelah kita menambahkan **1** ke **x**, kita mendapatkan output **3**, karena variabel tersebut telah ditambahkan nilai **1**.


3. Ubah **x** menjadi **3.0** dan tambahkan **1** ke **x**:

  ```
  x = 3,0 
  x + 1
  ```

  Kita akan mendapatkan output berikut:

  ```
  4.0
  ```

  Pada langkah ini, kita mengubah nilai **x** menjadi **4.0**, dan seperti pada 2 langkah sebelumnya, kita akan menambahkan **1** ke variabel **x**.


###### Mengubah Tipe Data

Dalam beberapa bahasa, variabel tidak mungkin berubah jenis. Artinya jika variabel **y** adalah bilangan bulat, maka y akan selalu berupa bilangan bulat. Python, diketik secara dinamis, seperti yang kita lihat di Latihan 3, Menetapkan Variabel dan seperti yang diilustrasikan dalam contoh berikut:

1. **y** dimulai sebagai integer:

  ```
  y = 10
  ```

2. **y** menjadi pelampung:

  ```
  y = y - 10.0
  ```

3. Periksa tipe **y**: 

  ```
  type(y)
  ```

  Kita akan mendapatkan output berikut: 

  ```
  float
  ```

  Di topik berikutnya, kita akan melihat pemberian tipe data berbeda pada variabel.

  

###### Menetapkan Ulang Variabel dengan Ketentuan Sendiri

Biasanya dalam pemrograman untuk menambahkan 1 ke variabe seperti ini, **x = x + 1**. Dapat di singkat menggunakan **+=** seperti pada contoh berikut:

```
x += 1
```

Jadi, jika **x** sebelumnya **6**, **x** yg sekarang adalah **7**. Operator **+=** menambahkan bilangan di sebelah kanan ke variabel dan menetapkan variabel sama dengan bilangan baru.



###### Kegiatan 1 : Menetapkan Nilai ke Variabel

Dalam kegiatan ini, kita akan menetapkan angka ke variabel x, menambah angka, dan melakukan operasi tambahan.

Dengan menyelesaikan aktivitas ini, kita akan belajar bagaimana melakukan beberapa operasi matematika menggunakan Python.

Langkah-langkahnya sebagai berikut:
1. Pertama, masukkan 14 ke variabel x.
2. Sekarang, tambahkan 1 ke x.
3. Terakhir, bagi x dengan 5 dan kuadratkan.

Kita akan mendapatkan output berikut: 

```
9.0
```



###### Nama Variabel

Untuk menghindari kebingungan, disarankan untuk menggunakan nama variabel yang masuk akal bagi pembaca. Alih-alih menggunakan **x**, variabel yang mungkin dipakai ke **pendapatan** atau **usia**. Meskipun **x** lebih pendek, orang lain yang membaca kode itu mungkin tidak mengerti apa yang dimaksud **x**. Coba gunakan nama variabel yang menunjukkan artinya.

Ada beberapa batasan saat menamai variabel. Misalnya, variabel tidak boleh dimulai dengan angka, sebagian besar karakter khusus, kata kunci, atau tipe bawaan. Variabel juga tidak boleh berisi spasi di antara huruf.

Menurut konvensi Python, yang terbaik menggunakan huruf kecil dan menghindari karakter khusus yg sama karena akan sering menyebabkan error.

Kata kunci (keyword) Python disediakan dalam bahasa Python. Keyword memiliki arti khusus. Kita akan membahas sebagian besar kata kunci ini nanti.

Menjalankan dua baris berikut selalu menampilkan daftar kata kunci (keyword) Python saat ini :

```
import keyword 
print(keyword.kwlist)
```

Kita akan mendapatkan output berikut: 

![](D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\3.png)



###### Latihan 4 : Nama Variabel

Tujuan dari latihan ini adalah untuk mempelajari cara standar menamai variabel dengan mempertimbangkan praktik yang baik dan buruk.

1. Buat variabel bernama **1_angka** dan tetapkan nilainya adalah **1** : 

  ```
  1_angka = 1
  ```


  Kita akan mendapatkan output berikut :

<img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\4.png" style="zoom: 80%;" />

Kita akan mendapatkan error yang seperti pada gambar sebelumnya karena kita tidak dapat memulai variabel dengan angka.

2. Sekarang, mari coba menggunakan huruf untuk memulai variabel: 

   ```
   bilangan_pertama = 1 
   ```

3. Sekarang, gunakan karakter khusus dalam nama variabel, seperti pada kode berikut: 

   ```
   uang_$ = 1000.00 
   ```

   Kita akan mendapatkan output berikut:

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\5.png" style="zoom:80%;" />

Kita mendapatkan error yang disebutkan pada gambar di atas karena kita tidak dapat menyertakan variabel dengan karakter khusus.

4. Sekarang, gunakan lagi huruf daripada karakter biasa untuk nama variabel: 

   ```
   uang_ku = 1000.00
   ```

   

###### Variabel Lebih dari Satu

Kebanyakan program berisi variabel lebih dari satu. Aturan yang sama berlaku seperti saat dengan variabel tunggal. Kita akan berlatih dengan variabel lebih dari satu.



###### Latihan 5 : Banyak Variabel dengan Python

Dalam latihan ini, Kita akan melakukan operasi matematika menggunakan lebih dari satu variabel.

1. Tetapkan **5** ke **x** dan **2** ke **y**: 

   ```
   x = 5 
   y = 2 
   ```

2. Tambahkan **x** ke **x** dan kurangi **y** dengan pangkat dua : 

   ```
   x + x - y ** 2 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   6 
   ```

   Python memiliki banyak pintasan keren, dan beberapa tugas variabel adalah salah satunya. Inilah cara Pythonic untuk mendeklarasikan dua variabel.

3. Tetapkan **8** ke **x** dan **5** ke **y** dalam satu baris:

   ```
   x, y = 8, 5
   ```

4. Temukan pembagian bilangan bulat dari x dan y:

    ```
x // y
    ```

    Kita akan mendapatkan output berikut:
    
    ```
    1
    ```
    
    

###### Komentar

Komentar adalah blok kode tambahan yang tidak berjalan. Mereka dimaksudkan untuk mengklarifikasi kode bagi pembaca. Di Python, teks apa pun yang mengikuti simbol # pada satu baris adalah komentar.



###### Latihan 6 : Komentar di Python

Dalam latihan ini, Kita akan mempelajari dua cara berbeda untuk menampilkan komentar dengan Python.

1. Tulis komentar yang menyatakan **Ini adalah komentar**: 

   ```
   # Ini adalah komentar 
   ```

   Ketika kita menjalankan sel ini, tidak ada yang terjadi.

2. Atur variabel **pi** sama dengan **3,14**. Tambahkan komentar di atas baris : 

   ```
   # Atur variabel pi sama dengan 3.14
   pi = 3.14 
   ```

3. Sekarang, coba atur variabel **pi** sama dengan **3.14** lagi, tetapi tambahkan komentar pada baris yang sama: 

   ```
   pi = 3.14 # Atur variabel pi sama dengan 3.14 
   ```

   Meskipun kurang umum untuk memberikan komentar pada baris yang sama namun dapat diterima dan seringkali digunakan.



###### Docstrings

Docstrings, kependekan dari documen string, menyatakan apa yang sebenarnya dilakukan oleh dokumen tertentu, seperti program, fungsi, atau kelas. Perbedaan utama dalam sintaksis antara docstring dan komentar adalah bahwa docstring dimaksudkan untuk ditulis dalam beberapa baris, yang dapat diselesaikan dengan tanda kutip tiga " " ". Mereka juga memperkenalkan dokumen tertentu, sehingga ditempatkan di bagian atas koding.

Contoh docstrings :

```
"""
Dokumen ini akan menjelaskan mengapa komentar sangat berguna saat menulis dan membaca kode.
"""
```

Saat kita menjalankan sel ini, tidak ada yang terjadi. Docstrings, seperti komentar, dirancang sebagai informasi bagi pengembang yang membaca dan menulis kode; mereka tidak ada hubungannya dengan output.



###### Kegiatan 2 : Menemukan Solusi Menggunakan Teorema Pythagoras dengan Python

Dalam kegiatan ini, kita akan menentukan jarak Pythagoras antara tiga titik. Kita akan menggunakan docstring dan komentar untuk memperjelas prosesnya. Dalam aktivitas ini, kita perlu menetapkan angka ke variabel **x**, **y**, dan **z**, mengkuadratkan variabel, dan mengambil akar kuadrat untuk mendapatkan jarak, sambil memberikan komentar di sepanjang jalan dan docstring untuk menjelaskan urutan langkah. 

Langkah-langkahnya adalah sebagai berikut:
1. Tulis dokumen yang menjelaskan apa yang terjadi.

2. Set **x**, **y**, dan **z** sama dengan **2**, **3**, dan **4**.

3. Tentukan jarak Pythagoras antara **x**, **y**, dan **z**.

4. Sertakan komentar untuk memperjelas setiap baris kode.

  Kita akan mendapatkan output berikut:

  ```
  5.385164807134504
  ```



##### Strings: Concatenation, Methods, dan input() 

Kita telah belajar bagaimana mengekspresikan angka, operasi, dan variabel. Bagaimana dengan kata-kata ? Dalam Python, apa pun yang berada di antara tanda kutip 'tunggal' atau "ganda" dianggap sebagai string. String biasanya digunakan untuk mengekspresikan kata-kata, tetapi memiliki banyak kegunaan lain, termasuk menampilkan informasi kepada pengguna dan mengambil informasi dari pengguna.

Contohnya termasuk 'halo', "halo", 'HELLoo00', '12345', dan 'karakter unik :! @ # $% ^ & * ('.

Di bagian ini, kita akan mendapatkan belajar dengan string dengan memeriksa metode string, penggabungan string, dan fungsi bawaan yang berguna termasuk **print()** dan **len()** dengan berbagai contoh.



###### String Syntax

Meskipun string dapat menggunakan tanda kutip tunggal atau ganda, string yang diberikan akan konsisten secara internal. Artinya, jika sebuah string dimulai dengan satu kutipan, maka harus diakhiri dengan satu kutipan. Hal yang sama berlaku untuk tanda kutip ganda.



###### Latihan 7 : String Error Syntax

Tujuan dari latihan ini adalah untuk mempelajari syntax string yang sesuai :

1. Buka Jupyter Notebook.

2. Masukkan string yang valid:

  ```
  tokobuku = 'Gramedia'
  ```

3. Sekarang masukkan string yang tidak valid:

  ```
  tokobuku = 'Gramedia"
  ```

  Kita mendapatkan output berikut :

<img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\5a.png" style="zoom:67%;" />

Jika kita memulai dengan satu kutipan, harus diakhiri dengan satu kutipan. Karena string belum selesai, kita menerima syntax error.

4. Sekarang Anda perlu memasukkan format string yang valid lagi, seperti pada cuplikan kode berikut: 

   ```
   tokobuku = "Moe's"
   ```

   Tidak apa-apa. String dimulai dan diakhiri dengan tanda kutip ganda. Apa pun boleh di dalam tanda kutip, kecuali tanda kutip lainnya.

5. Sekarang tambahkan lagi string yang tidak valid: 

   ```
   tokobuku = 'Moe's'
   ```

   Kita mendapatkan output berikut :

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\7.png" style="zoom:67%;" />

Ini adalah sebuah masalah. Kita memulai dan mengakhiri dengan tanda kutip tunggal, lalu kita menambahkan tanda s dan tanda kutip tunggal lainnya.



Beberapa pertanyaan muncul. Yang pertama adalah apakah tanda kutip tunggal atau ganda harus digunakan. Jawabannya adalah itu tergantung pada preferensi pengembang. Kutipan ganda lebih tradisional, dan dapat digunakan untuk menghindari situasi yang berpotensi menimbulkan masalah seperti contoh **Moe** yang disebutkan di atas. 



Dalam latihan ini, kita telah mempelajari cara yang benar dan salah dalam menetapkan string ke variabel, termasuk tanda kutip tunggal dan ganda.



Python menggunakan karakter garis miring terbalik, \, yang disebut urutan escape dalam string, untuk memungkinkan penyisipan semua jenis kutipan di dalam string. Karakter yang mengikuti garis miring terbalik dalam urutan escape dapat ditafsirkan seperti yang disebutkan dalam dokumentasi resmi Python, yang mengikuti. Catatan khusus adalah \n, yang digunakan untuk membuat baris baru:

<img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\8.png" style="zoom: 50%;" />

<div style="text-align:center">Sumber : Medium - Raka Flyhigh A.</div>



###### Escape Sequence dengan Tanda Kutip

Berikut adalah cara kerja escape sequence dengan tanda kutip. Garis miring terbalik menimpa kutipan tunggal sebagai kutipan akhir dan memungkinkannya untuk diinterpretasikan sebagai karakter string :

```
tokobuku = 'Moe\'s'
```



###### String Lebih dari Satu Baris

String pendek selalu ditampilkan dengan baik, tetapi bagaimana dengan string yang barisnya lebih dari satu ? Ini bisa menjadi rumit untuk mendefinisikan variabel paragraf yang menyertakan string di beberapa baris. Di beberapa IDE, string mungkin keluar dari layar, dan mungkin sulit dibaca. Selain itu, mungkin menguntungkan untuk memiliki jeda baris pada titik-titik tertentu bagi pengguna.

Ketika string perlu menjangkau banyak baris, Python memberikan tanda kutip tiga, menggunakan tanda kutip tunggal atau ganda, sebagai opsi yang bagus. Berikut adalah contoh tanda kutip tiga ( ''' ) yang digunakan untuk menulis string banyak baris:

```
catatan_liburan = '''
Selama liburan ke Jakarta, kami menunggu dalam antrean panjang di Stasiun Gambir untuk naik kereta. Pada saat kereta kami tiba, kami mulai mencari online tempat makan yang enak. Kami sedang menuju ke Pantai Utara. 
'''
```



###### Fungsi print()

Fungsi **print()** digunakan untuk menampilkan informasi kepada pengguna, atau developer. Ini adalah salah satu fungsi bawaan Python yang paling banyak digunakan.



###### Latihan 8 : Menampilkan String

Dalam latihan ini, kita akan mempelajari berbagai cara untuk menampilkan string :

1. Buka Notebook Jupyter baru.

2. Tentukan variabel salam dengan nilai 'Halo'. Tampilkan salam menggunakan fungsi **print()** :

   ```
   salam = 'Halo'
   print(salam)
   ```

   Kita mendapatkan output berikut :

   ```
   Halo
   ```

   **Halo**, seperti yang ditunjukkan di layar, tidak termasuk tanda kutip tunggal. Ini karena fungsi **print()** umumnya ditujukan bagi user untuk mencetak output.

3. Tampilkan nilai **salam** tanpa menggunakan fungsi **print()**: 

   ```
   salam 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   'Halo' 
   ```

   Saat kita memasukkan **salam** tanpa fungsi **print()**, kita mendapatkan nilai yang dikodekan, karenanya tanda kutip. 

4. Pertimbangkan urutan kode berikut dalam satu sel di Notebook Jupyter :

   ```
   salam_ spanyol = 'Hola.'
   salam_ spanyol
   salam_ arab = 'Ahlan wa sahlan.'
   ```

   Ketika sel sebelumnya dijalankan, kode sebelumnya tidak menampilkan **salam_spanyol**. Jika kode dijalankan pada terminal sebagai tiga baris terpisah, maka akan menampilkan **Hola.**, String yang ditetapkan ke **salam_spanyol**. Hal yang sama juga berlaku jika urutan kode sebelumnya dijalankan dalam tiga sel terpisah di Notebook Jupyter. Agar konsistensi, berguna untuk menggunakan **print()** setiap kali informasi harus ditampilkan.

5. Tampilkan salam bahasa Spanyol:

  ```
  salam_spanyol = 'Hola.'
  cetak(salam_spanyol)
  ```

  Kita harus mendapatkan output berikut:

  ```
  Halo.
  ```

6. Sekarang, tampilkan pesan ucapan bahasa Arab, seperti yang disebutkan dalam potongan kode berikut: 

   ```
   arabic_greeting = 'Ahlan wa sahlan.' 
   print (arabic_greeting) 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   Ahlan wa sahlan. 
   ```

   Compiler menjalankan setiap baris secara berurutan. Setiap kali tiba di print(), maka akan menampilkan informasi.



###### Operasi String dan Concatenation

Operator perkalian dan penjumlahan bisa dijalankan dengan string. Secara khusus, operator + menggabungkan dua string menjadi satu dan disebut sebagai penggabungan string. Operator *, untuk perkalian, mengulang sebuah string. Dalam latihan berikut, Anda akan melihat rangkaian string dalam sampel string kami.



###### Latihan 9 : Concatenation String 

Dalam latihan ini, kita akan belajar cara menggabungkan string menggunakan concatenation string:

1. Buka Notebook Jupyter baru.

2. Gabungkan **salam_spanyol** yang kita gunakan dalam Latihan 8, Tampilkan String, dengan tambahan 'Senor.' menggunakan operator **+** dan tampilkan hasilnya: 

  ```
  salam_spanyol = 'Hola'
  print(salam_spanyol + 'Senor.')
  ```

  Kita akan mendapatkan output berikut:

  ```
  HolaSenor.
  ```

  Perhatikan bahwa tidak ada spasi antara **salam** dan nama. Jika kita menginginkan spasi antar string, kita perlu menambahkannya secara eksplisit.

3. Sekarang, gabungkan **salam_spanyol** dengan 'Senor.' menggunakan operator **+**, tapi kali ini, masukkan spasi:

  ```
  salam_spanyol = 'Hola '
  print(salam_spanyol + 'Senor.')
  ```

  Kita akan mendapatkan output berikut:

  ```
  Hola Senor.
  ```

4. Tampilkan salam 5 kali menggunakan ***** operator perkalian:

  ```
  salam = 'Halo' 
  print(salam * 5)
  ```

  Kita akan mendapatkan output berikut:

  ```
  HaloHaloHaloHaloHalo
  ```



##### Interpolasi String 

Saat menulis string, kita mungkin ingin memasukkan variabel ke dalam output. Interpolasi string menyertakan nama variabel sebagai placeholder di dalam string. Ada dua metode standar untuk mencapai interpolasi string: **koma pemisah** dan **format**.

###### Koma Pemisah

Variabel dapat diinterpolasi menjadi string menggunakan koma untuk memisahkan klausa. Ini mirip dengan operator **+**, kecuali kita menambahkan spasi. 

Kita dapat melihat contoh di sini, di mana kita menambahkan **Ciao** dalam fungsi **print** : 

```
salam_itali = 'Ciao' 
print('Haruskah kita menyapa orang dengan', salam_itali, 'di Pantai Utara ?') 
```

Kita akan mendapatkan output berikut: 

```
Haruskah kita menyapa orang dengan Ciao di Pantai Utara?
```



###### Format

Dengan **format**, seperti koma, tipe data Python, **int**, **float**, dan sebagainya, diubah menjadi string saat dieksekusi. **Format**diakses menggunakan tanda kurung dan notasi titik :

```
pemilik = 'Iqbal Ahdagita Elbadra'
umur = 25
print('Founder toko buku Cupiz, {}, sekarang berumur {} tahun.'.format(pemilik, umur))
```

Kita akan mendapatkan output berikut: 

```
Founder toko buku Cupiz, Iqbal Ahdagita Elbadra, sekarang berumur 25 tahun.
```

Cara kerja **Format** sebagai berikut: Pertama, tentukan variabel. Selanjutnya, dalam string yang diberikan, gunakan **{}** sebagai pengganti setiap variabel. Di akhir string, tambahkan titik (.) Diikuti dengan kata kunci **format**. Kemudian, dalam tanda kurung, masukkan setiap variabel dalam urutan tampilan yang diinginkan. Di bagian selanjutnya, kita akan melihat fungsi string bawaan yang tersedia untuk developer Python.



###### Fungsi len()

Ada banyak fungsi bawaan yang sangat berguna untuk string. Salah satu fungsi tersebut adalah **len()**, yang merupakan kependekan dari length. Fungsi **len()** menentukan jumlah karakter dalam string tertentu.

Perhatikan bahwa fungsi len() juga akan menghitung spasi kosong dalam string tertentu.

Kita akan menggunakan variabel **salam_arab** yang digunakan pada Latihan 8, Tampilkan String:

```
len(salam_arab)
```

Kita akan mendapatkan output berikut:

```
16
```



###### String Methods

Semua tipe data Python, termasuk string, memiliki metodenya sendiri. Metode ini umumnya menyediakan pintasan untuk mengimplementasikan tugas yang berguna. Metode dalam Python, seperti dalam banyak bahasa lainnya, diakses melalui notasi titik. 

Kita dapat menggunakan variabel baru, **name**, untuk mengakses berbagai metode. Kita dapat melihat semua metode dengan menekan tombol Tab setelah variabel **name** dan titik.



###### Latihan 10 : Method String

Dalam latihan ini, Kita akan belajar bagaimana mengimplementasikan method string.

1. Tetapkan variabel baru, bernama **name**, ke nama apa pun yang kalian mau :

  ```
  name = 'Iqbal'
  ```

2. Sekarang, ubah nama menjadi huruf kecil menggunakan fungsi **lower()**: 

   ```
   name.lower() 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   'iqbal'
   ```

3. Sekarang, kapitalisasi nama menggunakan fungsi **capitalize()**: .

   ```
   name.capitalize()
   ```

   Kita akan mendapatkan output berikut: 

   ```
   'Iqbal' 
   ```

4. Ubah nama menjadi huruf besar menggunakan **upper()**: 

   ```
   name.upper() 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   'IQBAL' 
   ```

5. Terakhir, hitung jumlah **a** dalam kata **'Iqbal'**: 

   ```
   name.count('a') 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   1
   ```

   

###### Casting

Biasanya bilangan dinyatakan sebagai string saat berhadapan dengan input dan output. Perhatikan bahwa **'5'** dan **5** adalah tipe yang berbeda. Kita dapat dengan mudah mengkonversi antara angka dan string menggunakan kata kunci jenis yang sesuai. Dalam latihan berikut, kita akan menggunakan tipe data dan casting untuk memahami konsep dengan lebih baik.



###### Latihan 11 :  Tipe Data dan Casting

Dalam latihan ini, Kita akan mempelajari bagaimana tipe data dan casting dapat bekerja secara bersamaan :

1. Buka Notebook Jupyter baru. 

2. Tentukan tipe **'5'**: 

   ```
   type('5') 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   str 
   ```

3. Sekarang, tambahkan '5' dan '7': 

   ```
   '5' + '7' 
   ```

   Kita akan mendapatkan output berikut : 

   ```
   '57' 
   ```

   Jawabannya bukan 12 karena, di sini, **5** dan **7** adalah tipe data **string**, bukan tipe data **int**. Ingatlah bahwa operator **+** menggabungkan string. Jika kita ingin menjumlahkan **5** dan **7**, kita harus mengkonversinya terlebih dahulu. 

4. Ubah string '5' menjadi **int** seperti berikut: 

   ```
   int('5') 
   ```

   Kita akan mendapatkan output berikut: 

   ```
   5
   ```

   Sekarang **5** adalah angka, sehingga dapat digabungkan dengan angka lain melalui operasi matematika. 

5. Tambahkan '5' dan '7' dengan mengubahnya menjadi **int** terlebih dahulu: 

   ```
   int ('5') + int ('7') 
   ```

   Kita akan mendapatkan output berikut:

   ```
   12
   ```

   

###### Fungsi input()

Fungsi **input()** adalah fungsi bawaan yang memungkinkan inputan dari pengguna. Ini sedikit berbeda dari yang telah kita lihat sejauh ini.



###### Latihan 12 : Fungsi input()

Dalam latihan ini, Kita akan menggunakan fungsi **input()** untuk mendapatkan informasi dari pengguna:

1. Buka Notebook Jupyter baru. 

2. Minta nama pengguna. Menanggapi dengan salam yang sesuai: 

   ```
   # Tanya pengguna siapa namanya
   print('Siapa namamu?') 
   ```

   Kita akan mendapatkan hasil sebagai berikut:

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\9.png" style="zoom:67%;" />

3. Sekarang, atur variabel yang akan sama dengan fungsi **input()**, seperti berikut: 

   ```
   name = input() 
   ```

   Kita akan mendapatkan output berikut:

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\10.png" style="zoom:67%;" />

4. Terakhir, pilih ouput yang sesuai: 

   ```
   print('Halo,' + name + '.') 
   ```

   Kita akan mendapatkan ouput berikut:

   <img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\11.png" style="zoom:67%;" />



###### Kegiatan 3 : Menggunakan Fungsi input() untuk Menilai Hari Mu

Dalam kegiatan ini, Kita perlu membuat tipe data input di mana kita meminta pengguna untuk menilai hari mereka pada skala 1 sampai 10. 

Dengan menggunakan fungsi **input()**, Kita akan meminta pengguna untuk memasukkan dan menanggapi dengan komentar termasuk dengan inputan. Dalam kegiatan ini, Kita akan mencetak pesan kepada pengguna yang meminta nomor. Kemudian, Kita akan menetapkan nomor ke variabel dan menggunakan variabel itu di pesan kedua yang kita tampilkan kepada pengguna. 

Langkah-langkahnya adalah sebagai berikut:

1. Buka Notebook Jupyter baru. 
2. Tampilkan pertanyaan yang meminta pengguna untuk menilai hari mereka pada skala angka **1** sampai **10**. 
3. Simpan masukan pengguna sebagai variabel. 
4. Tampilkan pernyataan kepada pengguna yang menyertakan nomor tersebut.



##### String Indexing dan Slicing 

**Indexing** dan **Slicing** adalah bagian penting dari pemrograman. Dalam analisis data, pengindeksan (indexing) dan pemotongan (slicing) DataFrames sangat penting untuk melacak baris dan kolom, sesuatu yang akan kita akan pelajari dengan pandas dan NumPy nanti. Mekanika di balik pengindeksan dan pemotongan dataFrames sama dengan pengindeksan dan pemotongan string, yang akan kita pelajari sekarang ini.



###### Indexing

Karakter string Python ada di lokasi tertentu; dengan kata lain, urutan mereka penting. Indeks adalah representasi numerik di mana setiap karakter berada. Karakter pertama ada di indeks 0, karakter kedua ada di indeks 1; karakter ketiga ada di indeks 2, dan seterusnya.

Perhatikan string berikut: 

```
destination = 'San Francisco' 
```

**'S'** ada di indeks ke-0, **'a'** ada di indeks pertama, **'n'** di indeks ke-2, dan seterusnya. Karakter dari setiap indeks diakses menggunakan notasi braket sebagai berikut: 

```
destination[0] 
```

Kita akan mendapatkan output berikut: 

```
'S' 
```

Untuk mengakses data dari indeks pertama, masukkan berikut ini: 

```
destination[1] 
```

Kita akan mendapatkan output berikut : 

```
'a' 
```

Untuk mengakses data dari indeks kedua, masukkan berikut ini: 

```
destination[2] 
```

Kita akan mendapatkan output berikut: 

```
'n'
```

Nilai karakter **San Francisco** dan hitungan indeks yang sesuai seperti tabel berikut:

```
+----------------+---+---+---+
| Nilai Karakter | S | a | n |  
+----------------+---+---+---+
| Indeks         | 0 | 1 | 2 |  
+----------------+---+---+---+
```

Sekarang, coba tambahkan **-1** sebagai nilai indeks dan amati outputnya : 

```
destination[-1] 
```

Kita akan mendapatkan output berikut: 

```
'o'
```

Untuk mengakses data dari belakang **San Francisco**, kita menggunakan tanda negatif dalam kasus ini **-2**: 

```
destination[-2] 
```

Kita akan mendapatkan output berikut: 

```
'c'
```

Karakter **sco** dari kata **Francisco**, dan jumlah indeks yang sesuai:

```
+----------------+---+---+---+
| Nilai Karakter | s | c | o |  
+----------------+---+---+---+
| Indeks         |-3 | -2| -1|  
+----------------+---+---+---+
```

Contoh lainnya :

```
bridge = 'Golden Gate' 
bridge[6]
```

Kita akan mendapatkan output berikut: 

```
' '
```

Kita mungkin bertanya-tanya apakah kita melakukan kesalahan karena tidak ada huruf yang ditampilkan. Sebaliknya, tidak masalah karena string kosong. Faktanya, string kosong adalah salah satu string paling umum dalam pemrograman.



##### Slicing

Slice adalah bagian dari string atau elemen lainnya. Irisan (slice) dapat berupa seluruh elemen atau satu karakter, tetapi lebih umum sekelompok karakter yang berdampingan.

Katakanlah kita ingin mengakses huruf kelima sampai kesebelas dari sebuah string. Jadi, kita mulai di indeks 4 dan berakhir di indeks 10, seperti yang dijelaskan di bagian Indexing sebelumnya. Saat slicing, simbol titik dua (:) disisipkan di antara indeks, seperti: [4:10].

Ada satu peringatan. Batas bawah potongan selalu disertakan, tetapi batas atasnya tidak. Jadi, pada contoh sebelumnya, jika kita ingin memasukkan indeks ke-10, kita harus menggunakan [4:11].

Kita sekarang akan melihat contoh berikut untuk slicing.

Ambil huruf kelima sampai kesebelas **San Francisco**, yang kita gunakan di bagian Indexing sebelumnya:

```
destination[4:11]
```

Kita akan mendapatkan output berikut:

```
'Francis'
```

Ambil tiga huruf pertama **destination**:

```
destination[0:3]
```

Kita akan mendapatkan output berikut:

```
'San'
```


Ada cara lain untuk mendapatkan n huruf pertama dari sebuah string. Jika karakter numerik pertama dihilangkan, Python akan mulai dari indeks ke-0.

Sekarang, untuk mengambil delapan huruf pertama **destination** menggunakan pintasan, gunakan kode berikut:

```
destination[:8]
```

Kita akan mendapatkan keluaran berikut:

```
'San Fran'
```

Terakhir, untuk mengambil tiga huruf **destination** terakhir, gunakan kode ini:

```
destination[-3:]
```


Kita akan mendapatkan keluaran berikut:

```
'sco'
```

Tanda negatif, **-**, berarti kita mulai dari huruf ketiga sampai terakhir, dan titik dua berarti paling akhir.



###### String dan Metodenya

Kita mulai dengan sintaks string, sebelum beralih ke berbagai cara untuk menggabungkan string. Kita melihat fungsi built-in yang berguna termasuk **len()** dan memeriksa contoh metode string. Selanjutnya, Anda memasukkan angka sebagai string dan sebaliknya.

Fungsi **input()** digunakan untuk mengakses input pengguna. Menanggapi umpan balik pengguna adalah elemen inti dari pemrograman yang akan terus kita kembangkan. Terakhir, kita menutup dengan dua alat canggih yang sering digunakan developer: indexing dan slicing.

Ada banyak hal yang perlu dipelajari tentang string.  Selanjutnya, Kita akan belajar cara mencabangkan program menggunakan Conditional dan Boolean.



##### Conditional dan Boolean

Boolean, diambil dari nama George Boole, mengambil nilai True atau False. Meskipun ide di balik Boolean agak sederhana, mereka membuat pemrograman menjadi jauh menarik. Saat menulis program, misalnya, ada baiknya mempertimbangkan banyak kasus. Jika kita meminta informasi kepada pengguna, kita mungkin ingin merespons secara berbeda tergantung pada jawaban pengguna. Misalnya, jika pengguna memberikan peringkat 0 atau 1, kita mungkin memberikan tanggapan yang berbeda dari peringkat 9 atau 10. Kata kuncinya di sini adalah **if**.

Pemrograman berdasarkan banyak kasus disebut sebagai percabangan. Setiap cabang diwakili oleh kondisi yang berbeda. Persyaratan sering kali dimulai dengan klausa **'if'**, diikuti dengan klausa **'else'**. Pilihan cabang ditentukan oleh Boolean, bergantung pada apakah kondisi yang diberikan adalah **True** atau **False**.



###### Booleans

Dalam Python, objek kelas Boolean diwakili oleh kata kunci **bool** dan memiliki nilai **True** atau **False**.



###### Latihan 13  : Variabel Boolean

Dalam latihan singkat ini, kita akan menggunakan, menetapkan, dan memeriksa tipe data variabel Boolean:

1. Buka Notebook Jupyter baru.

2. Sekarang, gunakan Boolean untuk mengklasifikasikan seseorang berusia di atas **18** tahun menggunakan kode berikut:

  ```
  over_18 = True
  type(over_18)
  ```

  Kita akan mendapatkan output berikut:

  ```
  bool
  ```


  Outputnya terpenuhi, dan tipenya disebut sebagai Boolean, yaitu **bool**.

3. Gunakan Boolean untuk mengklasifikasikan seseorang sebagai tidak berusia lebih dari **21**:

  ```
  over_21 = False
  type(over_21)
  ```

  Kita akan mendapatkan output berikut:

  ```
  bool
  ```


  Dalam latihan singkat dan cepat ini, kita telah belajar tentang tipe data **bool**, salah satu tipe terpenting Python.



###### Operator Logika 

Boolean dapat digabungkan dengan operator logika **and**, **or**, dan **not**. Misalnya, sebagai berikut:

A = True 

B = True 

Y = False 

Z = False

**Not** berarti bernilai negatif :

not A = False 

not Z = True. 

**And** hanya benar jika kedua proposisi benar. Jika tidak, maka salah:

A and B = True 

A and Y = False 

Y and Z = False 

**Or** benar jika salah satu proposisi benar. Jika tidak, maka salah:

A or B = True 

A or Y = True 

Y or Z = False 

Sekarang mari kita gunakan dalam contoh latihan berikut.

Tentukan apakah kondisi berikut ini **True** atau **False** mengingat **over_18 = True** dan **over_21 = False** :

• **over_18** and **over_21** 

• **over_18** or **over_21** 

• not **over_18** 

• not **over_21** or (**over_21** or **over_18**) 

1. Kita harus memasukkannya ke dalam kode dan pertama tetapkan **True** dan **False** ke **over_18** dan **over_21**:

   over_18, over_21 = True, False 

2. Selanjutnya kita dapat mengasumsikan individu tersebut **over_18** and **over_21**:

   ```
   over_18 and over_21 
   ```

   Kita akan mendapatkan output berikut:

   ```
   False
   ```

3. Kita sekarang menganggap individu tersebut **over_18** or **over_21**:

   ```
   over_18 or over_21 
   ```

   Kita akan mendapatkan output berikut:

   ```
   True
   ```

4. Sekarang kita menganggap individu tersebut not **over_18**:

   ```
   not over_18
   ```

    Kita akan mendapatkan output berikut:

   ```
   False
   ```

5. Kita menganggap individu tersebut not **over_21** or (**over_21** or **over_18**):

   ```
   not over_21 or (over_21 or over_18) 
   ```

   Kita akan mendapatkan output berikut:

   ```
   True
   ```



###### Operator Perbandingan

Objek Python dapat dibandingkan menggunakan berbagai simbol yang mengevaluasi Boolean.

Gambar berikut menunjukkan tabel perbandingan dengan operator yang sesuai:



<img src="D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\12.jpg" style="zoom:80%;" />

<div style="text-align:center">Sumber : galery-it.site</div>



###### Latihan 14 : Operator Perbandingan

Dalam latihan ini, kita akan berlatih menggunakan operator pembanding. Kita akan mulai dengan beberapa contoh matematika dasar:

1. Buka Notebook Jupyter baru.

2. Sekarang, tetapkan **usia** sama dengan **20** dan sertakan operator pembanding untuk memeriksa apakah **usia** kurang dari 13:

  ```
  usia = 20
  usia < 13
  ```

  Kita akan mendapatkan output berikut: 

  ```
  False
  ```

3. Dengan menggunakan cuplikan kode berikut, kita dapat memeriksa apakah **usia** lebih dari atau sama dengan **20** dan kurang dari atau sama dengan **21**:

  ```
  usia> = 20 and usia <= 21
  ```

  Kita akan mendapatkan output berikut: 

  ```
  True
  ```

4. Sekarang periksa apakah **usia** tidak sama dengan **21**:

  ```
  usia != 21
  ```

  Kita akan mendapatkan output berikut: 

  ```
  True
  ```

5. Sekarang, periksa apakah **usia** sama dengan **19**:

  ```
  usia == 19
  ```

  Kita akan mendapatkan output berikut: 

  ```
  False
  ```


  Tanda ganda sama dengan, atau operator yang setara, ==, sangat penting dalam Python. Ini memungkinkan kita untuk menentukan apakah dua objek itu sama. Kita sekarang dapat menjawab pertanyaan apakah 6 dan 6.0 sama dengan Python.

6. Apakah **6** setara dengan 6.0 di Python? :

     ```
     6 == 6.0
     ```


     Kita akan mendapatkan output berikut: 
    
     ```
     True
     ```
    
     **6** dan **6.0** adalah tipe yang berbeda, tetapi keduanya sama. Mengapa demikian?
    
     Karena **6** dan **6.0** sama secara matematis, masuk akal jika keduanya sama dalam Python, meskipun jenisnya berbeda. Pertimbangkan apakah 6 harus sama dengan 42/7. Jawaban matematisnya adalah ya. Python sering kali sesuai dengan prinsip matematika, bahkan dengan pembagian integer. Kita dapat menyimpulkan bahwa mungkin saja tipe data yang berbeda memiliki objek yang sama.

7. Sekarang cari tahu apakah **6** sama dengan string **'6'**:

  ```
  6 == '6'
  ```


  Kita akan mendapatkan output berikut:

  ```
  False
  ```

  Di sini, Kita menekankan bahwa tipe data yang berbeda biasanya tidak memiliki objek yang sama. Secara umum, ada baiknya untuk mentransmisikan objek sebagai tipe data yang sama sebelum menguji kesetaraan.
  Selanjutnya, mari kita cari tahu apakah seseorang berusia 20-an atau 30-an:

  ```
  (usia >= 20 and usia < 30) or (usia >= 30 and usia < 40)
  ```


  Kita akan mendapatkan output berikut:

  ```
  True
  ```

  Tanda kurung tidak diperlukan jika hanya ada satu kemungkinan interpretasi. Saat menggunakan lebih dari dua kondisi, tanda kurung biasanya merupakan ide yang bagus. Perhatikan bahwa tanda kurung selalu diizinkan. Berikut ini adalah pendekatan lain:

  ```
  (20 <= usia <30) atau (30 <= usia <40)
  ```


  Kita akan mendapatkan output berikut:

  ```
  True
  ```

  Meskipun tanda kurung di baris kode sebelumnya tidak sepenuhnya diperlukan, tapi membuat kode lebih mudah dibaca. Aturan praktis yang baik adalah menggunakan tanda kurung untuk kejelasan.



###### Membandingkan String

Apakah **'a' < 'c'** masuk akal? Bagaimana dengan **'New York' > 'San Francisco'**? Python menggunakan konvensi urutan abjad untuk memahami perbandingan ini. Pemikiran kamus : ketika membandingkan dua kata, kata yang muncul belakangan dalam kamus dianggap lebih besar dari kata yang muncul sebelumnya.



###### Latihan 15 : Membandingkan String

Dalam latihan ini, Kita akan membandingkan string menggunakan Python:

Dalam latihan ini, Anda akan membandingkan string menggunakan Python:
1. Buka Notebook Jupyter baru.

2. Mari bandingkan satu huruf:

  ```
  'a' < 'c'
  ```


  Kita akan mendapatkan output berikut:

  ```
  True
  ```

3. Sekarang, mari bandingkan 'New York' dan 'San Francisco':

  ```
  'New York' > 'San Francisco'
  ```


  Kita akan mendapatkan output berikut:

  ```
  False
  ```


  Ini **False** karena **'New York' < 'San Francisco'**. 'New York' tidak datang belakangan dalam kamus daripada 'San Francisco'.



###### Conditional

Conditional digunakan ketika kita ingin mengekspresikan kode berdasarkan serangkaian keadaan atau nilai. Kondisional mengevaluasi nilai Boolean atau ekspresi Boolean, dan biasanya diawali dengan **'if'**. 

Katakanlah kita sedang menulis program pemungutan suara, dan kita ingin mencetak sesuatu hanya jika pengguna berusia di bawah 18 tahun.



###### Syntax If

```
if usia < 18 :
print('Kamu belum cukup umur untuk memilih.')
```

Ada beberapa komponen kunci untuk suatu kondisi. 

Yang pertama adalah kata kunci **'if'**. Kebanyakan kondisional dimulai dengan klausa **if**. 

Bagian penting berikutnya adalah titik dua **:** . Titik dua menunjukkan bahwa klausa **if** telah selesai. Pada titik ini, kompilator memutuskan apakah kondisi sebelumnya adalah **True** atau **False**.

Secara sintaksis, semua yang mengikuti titik dua diberi indentasi.

Python menggunakan **indentasi**, bukan tanda kurung. Indentasi bisa menguntungkan saat berhadapan dengan kondisional bersarang (nested) karena menghindari notasi yang rumit. Identasi Python mempunyai ciri-ciri **empat spasi** dan biasanya bisa digunakan dengan menekan **Tab** pada keyboard kita. Garis indentasi hanya akan berjalan jika kondisi bernilai **True**. Jika kondisi bernilai **False**, baris berikutnya akan dilewati seluruhnya.



###### Indentasi

Indentasi adalah salah satu fitur tunggal Python. Indentasi digunakan di semua tempat dengan Python. Salah satu keuntungannya adalah jumlah penekanan tombol. Dibutuhkan satu penekanan tombol untuk tab, dan dua kali penekanan tombol untuk menyisipkan tanda kurung. Keuntungan lainnya adalah keterbacaan. Lebih jelas dan lebih mudah untuk membaca kode ketika semuanya berbagi indentasi yang sama, yang berarti blok kode memiliki cabang yang sama.

Salah satu potensi kekurangannya adalah banyak tab dapat menarik teks ke luar layar, tetapi ini jarang terjadi, dan biasanya dapat dihindari dengan kode yang elegan. Masalah lain, seperti membuat indentasi atau menghapus beberapa baris, dapat ditangani melalui shortcut. Pilih semua teks dan tekan **Tab** untuk membuat indentasi. Pilih semua teks dan tekan **Shift + Tab** untuk membatalkan indentasi.



###### Latihan 16 : Menggunakan Sintaks if

Dalam latihan ini, kita akan menggunakan kondisional menggunakan klausa **if** :

1. Buka Notebook Jupyter baru.

2. Sekarang, jalankan beberapa baris kode di mana kita menetapkan variabel **usia** dengan nilai **20** dan menambahkan klausa **if**, seperti yang disebutkan dalam cuplikan kode berikut:

  ```
  usia = 20
  if usia >= 18 and usia < 21 :
  	print('Setidaknya kita dapat memilih.')
  	print('Poker harus menunggu.')
  ```

  Kita akan mendapatkan output berikut:

  ```
  Setidaknya kita dapat memilih. 
  Poker harus menunggu.
  ```

  Tidak ada batasan jumlah pernyataan Indentasi. Setiap pernyataan akan berjalan secara berurutan, asalkan kondisi sebelumnya adalah **True**.

3. Sekarang, gunakan kondisional bersarang (nested) :

   ```
   if usia >= 18 :
       print('Kita bisa memilih.') 
       if usia >= 21 : 
   		print ('Kita bisa bermain poker.')
   ```

   Kita akan mendapatkan output berikut:

   ```
   Kita bisa memilih.
   ```

   Dalam hal ini, benar bahwa **usia >= 18**, jadi pernyataan pertama dicetak **Kita bisa memilih**. Kondisi kedua, **umur >= 21**, bagaimanapun, adalah false, sehingga pernyataan kedua tidak tercetak.



###### if else

Kondisional **if** biasanya digabungkan dengan klausa **else**. Contohnya adalah sebagai berikut. Katakanlah kita ingin mencetak semua pengguna kecuali pengguna berusia di bawah 18 tahun. Kitadapat mengatasinya dengan kondisional **if-else**. Jika pengguna kurang dari 18, Kita akan mencetak satu pernyataan. Jika tidak, Kita akan mencetak yang lain. Klausa sebaliknya diawali dengan **else**.



###### Latihan 17 : Menggunakan Sintaks if-else

Dalam latihan ini, kita akan mempelajari cara menggunakan kondisional yang memiliki dua opsi, satu **if**, dan satu lagi **else**:

1. Buka Notebook Jupyter baru.

2. Perkenalkan program pemungutan suara hanya untuk pengguna di atas 18 tahun dengan menggunakan cuplikan kode berikut:

  ```
  usia = 20
  if usia < 18:
  	print('Kamu belum cukup umur untuk memilih.')
  else:
  	print('Selamat datang di program pemungutan suara kami.')
  ```

  Kita akan mendapatkan output berikut:

  ```
  Selamat datang di program pemungutan suara kami.
  ```

3. Sekarang jalankan potongan kode berikut, yang merupakan alternatif dari kode yang disebutkan di langkah 2 latihan ini:

  ```
  if usia >= 18:
  	print('Selamat datang di program pemungutan suara kami.')
  else:
  	print('Kamu belum cukup umur untuk memilih.')
  ```


  Kita akan mendapatkan output berikut:

  ```
  Selamat datang di program pemungutan suara kami.
  ```

Dalam latihan ini, kita telah mempelajari cara menggunakan if-else bersama dengan loop.

Ada banyak cara untuk menulis program dengan Python. Yang satu belum tentu lebih baik dari yang lain. Mungkin menguntungkan untuk menulis program yang lebih cepat atau program yang lebih mudah dibaca.

Program adalah sekumpulan instruksi yang dijalankan oleh komputer untuk menyelesaikan tugas tertentu. Program bisa berupa satu baris kode, atau puluhan ribu. Kita akan mempelajari keterampilan dan teknik penting untuk menulis program Python,



###### Pernyataan elif

**elif** adalah kependekan dari **else if**. **elif** tidak memiliki arti dalam isolasi. elif muncul di antara klausa **if** dan **else**. Sebuah contoh harus membuat segalanya lebih jelas. Lihat cuplikan kode berikut dan salin ke notebook Jupyter. Penjelasan untuk kode ini disebutkan tepat setelah output (usia menggunakan nilai dari sebelumnya) :

```
if usia <= 10:
	print('Dengarkan, pelajari, dan bersenang-senanglah.')
elif usia <= 19:
	print('Maju tanpa rasa takut.')
elif usia <= 29:
	print('Rebut hari itu.')
elif usia <= 39:
	print('Lakukan apa yang kamu inginkan.')
elif usia <= 59:
	print('Tetap bugar dan sehat secara fisik.')
else:
	print ('Di setiap hari yang ajaib.')
```

Kita akan mendapatkan output berikut:

```
Rebut hari itu
```

Sekarang, mari kita uraikan kode untuk penjelasannya :

1. Baris pertama memeriksa **if** usia kurang dari atau sama dengan **10**. Karena kondisi ini false, maka cabang berikutnya diperiksa.
2. Cabang berikutnya adalah **elif** usia **<= 19**. Baris ini memeriksa apakah umur kurang dari atau sama dengan 19. Ini juga tidak benar, jadi kita pindah ke cabang berikutnya.
3. Cabang berikutnya adalah **elif** usia <= **29**. Hal ini berlaku karena **usia = 20**. Pernyataan indentasi yang mengikuti akan dicetak.
4. Setelah setiap cabang dijalankan, seluruh urutan dibatalkan, tidak ada cabang **elif** berikutnya atau cabang lain yang diperiksa.
5. Jika tidak ada cabang **if** atau **elif** yang benar, cabang **else** terakhir secara otomatis akan dijalankan.



##### Loops

"Tulis 100 angka pertama."

Ada beberapa asumsi yang tersirat dalam perintah yang tampaknya sederhana ini. Pertama, siswa tahu harus mulai dari mana, yaitu di nomor 1. Asumsi kedua, siswa tahu di mana harus mengakhiri, di nomor 100. Dan yang ketiga, siswa memahami bahwa mereka harus menghitung satu per satu.

Dalam pemrograman, sekumpulan instruksi ini dapat dijalankan dengan sebuah perulangan (loop).

Ada tiga komponen utama loop:

1. Awal dari loop
2. Akhir dari loop
3. Kenaikan antara angka dalam loop

Python membedakan antara dua jenis loop dasar: **while** loop, dan **for** loop.



###### While Loop

Dalam **while** loop, segmen kode yang ditentukan diulang dengan syarat kondisi tertentu true. Saat kondisi bernilai false, **while** loop berhenti berjalan. **While** loop mencetak 10 angka pertama.

Kita dapat mencetak 10 angka pertama dengan menerapkan fungsi print 10 kali, tetapi menggunakan **while** loop lebih efisien, dan skalanya mudah. Secara umum, bukan ide yang baik untuk menyalin dan menempel saat membuat kode. Jika kita menemukan diri kita menyalin dan menempel, mungkin ada cara yang lebih efisien. Mari kita lihat blok kode contoh berikut:

```
i = 1 
while i <= 10:  
	print(i)  
	i += 1 
```

Kita akan mendapatkan output berikut:

```
1 
2 
3 
4 
5 
6 
7 
8 
9 
10 
```

Kita dapat memecah blok kode sebelumnya dan mencari tahu apa yang terjadi dalam langkah-langkahnya :

• **Inisialisasi variabel**: Loop perlu diinisialisasi dengan variabel. Variabel akan berubah sepanjang loop. Penamaan variabel terserah kita. **i** sering dipilih karena singkatan dari incrementor. Contohnya adalah **i = 1**.

• **Siapkan perulangan while**: Perulangan while dimulai dengan kata kunci while. Diikuti dengan variabel yang dipilih. Setelah variabel muncul kondisi yang harus dipenuhi agar loop berjalan. Secara umum, kondisi tersebut harus memiliki beberapa cara. Saat menghitung, kondisi biasanya menyertakan batas atas, tetapi bisa juga dipatahkan dengan cara lain, seperti **i != 10**. Baris kode ini adalah bagian paling penting dari perulangan. Dengan mengatur berapa kali loop diharapkan untuk berjalan. Contohnya adalah **while i <= 10 :**.

• **Instruksi**: Instruksi mencakup semua baris identasi setelah titik dua. Apa pun bisa dicetak, fungsi apa pun bisa dipanggil, dan sejumlah baris bisa dieksekusi. Itu semua tergantung programnya. Selama kode tersebut benar secara sintaksis, secara umum, apa pun boleh. Bagian dari loop ini akan terus berjalan selama kondisi yang disebutkan di atas benar. Contohnya adalah **print(i)**.

 • **Increment**: Incrementor adalah bagian penting dari contoh ini. Tanpanya, kode sebelumnya tidak akan pernah berhenti berjalan. Ini akan mencetak 1 tanpa henti karena 1 selalu kurang dari 10. Di sini, kita menambah 1, tetapi kita juga bisa menambah 2, atau angka lainnya. Contohnya adalah **i += 1**.

Sekarang setelah kita memahami bagiannya, sekarang kita harus melihat cara kerjanya :

1. Variabel diinisialisasi sebagai 1. Perulangan while memeriksa kondisi. 1 kurang dari atau sama dengan 10. 1 dicetak. 1 ditambahkan ke i. Kita menambah ke i = 2.
2. Setelah semua kode indentasi setelah titik dua dijalankan, loop dijalankan lagi dengan kembali ke kata kunci while.
3. Loop sementara memeriksa kembali kondisi. 2 kurang dari atau sama dengan 10. 2 dicetak ke konsol. 1 ditambahkan ke i. Kita sekarang menambah ke i = 3.
4. Loop sementara memeriksa kembali kondisi. 3 kurang dari atau sama dengan 10. 3 dicetak ke konsol. 1 ditambahkan ke i. Kita menambah ke i = 4.
5. Perulangan while terus bertambah dan mencetak angka sampai mencapai angka 10.
6. Loop sementara memeriksa kondisi. 10 kurang dari atau sama dengan 10. 10 dicetak ke konsol. 1 ditambahkan ke i. Sekarang, tingkatkan ke i = 11.
7. Loop sementara memeriksa kondisi. 11 tidak kurang dari atau sama dengan 10. Kita keluar dari loop dengan bergerak di luar indentasi.



###### Loop Tak Terhingga

Sekarang kita akan mencoba loop tak terhingga. Potongan kode berikut mendukung topik ini:

```
x = 5
while x <= 20:
	print(x)
```

Python sering kali berjalan sangat cepat. Jika ada sesuatu yang memakan waktu lebih lama dari yang diharapkan, loop tak terbatas mungkin menjadi penyebabnya, seperti dalam cuplikan kode yang disebutkan di atas. Developer di sini akan menyetel semua variabel dan kondisi dengan benar untuk menghindari kasus loop tak terbatas. Contoh kode Python yang ditulis dengan baik adalah sebagai berikut:

```
x = 5
while x<= 20:
    print(x)
    x += 5
```



###### break

**break**  adalah kata kunci khusus dalam Python yang dirancang khusus untuk loop. Jika ditempatkan di dalam loop, biasanya dalam kondisi bersyarat, **break** akan segera menghentikan loop. Tidak peduli apa yang datang sebelum atau sesudah loop. break ditempatkan pada barisnya sendiri, dan keluar dari loop.

Untuk berlatih, kita harus mencetak angka pertama yang lebih besar dari **100** yang habis dibagi **17**.

Idenya adalah kita akan mulai dari 101 dan terus menghitung sampai kita menemukan sebuah angka yang habis dibagi **17**. Asumsikan kita tidak tahu harus berhenti di angka berapa. Di sinilah break berperan. **break** akan menghentikan loop. Kita dapat mengatur batas atas kami pada beberapa angka yang kita tahu tidak akan pernah mencapai dan keluar dari lingkaran ketika kita sampai di sana:

```
# Temukan angka pertama yang lebih besar dari 100 dan habis dibagi 17.
x = 100
while x <= 1000:
    x += 1
    if x % 17 == 0:
        print('', x, 'adalah bilangan pertama yang lebih besar dari 100 yang habis dibagi 17.')
        break
```

Iterator **x + = 1** ditempatkan di awal pengulangan. Ini memungkinkan kita untuk memulai dengan 101. Iterator dapat ditempatkan di mana saja dalam loop.

Karena 101 tidak habis dibagi **17**, loop berulang, dan **x = 102**. Karena **102** habis dibagi **17**, statement print dieksekusi dan kita keluar dari loop.
Ini adalah pertama kalinya kita menggunakan **indentasi ganda**. Karena kondisional **if** ada di dalam **loop** sementara, itu harus diindentasi juga.



###### Kegiatan 4 : Menemukan Kelipatan Persekutuan Terkecil (KPK)

Dalam kegiatan ini, kita akan menemukan KPK dari dua pembagi. KPK dari dua pembagi adalah bilangan pertama yang dapat membagi kedua pembagi.

Misalnya KPK dari 4 dan 6 adalah 12, karena 12 adalah bilangan pertama yang dapat membagi 4 dan 6. Kita akan menemukan KPK dari 2 angka. Kita akan mengatur variabel, kemudian menginisialisasi **while** loop dengan iterator dan Boolean yang **True** secara default. Kita akan menyiapkan kondisional yang akan putus jika iterator membagi kedua angka. Kita akan meningkatkan iterator dan mencetak hasilnya setelah loop selesai.

Dalam aktivitas ini, dengan menggunakan langkah-langkah berikut, Kita perlu mencari KPK dari 24 dan 36.

Ikuti cara berikut :

1. Tetapkan pasangan variabel sebagai **24** dan **36**.

2. Inisialisasi **while** loop, berdasarkan Boolean yang **True** secara default, dengan iterator.

3. Siapkan kondisi untuk memeriksa apakah iterator membagi kedua angka.

4. Putuskan loop while saat KPK ditemukan.

5. Tingkatkan iterator di akhir loop.

6. Cetak hasilnya.

   Kita akan mendapatkan output berikut:

   ```
   Kelipatan Persekutuan Terkecil dari 24 dan 36 adalah 72.
   ```

   

###### Latihan 18 : Menghitung Kuadrat Sempurna

Tujuan latihan ini adalah untuk meminta pengguna memasukkan bilangan tertentu dan mencari tahu apakah itu bilangan kuadrat sempurna.

Ikuti langkah berikut :

1. Buka Notebook Jupyter baru.

2. Minta pengguna memasukkan angka untuk melihat apakah itu kuadrat sempurna:

  ```
  print('Masukkan angka untuk melihat apakah itu persegi yang sempurna.')
  ```

3. Tetapkan variabel sebagai sama dengan **input()**. Dalam hal ini, masukkan 64:

  ```
  angka = input()
  ```

  

4. Pastikan input pengguna adalah bilangan bulat positif:

  ```
  angka = abs(int(angka))
  ```

5. Pilih variabel iterator:

  ```
  i = -1
  ```

6. Inisialisasi Boolean untuk memeriksa kuadrat sempurna:

  ```
  square = False
  ```

7. Inisialisasi **while** loop dari -1 ke akar kuadrat dari bilangan tersebut:

   ```
   while i <= angka** (0.5):
   ```

8. Naikan i sebesar 1:

  ```
  i += 1
  ```

9. Periksa akar kuadrat dari bilangan tersebut:

  ```
  if i*i == angka:
  ```

10. Tunjukkan bahwa kita memiliki kuadrat sempurna:

    ```
    square = True
    ```

11. **Break** dari loop:

    ```
    break
    ```

12. Jika angkanya persegi, cetak hasilnya:

    ```
    if square:
    	print('Akar kuadrat dari', angka, 'adalah', i, '.')
    ```

    

13. Jika angkanya bukan persegi, cetak hasil ini:

    ```
    else:
    	print('', number, 'bukan kuadran sempurna.')
    ```

    

    Kita akan mendapatkan output berikut:

    ```
    Akar kuadrat dari 64 adalah 8.
    ```

    



###### Latihan 19 : Penawaran Real Estate

Tujuan dari latihan ini adalah untuk mendorong pengguna untuk menawar sebuah rumah dan memberi tahu mereka jika dan kapan tawaran telah diterima.

Ikuti langkah berikut : 

1. Buka Notebook Jupyter baru.

2. Mulailah dengan menyatakan harga pasar:

  ```
  print('Satu kamar tidur di Jakarta terdaftar seharga Rp 500.000.000')
  ```

3. Minta pengguna untuk membuat penawaran di rumah:

  ```
  print('Masukkan penawaran pertama anda.')
  ```

4. Setel **penawaran** sama dengan **input()**:

  ```
  penawaran = abs(int(input()))
  ```

5. Minta pengguna memasukkan penawaran terbaik untuk rumah tersebut:

  ```
  print('Masukkan penawaran terbaik anda.')
  ```

6. Setel yang **terbaik** sebagai sama dengan input():

  ```
  terbaik = abs(int(input()))
  ```

7. Minta pengguna untuk memilih kenaikan:

  ```
  print('Berapa banyak lagi yang ingin anda tawarkan setiap kali?')
  ```

8. Setel **increment** sama dengan **input()**:

  ```
  increment = abs(int(input()))
  ```

9. Setel **penawaran_disetujui** sama dengan **False**:

  ```
  penawaran_disetujui = False
  ```

10. Inisialisasi perulangan **while** dari **penawaran** ke **terbaik**:

    ```
    while penawaran <= terbaik:
    ```

11. Jika **penawaran** lebih besar dari **650000000**, mereka mendapatkan rumah:

    ```
    if penawaran >= 650000000:
        penawaran_disetujui = True
        print('Tawaran anda untuk', penawaran, 'telah diterima!')
        break
    ```

12. Jika tawaran tidak melebihi **650000000**, mereka tidak mendapatkan rumah:

    ```
    print('Maaf, Anda menawarkan', penawaran, 'belum diterima.')
    ```

13. Tambahkan **increment** untuk **penawaran**:

    ```
    penawaran += increment
    ```



Kita akan mendapatkan output sebagai berikut :

```
Satu kamar tidur di Jakarta terdaftar seharga Rp 500.000.000
Masukkan penawaran pertama anda.
500000000
Masukkan penawaran terbaik anda.
700000000
Berapa banyak lagi yang ingin anda tawarkan setiap kali?
50000000
Maaf, Anda menawarkan 500000000 belum diterima.
Maaf, Anda menawarkan 550000000 belum diterima.
Maaf, Anda menawarkan 600000000 belum diterima.
Tawaran anda untuk 650000000 telah diterima!
```



###### for Loop

Loop **for** mirip dengan **while** loop, tetapi memiliki kelebihan tambahan, seperti dapat melakukan iterasi terhadap string dan objek lainnya.



###### Latihan 20 : Menggunakan for Loops

Dalam latihan ini, kita akan menggunakan for loop untuk mencetak karakter dalam string selain serangkaian angka:

1. Buka Notebook Jupyter baru.
2. Cetak karakter 'Indonesia':

```
for i in 'Indonesia':
print(i)
```

Kita akan mendapatkan output sebagai berikut :

```
I
n
d
o
n
e
s
i
a
```

Kata kunci **for** sering kali mengikuti kata kunci **in**. Variabel **i** bersifat umum. Ungkapan, **for i in**, berarti Python akan memeriksa apa yang muncul selanjutnya dan melihat komponen individualnya. String terdiri dari karakter, jadi Python akan melakukan sesuatu dengan masing-masing karakter. Dalam kasus khusus ini, Python akan mencetak karakter individu, sesuai perintah print(i).


Bagaimana jika kita ingin melakukan sesuatu dengan berbagai angka? Bisakah for loop digunakan untuk itu? Benar. Python menyediakan kata kunci lain, **range**, untuk mengakses berbagai angka. **range** sering kali ditentukan oleh dua angka, angka pertama, dan angka terakhir, dan mencakup semua angka di antaranya. Menariknya, keluaran **range** mencakup angka pertama, tetapi bukan angka terakhir. Kita akan melihat alasannya sebentar lagi.



3. Kita menggunakan batas bawah 1 dan batas atas 10 dengan kisaran untuk mencetak 1-9:

```
for i in range(1,10):
	print(i)
```

Kita akan mendapatkan output sebagai berikut :

```
1
2
3
4
5
6
7
8
9
```

Tidak mencetak angka 10 dalam range.



4. Sekarang gunakan range dengan satu batasan saja, angka 10, untuk mencetak sepuluh angka pertama:

```
for i in range(10):
	print(i)
```

Kita akan mendapatkan output sebagai berikut :

```
0
1
2
3
4
5
6
7
8
9
```

Jadi, range(10) akan mencetak 10 angka pertama dari 0 sampai 9.

Sekarang katakanlah kita ingin menghitung dengan nilai increment 2. Kita dapat menambahkan batas ketiga, kenaikan langkah, untuk menghitung naik atau turun dengan angka yang diinginkan.
Gunakan kenaikan langkah untuk menghitung angka genap sampai 10:

```
for i in range(1, 11, 2):
	print(i)
```

Kita akan mendapatkan output sebagai berikut :

```
1
3
5
7
9
```

Demikian pula, kita dapat menghitung mundur menggunakan angka negatif, yang ditunjukkan pada langkah berikutnya.

5. Gunakan increment untuk menghitung mundur dari 3 ke -1:

```
for i in range(3, 0, -1):
	print(i)
```

Kita akan mendapatkan output sebagai berikut :

```
3
2
1
```

Dan, tentu saja, kita bisa menggunakan loop bersarang (nested), yang ditunjukkan pada langkah berikutnya.

6. Sekarang, cetak setiap huruf dari nama tiga kali:

```
nama = 'Iqbal'
for i in range(3):
	for i in nama:
		print(i)
```

Kita akan mendapatkan keluaran sebagai berikut :

```
I
q
b
a
l
I
q
b
a
l
```



###### Kata Kunci continue

**Continue** adalah kata kunci Python lain yang didesain untuk loop. Ketika Python mencapai kata kunci **continue**, itu menghentikan kode dan kembali ke awal perulangan.
**Continue** mirip dengan **break** karena keduanya menginterupsi proses loop, tetapi **break** menghentikan loop, melanjutkan loop dari awal.

Mari kita lihat contoh praktik continue. Kode berikut mencetak setiap bilangan prima dua digit:

```
for num in range(10,100):
    if num % 2 == 0:
    	continue
    if num % 3 == 0:
   	 	continue
    if num % 5 == 0:
    	continue
    if num % 7 == 0:
    	continue
    print(num)
```

Kita akan mendapatkan output sebagai berikut :

```
11
13
17
19
23
29
31
37
41
43
47
53
59
61
67
71
73
79
83
89
97
```

Mari kita lihat awal kode. Angka pertama yang harus diperiksa adalah 10. Baris pertama memeriksa untuk melihat apakah 10 dapat dibagi 2. Karena 2 membagi 10, kita masuk ke dalam kondisional dan mencapai kata kunci continue. Menjalankan continue kembali ke awal loop.

Angka berikutnya yang diperiksa adalah 11. Karena 2,3,5, dan 7 tidak membagi 11, Kita mencapai baris terakhir dan mencetak angka 11.



###### Kegiatan 5 : Membangun Bot Percakapan Menggunakan Python

Kamu bekerja sebagai Python Developer dan kamu sedang membangun dua bot percakapan untuk klienmu. Kamu membuat daftar langkah-langkah sebelumnya untuk membantumu, seperti yang diuraikan di bagian berikut. Langkah-langkah ini akan membantumu membangun dua bot yang mengambil masukan dari pengguna dan menghasilkan respon.

Tujuan dari kegiatan ini adalah menggunakan kondisional bersarang (nested) untuk membangun dua bot percakapan. Dalam aktivitas ini, kita akan membangun dua bot percakapan. Bot pertama akan menanyakan dua pertanyaan kepada pengguna dan menyertakan jawaban pengguna di setiap tanggapan tindak lanjutnya. Bot kedua akan menanyakan pertanyaan yang membutuhkan jawaban numerik. Respon yang berbeda akan diberikan pada skala yang berbeda. Proses ini akan diulangi untuk pertanyaan kedua.



Ikuti langkah berikut :

Untuk bot pertama, langkah-langkahnya adalah sebagai berikut:
1. Ajukan setidaknya dua pertanyaan kepada pengguna.
2. Tanggapi setiap jawaban. Sertakan jawabannya dalam tanggapannya.

Untuk bot kedua, langkah-langkahnya adalah sebagai berikut:

1. Ajukan pertanyaan yang dapat dijawab dengan skala angka, seperti "Pada skala 1-10 ... ".
2. Menanggapi secara berbeda tergantung pada jawaban yang diberikan.
3. Sebutkan pertanyaan berbeda mengikuti setiap jawaban yang dapat dijawab dengan skala angka.
4. Menanggapi secara berbeda tergantung pada jawaban yang diberikan.



Output yang diharapkan untuk bot 1 adalah sebagai berikut:

![13](D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\13.png)

Output yang diharapkan untuk bot 2 adalah sebagai berikut:

![14](D:\Cupiz\Nulis\Python\Workshop\gambar\sesi1\14.png)



##### Kesimpulan

Kita telah mempelajari banyak materi di sesi pengantar ini. Kita telah membahas operasi matematika, penggabungan string dan metode, jenis Python umum, variabel, kondisional, dan loop. Menggabungkan elemen-elemen ini memungkinkan kita untuk menulis program yang bernilai nyata.

Selain itu, kita telah mempelajari sintaks Python. Sekarang kita memahami beberapa kesalahan paling umum, dan kita menjadi terbiasa dengan pentingnya identasi. Kita sedang mempelajari cara memanfaatkan kata kunci penting seperti **range**, **in**, **if**, dan **True** dan **False**.

Untuk selanjutnya, kita sekarang memiliki keterampilan dasar utama yang dibutuhkan oleh semua programmer Python. Meskipun ada banyak hal yang harus dipelajari, kita memiliki landasan penting untuk mengembangkan jenis dan teknik yang dibahas di sini.

Selanjutnya, kita akan belajar tentang beberapa jenis Python yang paling penting, termasuk list, dictionaries, tuple, dan sets.