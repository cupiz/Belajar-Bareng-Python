# Sesi 3 : Menjalankan Python - Program, Algoritma, dan Fungsi

[TOC]



### Python Scripts dan Modules

Kita telah menjalankan Python di konsol Python interaktif atau Jupyter Notebook. Namun, kita mungkin menyadari bahwa sebagian besar kode Python ada di file teks dengan ekstensi **.py**. File-file ini hanyalah teks biasa dan dapat diedit dengan editor teks apa pun. Pemrogram biasanya mengedit file ini menggunakan editor teks seperti Notepad ++, atau Integrated Development Environments (IDEs) seperti Jupyter atau PyCharm.

Biasanya, file **.py** mandiri disebut **scripts** atau **modules**. Skrip adalah file yang dirancang untuk dieksekusi, biasanya dari baris perintah. Di sisi lain, modul biasanya diimpor ke bagian lain dari kode atau shell interaktif untuk dieksekusi. Perhatikan bahwa ini bukanlah perbedaan yang tegas; modul dapat dijalankan, dan skrip dapat diimpor ke skrip / modul lain.





#### Latihan 34 : Menulis dan Menjalankan Script Pertama

Dalam latihan ini, kita akan membuat skrip bernama **my_script.py** dan menjalankannya pada baris perintah. Kemudian kita akan mencari jumlah faktorial dari tiga angka :

1. Menggunakan editor teks favorit, buat file baru bernama **my_script.py**. Kita juga dapat menggunakan Jupyter (**New | Text File**).

2. Import library **math** :

   ```
   import math
   ```

3. Misalkan kita memiliki list angka dan kita ingin mencetak jumlah faktorial dari angka-angka ini. Ingatlah bahwa faktorial adalah hasil kali dari semua bilangan bulat dan sama dengan bilangan tertentu.
   Misalnya, faktorial dari 5 dihitung sebagai 5! = 5 * 4 * 3 * 2 * 1 = 120.
   Dalam potongan kode berikut, kita akan menemukan jumlah faktorial dari 5,7 dan 11.

   ```
   numbers = [5, 7, 11]
   ```

4. Menggunakan fungsi **math.factorial** dan pemahaman list, menghitung dan mencetak **result** :

   ```
   result = sum([math.factorial(n) for n in numbers])
   print(result)
   ```

5. Simpan file

6. Buka Terminal atau Notebook Jupyter dan pastikan bahwa direktori kita saat ini sama dengan yang ada di file **my_script.py**. Untuk memeriksanya, jika kita menjalankan **dir** di Terminal, kita akan melihat **my_script.py** di list berkas. Jika tidak, navigasikan ke direktori yang benar menggunakan perintah **cd**.

7. Ketik **python my_script.py** dan Run untuk menjalankan script.

   Kita akan mendapatkan output berikut :

   ```
   39921960
   ```





#### Latihan 35 : Menulis dan Mengimpor Modules Pertama

Dalam latihan ini, seperti dalam latihan sebelumnya, kita akan menemukan faktorial dari tiga bilangan. Namun, kita sekarang akan membuat modul bernama my_module.py, dan mengimpornya ke shell Python:

1. Menggunakan editor teks favorit, buat file baru bernama **my_modules.py**. Kita juga dapat menggunakan Jupyter (**New | Text File**).

2. Tambahkan fungsi yang mencetak hasil komputasi di Latihan 34, Menulis dan Menjalankan Skrip Pertama. Kita akan mempelajari lebih lanjut tentang notasi fungsi ini di bagian selanjutnya tentang fungsi dasar :

   ```
   import math
   def compute(numbers):
   	return([math.factorial(n) for n in numbers])
   ```

3. Simpan file

4. Bukan shell Python atau Jupyter dan jalankan perintah ini :

   ```
   from my_module import compute
   compute([5, 7, 11])
   ```

   Kita akan mendapatkan output berikut :

   ```
   [120, 5040, 39916800]
   ```





#### Shebangs di Ubuntu

Baris pertama dari skrip Python adalah:

```
#!/usr/bin/env python
```

