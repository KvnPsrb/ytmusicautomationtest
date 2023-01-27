# ytmusicautomationtest

Project ini merupakan rincian alur dalam melakukan proses pengujian otomatisasi yang telah saya lakukan dalam menguji website [Youtube Music](https://music.youtube.com) menggunakan Selenium IDE dengan bahasa pemrograman Python (Anaconda Prompt)

**Tools yang dibutuhkan** :
- [Python 3.11](https://www.python.org/downloads/)
- [PyCharm Community Version](https://www.jetbrains.com/pycharm/download/#section=windows)
- [Selenium IDE](https://www.selenium.dev/selenium-ide/)
- [Anaconda Distribution](https://www.anaconda.com/products/distribution)
- [Chrome Browser](https://www.google.com/chrome/)

**Berikut adalah langkah2 nya :**

1. Langkah pertama yaitu pastikan sudah menginstal Python, PyCharm, dan Selenium IDE sebelum memulai melakukan pengujian otomatisasi. Dalam project ini saya menggunakan Python sebagai bahasa pemrogramannya, PyCharm sebagai software IDE dalam pengolahan kode nya, Selenium IDE sebagai alat dalam perekaman dan pengujian websitenya, dan Anaconda Distribution sebagai media penginstalan paket dan dependensi sekaligus media dalam menjalankan skrip pengujian otomatisasi (lebih lanjut nantinya yang digunakan hanyalah Anaconda Prompt).

2. Setelah semua terinstal, maka langkah selanjutnya yaitu dengan membuka Anaconda Prompt dan mulai untuk menginstal semua paket dan dependensi yang diperlukan. Untuk perintah yang perlu dijalankan dalam melakukan penginstalan akan dijelaskan dibawah ini:

   - Untuk penginstalan paket Selenium
     > conda install -c conda-forge selenium
  
   - Untuk penginstalan dependensi Selenium IDE
     > npm install -g selenium-side-runner
  
   - Untuk penginstalan browser driver (di project ini saya menggunakan Chrome Browser)
     > npm install -g chromedriver

3. Setelah command diatas berhasil, maka langkah selanjutnya yaitu dengan membuka Selenium IDE yang sudah diinstal pada browser yang akan digunakan dalam pengujian website. Jika sudah terbuka, maka pilih bagian yang ditunjuk panah pada gambar dibawah ini (untuk membuat project baru):

&ensp;&ensp;&ensp;&ensp;![Side_1](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_1.PNG)

4. Selanjutnya isi nama dari project yang ingin dibuat.

&ensp;&ensp;&ensp;&ensp;![Side_2](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_2.PNG)

5. Lalu, isi URL link yang ingin diuji. Disini saya memilih URL music.youtube.com/explore karena pada halaman ini tampilan antarmukanya tidak berubah-ubah, sehingga memudahkan dalam proses pengujian. Setelah itu klik "Start Recording".

&ensp;&ensp;&ensp;&ensp;![Side_3](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_3.PNG)

6. Maka akan langsung diarahkan kepada website yang akan diuji berdasarkan URL link yang sudah diisi sebelumnya seperti gambar dibawah ini.

&ensp;&ensp;&ensp;&ensp;![Side_4](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_4.PNG)

   * Seperti yang tertera pada gambar, pada bagian bawah kanan disampaikan bahwa Selenium IDE sedang melakukan perekaman, karena memang pada tahapan ini akan dilakukan perekaman mengenai fitur-fitur yang ada pada website YT Music sesuai dengan test case yang akan diimplementasikan. Dalam project ini saya memilih test case dalam memutar dan menjeda lagu yang dimainkan, karena menurut saya fitur ini merupakan yang terpenting dalam aplikasi streaming musik. Cara untuk mendapatkan data rekamannya yaitu dengan melakukan alur penggunaan fitur yang sebenarnya. Jika sudah selesai maka kembali kepada halaman aplikasi Selenium IDE dan hentikan rekaman.

7. Jika rekaman telah dihentikan, maka akan muncul pop-up pemberian nama dari test nya. Saya menganjurkan untuk menamai test nya sesuai dengan apa yang diuji seperti gambar dibawah ini:

&ensp;&ensp;&ensp;&ensp;![Side_5](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_5.PNG)

8. Jika sudah tersimpan, maka test nya akan menampilkan tahapan-tahapan yang sudah dilakukan pada proses rekaman sebelumnya. Setelah itu simpan project yang sudah dibuat dengan menekan tombol Save pada bagian atas kanan atau dengan menekan CTRL+S pada keyboard. Perlu diingat pada tempat project disimpan karena nantinya project akan dijalankan pada Anaconda Prompt.

&ensp;&ensp;&ensp;&ensp;![Side_6](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_6.PNG)

9. Setelah project tersimpan, maka langkah selanjutnya yaitu dengan melakukan ekspor terhadap individu test yang sudah dibuat. Caranya dengan mengklik bagian kanan pada mouse di bagian nama test nya lalu pilih "Export", nanti akan muncul pop-up seperti gambar dibawah ini:

&ensp;&ensp;&ensp;&ensp;![Side_7](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_7.PNG)

   * Karena dalam project ini saya menggunakan Python, maka pilih Python pytest untuk jenis file yang akan terekspor disertai dengan mencentang bagian pertama dan kedua checkbox. Hal ini bertujuan untuk menyimpan variabel yang diperoleh saat melakukan proses perekaman kedalam script yang akan dibentuk. Perlu diingat pada tempat test ini disimpan karena nantinya test ini juga akan dijalankan pada Anaconda Prompt sehingga saya menyarankan untuk menyimpan test ini ditempat project tersimpan.

10. Setelah tersimpan maka hasil ekspor dapat kita akses melalui IDE yang kita miliki (disini saya menggunakan PyCharm) untuk melihat script yang dibentuk berdasarkan proses perekaman yang sudah dilakukan. Untuk lihat lebih lanjut dapat diakses pada file [ini](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/test/test_playandpausebutton.py)

11. Setelah semua file berhasil disimpan, maka langkah selanjutnya yaitu dengan membuka kembali Anaconda Prompt dan mengetik command seperti pada gambar dibawah ini:

&ensp;&ensp;&ensp;&ensp;![Side_Runner](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/side_runner.PNG)

   * Command ini akan menjalankan pengujian otomatisasi dari project yang sudah dibuat berdasarkan rekaman yang telah dilakukan sebelumnya. Setelah dijalankan maka disaat proses berlangsung akan muncul pop-up browser yang berjalan secara otomatis berdasarkan rekaman yang sudah dibuat. Setelah proses selesai maka hasilnya akan seperti pada gambar dibawah ini:

&ensp;&ensp;&ensp;&ensp;![Side_Runner_Result](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/sr_result.PNG)

   * Gambar tersebut memberikan laporan mengenai hasil proses pengujian otomatis dari website yang diuji apakah lolos atau gagal berdasarkan rekaman yang ada pada project tersebut.

12. Setelah menjalankan pengujian berdasarkan project yang dibuat, maka akan dilakukan kembali pengujian berdasarkan individu test yang ada pada project tersebut yang sudah diekspor sebelumnya. Command dalam melakukan pengujiannya seperti gambar di bawah ini:

&ensp;&ensp;&ensp;&ensp;![Pytest](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/pytest.PNG)

   * Command ini akan menjalankan pengujian otomatisasi dari test yang sudah diekspor dari preject yang sudah dibuat berdasarkan rekaman yang telah dilakukan sebelumnya. Sama seperti sebelumnya, setelah dijalankan maka disaat proses berlangsung akan muncul pop-up browser yang berjalan secara otomatis berdasarkan rekaman yang sudah dibuat pada test tersebut. Setelah proses selesai maka hasilnya akan seperti pada gambar dibawah ini:

&ensp;&ensp;&ensp;&ensp;![Pytest_Result](https://raw.githubusercontent.com/KvnPsrb/ytmusicautomationtest/main/src/docs/pytest_result.PNG)

   * Gambar tersebut memberikan laporan mengenai hasil proses pengujian otomatis dari website yang diuji apakah lolos atau gagal berdasarkan rekaman yang ada pada test tersebut. 

   * Melihat akan hasil yang diperoleh sekilas sama, namun yang membedakan adalah jika yang dijalankan adalah project dalam proses pengujian, maka seluruh test yang ada pada project tersebut akan dijalankan semua, sedangkan jika ingin menjalankan test secara individu maka lebih tepat menjalankan proses individu test nya seperti pada tahapan ke-12.


Sekian dari project yang sudah saya lakukan, kurang lebihnya mohon maaf, dan saya benar-benar mengharapkan adanya feedback yang dapat saya terima dari project saya ini karena saya menyadari masih ada yang dapat disempurnakan dari project ini. Terima kasih atas perhatiannya.