Sebagai informasi tambahan, jika kita menggunakan sistem operasi Windows, kita dapat mengabaikan baris ini. Namun, perlu dipahami fungsinya. Jalur ini menentukan program yang harus digunakan komputer untuk menjalankan file ini. Pada contoh sebelumnya, kita harus memberi tahu Command Prompt untuk menggunakan Python untuk menjalankan skrip **my_script.py** kita. Namun, pada sistem UNIX (seperti Ubuntu atau macOS X), jika skrip kita memiliki shebang, kita dapat menjalankannya tanpa menentukan bahwa sistem harus menggunakan Python. Misalnya, menggunakan Ubuntu, kita cukup menulis:

```
./my_script.py
```





#### Docstrings

Docstring yang disebutkan di Sesi 1 adalah string yang muncul sebagai pernyataan pertama dalam skrip, fungsi, atau kelas. Docstring menjadi atribut khusus dari objek tersebut, dapat diakses dengan **__ doc__**. Docstrings digunakan untuk menyimpan **informasi deskriptif** untuk menjelaskan kepada pengguna untuk apa kode itu, dan beberapa informasi tingkat tinggi tentang bagaimana mereka harus menggunakannya.





#### Latihan 36 : Menambahkan Docstring ke my_module.py

Dalam latihan ini, Akita memperluas modul **my_module.py** dari Latihan 35, dengan menambahkan docstring:

1. Buka **my_module.py** di Jupyter atau teks editor .

2. Tambahkan docstring ke skrip (sebagai baris pertama sebelum memulai dengan kode kita seperti yang disebutkan dalam cuplikan kode berikut):

   ```
   """ This script computes the sum of the factorial of a list of numbers"""
   ```

3. Buka konsol Python di direktori yang sama dengan file **my_module.py**.

4. Import modul **my_module** :

   ```
   import my_module
   ```

5. Panggil fungsi **help** pada skrip **my_module** kita untuk melihat docstring. Fungsi **help** dapat digunakan untuk mendapatkan ringkasan informasi apa pun yang tersedia mengenai modul, fungsi, atau kelas dengan Python. Kita juga bisa memanggilnya tanpa argumen, yaitu, sebagai help(), untuk memulai rangkaian perintah interaktif:

   ```
   help(my_module)
   ```

   Kita akan mendapatkan output berikut :

   ![1](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/1.png)

6. Lihat properti **_ _doc__**  dan **my_module** sebagai cara kedua untuk melihat docstring:

   ```
   my_module.__doc__
   ```

   Kita akan mendapatkan output berikut :

   ```
   'This script computes the sum of the factorial of a list of numbers'
   ```

   Docstring dapat mencakup satu baris, seperti dalam contoh sebelumnya, atau beberapa baris. Berikut ini adalah contoh Docstring:

   ```
   """
   This script computes the sum of the factorial of a list of numbers.
   """
   ```





#### Import

Setelah pernyataan shebang dan docstring opsional, file Python biasanya mengimpor kelas, modul, dan fungsi dari pustaka lain. Misalnya, jika kita ingin menghitung nilai **exp(2)**, kita dapat mengimpor modul **math** dari pustaka standar (Kita akan mempelajari selengkapnya tentang standar library di Sesi 6, standar Library) :

```
import math
math.exp(2)
```

Kita akan mendapatkan output berikut :

```
7.38905609893065
```

Dalam contoh sebelumnya, kita mengimpor modul math dan memanggil fungsi **exp** yang ada di dalam modul. Alternatifnya, kita dapat mengimpor fungsi itu sendiri dari modul **math**:

```
from math import exp
exp(2)
```

Kita akan mendapatkan output berikut :

```
7.38905609893065
```

Perhatikan bahwa ada cara pengimporan ketiga, yang umumnya harus dihindari kecuali jika diperlukan:

```
from math import *
exp(2)
```

Kita akan mendapatkan output berikut :

```
7.38905609893065
```

Sintaks **import *** hanya mengimpor semua yang ada di modul. Ini dianggap tidak diinginkan terutama karena kita berakhir dengan referensi ke terlalu banyak objek, dan ada risiko bahwa nama objek ini akan bentrok. Juga lebih sulit untuk melihat dari mana objek tertentu diimpor jika ada beberapa pernyataan **import ***.

Kita juga dapat mengganti nama modul atau objek yang diimpor dalam pernyataan import itu sendiri:

```
from math import exp as exponential
exponential(2)
```

Kita akan mendapatkan output berikut :

```
7.38905609893065
```

Ini terkadang berguna jika kita merasa nama objeknya terlalu berat, membuat kode kita kurang dapat dibaca. Atau, mungkin diperlukan jika kita ingin menggunakan dua modul yang kebetulan memiliki nama yang sama.





#### Latihan 37 : Menemukan Tanggal Sistem

Dalam latihan ini, kita menulis skrip yang mencetak tanggal sistem saat ini ke konsol dengan mengimpor modul **datetime**:

1. Buat skrip baru bernama **today.py** di Terminal Python.

2. Tambahkan docstring ke skrip:

  ```
  """
  This script prints the current system date.
  """
  ```

3. Impor modul **datetime**:

  ```
  import datetime
  ```

4. Cetak tanggal sekarang menggunakan properti **now()** dari **datetime.date**:

  ```
  print(datetime.date.today())
  ```

5. Jalankan script dari baris perintah seperti yang ditunjukkan dan akan mendapatkan output seperti ini :

   ```
   2020-12-17
   ```

   Dalam latihan ini, kita dapat menulis skrip yang mencetak tanggal dan waktu menggunakan modul datetime. Karenanya, kita dapat melihat bagaimana modul dapat membantu.

   Pernyataan if **_ _name__** == **"_ _main__"**

   Kita akan sering melihat pernyataan samar ini dalam skrip Python. Kita tidak akan membahas konsep ini secara mendalam, tetapi perlu dipahami. Ini digunakan ketika kita ingin dapat menjalankan skrip dengan sendirinya, tetapi juga dapat mengimpor objek dari skrip seolah-olah itu adalah modul biasa.

   Misalnya, kita ingin mendapatkan jumlah angka dari 1 hingga 10. Jika kita menjalankan fungsi dari baris perintah, kita ingin hasilnya dicetak ke konsol. Namun, kita juga ingin dapat mengimpor nilai untuk digunakan di tempat lain dalam kode kita.

   Ketik kode di bawah :

   ```
   result = 0
   for n in range(1, 11): # Recall that this loops through 1 to 10, not including 11
   	result += n
   print(result)
   ```

   Jika kita menjalankan program ini dari baris perintah, ini akan mencetak keluaran 55, seperti yang diharapkan. Namun, jika kita mencoba mengimpor hasil di konsol Python, hasilnya akan dicetak lagi. Saat mengimpor hasil, kita hanya menginginkan variabel; kita tidak mengharapkannya untuk mencetak ke konsol:

   ```
   from sum_to_10 import result
   ```

   Kita akan mendapatkan output berikut :

   ```
   55
   ```

   Untuk memperbaikinya, kita hanya memanggil fungsi cetak jika **_ _name__** == '**_ _main__**':

   ```
   result = 0
   for n in range(1, 11): # Recall that this loops through 1 to 10, not including 11
   	result += n
   if __name__ == '__main__':
   	print(result)
   ```

   Saat mengeksekusi dari baris perintah, penerjemah Python menetapkan variabel __name__ khusus sama dengan string '__main__', sehingga ketika kita sampai ke bagian akhir skrip kita, hasilnya dicetak. Namun, saat mengimpor hasil, pernyataan cetak tidak pernah tercapai:

   ```
   from sum_to_10 import result
   result * 2
   110
   ```





#### Kegiatan 8 : Jam Berapa ?

Kita diminta untuk membuat skrip Python yang memberi tahu kita waktu saat ini.

Dalam kegiatan ini, kita akan menggunakan modul **datetime** untuk membangun skrip **current_time.py** yang mengeluarkan waktu sistem saat ini, dan kemudian kita akan mengimpor skrip **current_time.py** ke konsol Python.

Ikuti langkah berikut :

1. Buat skrip baru bernama **current_time.py** di Jupyter atau editor teks.

2. Tambahkan **docstring** ke skrip untuk menjelaskan fungsinya.

3. Impor modul **datetime**.

4. Dapatkan waktu saat ini menggunakan **datetime.now()**.

5. Cetak hasilnya, tetapi hanya jika skrip akan dijalankan.

6. Jalankan skrip dari Command Prompt untuk memeriksanya mencetak waktu.

7. Impor time ke konsol Python dan periksa apakah keluaran konsol tidak mencetak waktu.

8. Output dari Command Prompt adalah sebagai berikut:

   ```
   13:12:55.555555
   ```

   Output dari konsol Python akan terlihat seperti ini:

   ```
   datetime.time(18, 44, 21, 50000)
   ```





### Algoritma Python

Algoritme adalah rangkaian instruksi yang dapat dijalankan untuk melakukan tugas atau komputasi tertentu. Resep kue adalah contoh algoritme. Misalnya, panaskan oven, kocok 125 g gula pasir dan 100 g mentega, lalu tambahkan telur dan bahan lainnya. Demikian pula, perhitungan sederhana dalam matematika adalah algoritma. Misalnya, saat menghitung keliling lingkaran, kita mengalikan jari-jari dengan 2π. Ini adalah algoritma yang singkat, namun bagaimanapun juga sebuah algoritma.

Algoritme pada awalnya sering kali didefinisikan dalam **pseudocode**, yang merupakan cara menuliskan langkah-langkah yang akan dibuat program komputer tanpa membuat kode dalam bahasa tertentu. Seorang pembaca tidak perlu memiliki latar belakang teknis untuk membaca logika yang diekspresikan dalam pseudocode. Misalnya, jika kita memiliki list bilangan positif dan ingin mencari jumlah maksimum bilangan positif dalam list itu, algoritme yang dinyatakan dalam **pseudocode** adalah sebagai berikut:

1. Tetapkan variabel **maximum** ke 0.
2. Untuk setiap nomor dalam list kita, periksa apakah angkanya lebih besar dari maksimum.
    Tetapkan variabel **maximum** agar sama dengan angka itu.
3. **maximum** sekarang sama dengan angka terbesar dalam list.

Pseudocode berguna karena memungkinkan kita untuk menampilkan logika kode kita dalam format yang lebih dapat diakses secara universal daripada menulis dalam bahasa pemrograman tertentu. Pemrogram akan sering memetakan pemikiran mereka dalam pseudocode untuk mengeksplorasi logika pendekatan yang direncanakan sebelum menulis kode itu sendiri.

Dalam Latihan 38, Angka Maksimum, Kita akan menggunakan pseudocode ini untuk mencari angka maksimum dari list angka.





#### Latihan 38 : Angka Maksimum

Dalam latihan ini, kita akan menerapkan pseudocode untuk mencari nilai maksimum dari list bilangan positif:

1. Buat list nomor:

  ```
  l = [4, 2, 7, 3]
  ```

2. Tetapkan variabel **maximum** sama dengan 0:

  ```
  maximum = 0
  ```

3. Lihat setiap angka, dan bandingkan dengan **maximum**:

   ```
   for number in l:
   	if number > maximum:
   		maximum = number
   ```

4. Periksa hasilnya:

  ```
  print(maximum)
  ```

  Kita akan mendapatkan output berikut :

  ```
  7
  ```





#### Kompleksitas Waktu

Kita telah terbiasa dengan program yang dijalankan dengan kecepatan yang hampir seketika. Komputer sangat cepat, dan perbedaan antara melakukan 10 iterasi dalam satu loop dan 1.000 iterasi mungkin tampak tidak penting bagi kita. Namun, algoritma dapat dengan cepat menjadi tidak efisien saat masalah berkembang. Dalam mengukur kompleksitas, kita tertarik untuk mengetahui waktu yang dibutuhkan untuk mengeksekusi algoritma berubah seiring dengan perubahan ukuran masalah. Jika masalahnya 10 kali lebih besar, apakah algoritma memerlukan waktu 10 kali lebih lama untuk dieksekusi, 100 kali lebih lama, atau 1010 kali lebih lama? Hubungan antara ukuran masalah dan langkah-langkah yang diambil disebut kompleksitas waktu suatu algoritma.

Tentu saja, kita dapat mengatur waktu algoritme kita pada masalah dengan ukuran berbeda dan mengamati hubungannya pada grafik. Teknik ini sering kali berguna jika algoritmanya rumit, dan hubungan teoretis antara ukuran dan waktu tidak dapat dihitung. Namun, ini tidak sepenuhnya memuaskan, karena waktu sebenarnya yang dibutuhkan juga bergantung pada faktor-faktor seperti memori yang tersedia, prosesor, kecepatan disk, dan proses lain yang memakan sumber daya pada mesin. Ini hanya akan menjadi perkiraan empiris dan dapat bervariasi tergantung pada komputer.

Sebagai gantinya, kita cukup menghitung jumlah operasi yang diperlukan untuk menjalankan algoritme. Hasil penghitungan ini dinyatakan dengan notasi O besar. Misalnya, O(n) berarti bahwa, untuk soal berukuran n, banyaknya langkah yang dilakukan sebanding dengan n. Ini berarti bahwa jumlah langkah sebenarnya yang diperlukan dapat dinyatakan sebagai a * n + B, di mana alfa dan beta adalah konstanta. Cara lain untuk berpikir tentang ini adalah bahwa langkah-langkah yang diperlukan untuk mengeksekusi algoritme tumbuh secara linier dengan ukuran masalah:

Setiap masalah yang kompleksitasnya dapat diekspresikan sebagai fungsi linier, **a * n + B**, memiliki kompleksitas waktu **O(n)**.
Kompleksitas waktu umum lainnya termasuk:
• **O(1): Waktu konstan.** Di sini, waktu yang dibutuhkan selalu sama, terlepas dari ukuran masalahnya; misalnya, mengakses elemen array pada indeks tertentu.
• **O(n ^ 2): Waktu kuadrat.** Di sini, waktu yang dibutuhkan sebanding dengan kuadrat ukuran soal; misalnya, algoritma pengurutan gelembung (ini tercakup dalam Latihan 39, Menggunakan Bubble Sort dengan Python).
• **O(log n): Waktu logaritmik.** Di sini, waktu yang dibutuhkan sebanding dengan logaritma natural dari ukuran masalah; misalnya, algoritma pencarian biner (ini tercakup dalam Latihan 41, Pencarian Biner dengan Python).





#### Kompleksitas Waktu untuk Algoritma Bilangan Maksimum

Pada latihan sebelumnya, kita menghitung jumlah maksimum dari list bilangan positif.
Di sini, kita mengekspresikan kompleksitas algoritme menggunakan notasi big-O:

1. Program kita dimulai dengan menetapkan variabel **maximum = 0**. Ini adalah langkah pertama kita: **total_steps = 1**.
2. Untuk list ukuran **n**, kita akan mengulang setiap nomor dan melakukan operasi berikut:
(a) Periksa apakah lebih besar dari variabel maksimum.
(b) Jika demikian, tetapkan maksimum ke nomor tersebut.
3. Kadang-kadang, akan ada satu langkah yang dijalankan untuk sebuah nomor dan, terkadang, akan ada dua langkah (jika angka itu kebetulan adalah jumlah maksimum baru). Kita tidak terlalu peduli berapa angka ini, jadi, mari kita hitung rata-ratanya, yang akan kita sebut **a**. Artinya, untuk setiap angka akan ada rata-rata **a** langkah yang dilakukan, dimana **a** ada di antara angka 1 dan 2.
4. Jadi, **total_steps = 1 + a * n**. Ini adalah fungsi linier, jadi kompleksitas waktunya adalah **O(n)**.





#### Algoritma Sorting

Keluarga algoritma yang paling sering dibahas dalam kursus ilmu komputer adalah algoritma sorting. Algoritme sorting membantu kita ketika, katakanlah, kita memiliki list nilai, dan kita ingin menyortirnya ke dalam list berurutan. Masalah ini selalu ada di dunia berbasis data kita; pertimbangkan skenario berikut:

• Kita memiliki database kontak dan ingin melihatnya terlist menurut abjad.
• Kita ingin mendapatkan kembali lima hasil tes terbaik dari kelas siswa.
• Kita memiliki list polis asuransi dan ingin melihat mana yang memiliki klaim terbaru.

Output dari algoritme sorting apa pun harus memenuhi dua kondisi:
1. Itu harus dalam urutan tidak menurun. Artinya, setiap elemen harus sama atau lebih besar dari elemen yang datang sebelumnya.
2. Ini harus menjadi permutasi dari input. Artinya, elemen masukan harus diatur ulang dan tidak diubah.

Berikut adalah contoh sederhana tentang apa yang kita ingin agar algoritma sorting tercapai:

![2](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/2.png)

Salah satu algoritme untuk menjalankan operasi ini disebut bubble sort. Dijelaskan sebagai berikut:

1. Mulailah dengan dua elemen pertama dari list ini. Jika yang pertama lebih besar dari yang kedua, maka ganti posisi angkanya. Dalam hal ini, kita membiarkannya apa adanya, seperti 5 < 8 :

   ![3](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/3.png)

2. Pindah ke dua elemen berikutnya. Di sini, kita mengganti posisi 8 dan 1:

   ![4](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/4.png)

3. Untuk pasangan berikutnya, sekali lagi, ubah posisi, seperti 8 > 3 :

   ![5](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/5.png)

4. Untuk pasangan terakhir, ganti posisi lagi, seperti 8 > 2 :

   ![5a](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/5a.png)

5. Kembali ke awal list dan ulangi proses sebelumnya.
6. Lanjutkan perulangan melalui list sampai tidak ada pertukaran lebih lanjut yang diperlukan.





#### Latihan 39 : Menggunakan Bubble Sort dengan Python

Dalam latihan ini, kita akan mengimplementasikan algoritma pengurutan gelembung dengan Python dengan list angka:

1. Mulailah dengan list nomor:

   ```
   l = [5, 8, 1, 3, 2]
   ```

2. Buat indikator yang akan memberi tahu kami kapan kita dapat berhenti melakukan perulangan melalui array:

   ```
   still_swapping = True
   ```

3. Lihatlah setiap angka, dan bandingkan dengan maximum :

   ```
   while still_swapping:
       still_swapping = False
       for i in range(len(l) - 1):
           if l[i] > l[i+1]:
               l[i], l[i+1] = l[i+1], l[i]
               still_swapping = True
   ```

4. Cek hasilnya

   ```
   l
   ```

   Kita akan mendapatkan output berikut :

   ```
   [1, 2, 3, 5, 8]
   ```

   Bubble sort adalah algoritma pengurutan yang sangat sederhana namun tidak efisien. Kompleksitas waktunya adalah **O(n^2)**, artinya jumlah langkah yang diperlukan sebanding dengan kuadrat ukuran list.





#### Algoritma Searching

Keluarga algoritma penting lainnya adalah algoritma searching. Di dunia di mana kita menghasilkan jumlah data yang meningkat secara eksponensial, algoritme ini berdampak besar pada kehidupan sehari-hari kita. Hanya dengan mempertimbangkan ukuran Google seharusnya memberi kita apresiasi tentang pentingnya (dan kompleksitas) algoritme ini. Tentu saja, kita menemukan kebutuhan akan algoritme ini hampir setiap kali kita mengangkat telepon atau membuka laptop :

• Mencari list kontak kita untuk mengirim pesan
• Mencari aplikasi tertentu di komputer kita
• Mencari email yang berisi rencana perjalanan penerbangan

Dengan salah satu contoh berikut, kita dapat menerapkan bentuk pencarian yang paling sederhana, yaitu pencarian linier. Ini akan melibatkan hanya perulangan melalui semua kemungkinan hasil dan memeriksa apakah mereka cocok dengan kriteria pencarian. Misalnya, jika kita sedang mencari list kontak kita, kita akan melihat setiap kontak satu per satu, dan memeriksa apakah kontak tersebut memenuhi kriteria pencarian. Jika demikian, kembalikan posisi hasilnya. Ini adalah algoritma yang sederhana namun tidak efisien, dengan kompleksitas waktu **O(n)**.





#### Latihan 40 : Linear Search dengan Python

Dalam latihan ini, kita akan mengimplementasikan algoritma pencarian (searching) linier dengan Python menggunakan list angka:

1. Mulailah dengan list nomor:

   ```
   l = [5, 8, 1, 3, 2]
   ```

2. Tentukan nilai untuk **search_for**:

   ```
   search_for = 8
   ```

3. Buat variabel **result** yang memiliki nilai default -1. Jika pencarian tidak berhasil, nilai ini akan tetap -1 setelah algoritma dijalankan:

   ```
   result = -1
   ```

4. Loop list nya. Jika nilainya sama dengan nilai pencarian, atur **result**, dan keluar dari loop:

   ```
   for i in range(len(l)):
       if search_for == l[i]:
           result = i
           break
   ```

5. Cek **result** :

   ```
   print(result)
   ```

   Kita akan mendapatkan output berikut :

   ```
   1
   ```





Algoritme pengurutan umum lainnya disebut pencarian biner atau **binary search**. Algoritme pencarian biner mengambil array yang diurutkan dan menemukan posisi nilai target. Misalkan kita mencoba mencari posisi angka 11 dalam list berikut :

![7](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/7.png)

Algoritma pencarian biner akan dijelaskan sebagai berikut:

1. Ambil titik tengah dari list. Jika nilai ini kurang dari nilai target, buang bagian kiri list, dan sebaliknya. Dalam kasus ini, nilai target kita 11 lebih besar dari 8, jadi kita tahu bahwa kita dapat membatasi pencarian kita ke sisi kanan list (karena kita tahu array diurutkan):

   ![8](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/8.png)

2. Kita ulangi proses ini dengan sisi kanan list, memilih titik tengah dari nilai yang tersisa. Karena nilai target, 11 kurang dari titik tengah 12, dan kita membuang sisi kanan sublist kita :

   ![9](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/9.png)

3. Ini memberi kita nilai yang kita cari :

   ![10](https://github.com/cupiz/Belajar-Bareng-Python/blob/main/gambar/sesi3/10.png)





#### Latihan 41: Binary Search dengan Python

Dalam latihan ini, kita akan mengimplementasikan algoritma pencarian (searching) binary dengan Python menggunakan list angka:

1. Mulailah dengan list nomor:

   ```
   l = [2, 3, 5, 8, 11, 12, 18]
   ```

2. Tentukan nilai untuk **search_for**:

   ```
   search_for = 11
   ```

3. Buat dua variabel yang akan mewakili lokasi awal dan akhir sublist yang kita cari. Awalnya, ini akan mewakili indeks awal dan akhir untuk seluruh list :

   ```
   slice_start = 0
   slice_end = len(l) - 1
   ```

4. Tambahkan variabel untuk menunjukkan apakah pencarian berhasil :

  ```
  found = False
  ```

5. Temukan titik tengah list, dan periksa apakah nilainya lebih besar atau lebih kecil dari istilah pencarian. Bergantung pada hasil perbandingan, selesaikan pencarian atau perbarui lokasi untuk awal / akhir sublist :

   ```
   while slice_start <= slice_end and not found:
       location = (slice_start + slice_end) // 2
       if l[location] == search_for:
       	found = True
       else:
           if search_for < l[location]:
           	slice_end = location - 1
           else:
           	slice_start = location + 1
   ```

6. Cek hasilnya :

   ```
   print(found)
   print(location)
   ```

   Kita akan mendapatkan output berikut :

   ```
   True
   4
   ```





### Fungsi Dasar

