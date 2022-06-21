<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links -->


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h2 align="center">Laporan Praktikum</h2>
  <p align="center">
    Kharisma Ayu Pradani (221911095, 3SD1) <p>
  <p align="center">
    Dosen Pembimbing: Farid Ridho, S.S.T., M.T. <p>
</div>

#
#

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#pendahuluan">Pendahuluan</a>
    </li>
    <li>
      <a href="#metodologi">Metodologi</a>
    </li>
    <li>
      <a href="#hasil-dan-pembahasan">Hasil dan Pembahasan</a>
      <ul>
        <li><a href="#a-pengolahan-data">Pengolahan Data</a></li>
        <li><a href="#b-eksekusi-data">Eksekusi Data</a></li>
        <li><a href="#c-visualisasi-data">Visualisasi Data</a></li>
        <li><a href="#d-membuat-fungsi-memilih-grafik">Membuat Fungsi Memilih Grafik</a></li>
        <li><a href="#e-membuat-dashboard">Membuat Dashboard</a></li>
      </ul>
    </li>
    <li><a href="#kesimpulan">Kesimpulan</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
# Dashboard Iteraktif Data Infrastruktur Indonesia Tahun 2020 Menggunakan Aplikasi Tableau

<!-- PENDAHULUAN -->
## Pendahuluan

Pembangunan infrastruktur suatu negara merupakan pondasi untuk negara tersebut meningkatkan aspek kehidupan masyarakat, bahkan untuk berkompetisi dengan negara lain dalam banyak bidang. Dengan memahami keadaan infrastruktur yang ada di Indonesia, bisa menjadikan pembangunan infrastruktur menjadi lebih efektif dan efisien. Dashboard interaktif merupakan salah satu dari bentuk visualisasi atau penyampaian data yang dianggap baik menjalankan fungsinya. Sehingga dalam penelitian ini bertujuan untuk membangun sebuah dashboard data interaktif yang tepat untuk data infrastruktur yang digunakan (Statistik Infrastruktur Indonesia 2020) dengan memanfaatkan aplikasi Tableau Public sehingga penyampaian data kepada masyarakat maupun pihak manapun yang menggunakan data bisa memahami keadaan infrastruktur Indonesia dengan baik

<p align="right">(<a href="#top">back to top</a>)</p>

## Metodologi

Dalam pengumpulan data untuk penelitian ini, diperoleh dari data Statistik Infrastruktur Indonesia 2020 yang tersedia pada web bps.go.id. Dalam data set ini, terdapat banyak set data, data tersebut terdiri dari data untuk 16 infrastruktur di Indonesia, yaitu berupa jumlah SD, MI, SMP, MTs, SMA, MA, SMK, perguruan, rumah sakit, puskesmas, penginapan, koperasi, pasar, BUMDes, lumbung, dan bank..
Data lain yang digunakan dalam penelitian ini yaitu data latitude dan longitude daerah di Indonesia. Data geografi ini didapatkan dari gadm.org. Data geografi yang didapatkan memiliki format .shp.

<a>
  <img src="images\Metodologi.png" alt="Metodologi" width="250">
</a>

<p align="right">(<a href="#top">back to top</a>)</p>

## Hasil dan Pembahasan

### A. Pengolahan Data

Data yang digunakan dalam penelitian ini merupakan data infrastruktur Indonesia tahun 2020, dimana data ini terdiri dari jumlah infrastruktur pada masing masing provinsi di seluruh Indonesia. Dari sumber yang didapatkan, data memiliki format .xlsx dimana data tersebut diperoleh dari publikasi BPS pada bps.go.id. Data tersebut terdiri dari data untuk 16 infrastruktur di Indonesia, yaitu berupa jumlah SD, MI, SMP, MTs, SMA, MA, SMK, perguruan, rumah sakit, puskesmas, penginapan, koperasi, pasar, BUMDes, lumbung, dan bank. Dimana dari 18 data tersebut memiliki filter masing masing, seperti pada data pendidikan di klasifikasikan dengan swasta atau negeri. Data tersebut memiliki 34 banyak baris atau data tiap kategorinya. Hal ini dikarenakan pada data tersebut menjelaskan jumlah infrastruktur tiap provinsi. Data jenis ini akan dimasukkan ke dalam aplikasi Tableau publik sebagai data Microsoft Excel.

<a>
  <img src="images\new.png" alt="new">
</a>

Selain menggunakan data infrastruktur tersebut, juga didapatkan data latitude dan longitude daerah di Indonesia yang nantinya akan digunakan sebagai alat bantu penyajian data dan sebagai filter interaktif. Data geografi ini didapatkan dari gadm.org. Data geografi yang didapatkan memiliki format .shp. Saat mengunduh data geografi Indonesia, nantinya akan di peroleh 4 data .shp dimana tiap data tersebut memiliki batasan yang berbeda. Dikarenakan visualisasi yang di inginkan adalah visualisasi per provinsi, maka akan digunakan data dengan nama gadm36_IDN_1.shp karena pada data tersebutlah yang mengandung informasi geografi. Data sejenis ini akan dimasukkan ke pada Tableau publik sebagai spasial data.

<p align="right">(<a href="#top">back to top</a>)</p>

### B. Eksekusi Data

Pada tahapan ini akan menjelaskan proses pengeksekusian data. Penjelasan dari  proses eksekusi data adalah sebagai berikut.

1) Memasukkan Data:

Memasukkan data ke dalam Tableau serta membaca data masukan yang akan diproses, dimana data tersebut bertipe data .xlsx dan data .shp.

<a>
  <img src="images\Pengolahan data.png" alt="Pengolahan Data">
</a>

1) Menghubungkan Data

Pada proses ini, dilakukan penghubungan baik antara kedua data yang dimiliki, hingga penghubungan dengan aplikasi Tableau. Adapun proses penghubungannya diperlihatkan dalam gambar di bawah ini.

<a>
  <img src="images\datasource.png" alt="Datasource">
</a>

Pada gambar tersebut, terlihat bahwa terdapat 3 sheet data untuk data infrastruktur. Ketiga data tersebut digabungkan dengan data geometri provinsi Indonesia dengan cara menyamadengankan variabel Name 1 pada data geometri dimana variabel tersebut merupakan nama provinsi di Indonesia dengan variabel Provinsi yang ada pada data infrastruktur. Sehingga nantinya akan bisa menghasilkan data interaktif, dimana saat kita melakukan suatu proses yang melibatkan provinsi, baik data pada geometri Indonesia maupun data infrastruktur akan sama sama terproses.

3) Pengolahan Data:

Setelah menghubungkan data yang dimiliki ke dalam datasource, maka yang dilakukan selanjutnya adalah mengolah data tersebut hingga menjadi keluaran yang diinginkan.

<p align="right">(<a href="#top">back to top</a>)</p>

### C. Visualisasi Data

Pada tahap ini, akan dilakukan pengvisualisasian menggunakan Tableau sesuai dengan yang dibutuhkan oleh dashboard.

1) Tampilan peta Provinsi di Indonesia:

Pembuatan pet aini dilakukan dengan cara menarik variabel latitude dan lonngitude yang berasal dari data gadm36_IDN_1.shp dan memasukkan sebagai kolom dan baris. Data ditampilkan dalam bentu peta. Untuk menambah penjelas perbatasan antar provinsi, ditambahkan filter berupa nama provinsi ke dalam colour dan mengubah pallete pada colour tersebut dengan warna merah-emas untuk menambah keindahan visualisasi. Tampilan pembuatan visualisasi data Indonesia ditampilkan pada gamber beikut.

<a>
  <img src="images\peta.png" alt="Peta">
</a>

2) Grafik banyaknya infrastrutur berupa SD/MI

Pada pembuatan grafik ini, bertujuan untuk membandingkan jumlah infrastruktur berupa SD dan MI yang ada pada masing masing provinsi serta membandingkan julah berdasarkan jenisnya, yaitu swasta dan negeri. Kedua data tersebut digabungkan karena pada dasarnya, kedua infrastruktur tersebut memiliki tujuan, fungsi dan kurikulum secara umum tidak terlalu jauh. Dalam pembuatannya dilakukan dengan cara memasukkan data SD dan MI ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis sekolah sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang negeri mana yang swasta, dan mana yang SD mana yang MI. Penyajian grafik tersebut ditampilkan secara terurut beedasarkan jumlah infrastruktur yang bersangkutan yang dalam hal ini merupakan data SD dan MI.

<a>
  <img src="images\sdmi.png" alt="SD/MI">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Barat memiliki jumlah infrastruktur SD/MI tertinggi. Dilanjutkan oleh Jawa Timur dan Jawa Tengah.

3) Grafik banyaknya infrastrutur berupa SMP/MTs

Begitu juga pada pembuatan grafik yang satu ini. Grafik ini juga bertujuan untuk membandingkan banyaknya infrastruktur SMP/MTs pada tiap provinsi. Dengan alasan yang sama , kedua data tersebut disatukan dalam pembuatan visualisasinya pada Tableau. Dalam pembuatannya dilakukan dengan cara memasukkan data SMP dan MTs ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis sekolah sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang negeri mana yang swasta, dan mana yang SMP mana yang MTs. 
 
<a>
  <img src="images\smpmts.png" alt="SMP/MTs">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Barat juga memiliki jumlah infrastruktur SMP/MTs tertinggi. Dilanjutkan oleh Jawa Timur dan Jawa Tengah.

4) Grafik banyaknya infrastrutur berupa SMA/MA

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur SMA/MA pada tiap provinsi. Dengan alasan yang sama , kedua data tersebut disatukan dalam pembuatan visualisasinya pada Tableau. Dalam pembuatannya dilakukan dengan cara memasukkan data SMA dan MA ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis sekolah sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang negeri mana yang swasta, dan mana yang SMA mana yang MA.
 
<a>
  <img src="images\smama.png" alt="SMA/MA">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timur memiliki jumlah infrastruktur SMA/MA tertinggi. Dilanjutkan oleh Jawa Barat dan Sumatra Utara.

5) Grafik banyaknya infrastrutur berupa SMK
 
Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur SMK pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data SMK ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis sekolah sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang negeri mana yang swasta. Dari tampilan di atas, diketahui pahwa provinsi Jawa Barat juga memiliki jumlah infrastruktur SMK tertinggi. Dilanjutkan oleh Jawa Timur dan Jawa Tengah.

<a>
  <img src="images\smk.png" alt="SMK">
</a>

6) Grafik banyaknya infrastrutur berupa perguruan tinggi

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur perhuguruan tinggi pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data perguruan ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis sekolah sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang negeri mana yang swasta.
 
<a>
  <img src="images\pt.png" alt="Perguruan Tinggi">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Barat juga memiliki jumlah infrastruktur perguruan tinggi tertinggi. Dilanjutkan oleh Jawa Timur dan Jawa Tengah.

7) Grafik banyaknya infrastrutur berupa rumah sakit

Pada pembuatan grafik yang satu ini bertujuan untuk membandingkan banyaknya infrastruktur rumah sakit pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data rumah sakit ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis rumah sakit sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan rumah sakit umum, mana yang merupakan rumah sakit bersalin.
 
<a>
  <img src="images\rs.png" alt="Rumah Sakit">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timur memiliki jumlah infrastruktur rumah sakit tertinggi. Dilanjutkan oleh Jawa Barat dan Jawa Tengah.

8) Grafik banyaknya infrastrutur berupa puskesmas

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur puskesmas pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data puskesmas ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis puskesmas sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan puskesmas rawat inap, mana yang merupakan puskesmas tanpa rawat inap.
 
<a>
  <img src="images\puskesmas.png" alt="Puskesmas">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Barat juga memiliki jumlah infrastruktur puskesmas tertinggi. Dilanjutkan oleh Jawa Timur dan Jawa Tengah.

9) Grafik banyaknya infrastrutur berupa hotel dan penginapan

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur berupa hotel dan penginapan pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data penginapan ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis penginapan sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan hotel, mana yang merupakan penginapan.
 
<a>
  <img src="images\penginapan.png" alt="Hotel & Penginapan">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Bali memiliki jumlah infrastruktur hotel dan penginapan tertinggi. Dilanjutkan oleh Jawa Barat dan Jawa Timur.

10)   Grafik banyaknya infrastrutur berupa BUMDes

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur BUMDes pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data BUMDes ke dalam kolom, dan provinsi ke dalam baris.
 
<a>
  <img src="images\bumdes.png" alt="BUMDes">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timur memiliki jumlah infrastruktur BUMDes tertinggi. Dilanjutkan oleh Aceh dan Jawa Tengah.

11)  Grafik banyaknya infrastrutur berupa embung

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur embung pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data embung ke dalam kolom, dan provinsi ke dalam baris. 
 
<a>
  <img src="images\embung.png" alt="Embung">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Nusa Tenggara Timur memiliki jumlah infrastruktur embung tertinggi. Dilanjutkan oleh Sulawesi Selatan dan Jawa Timur.

12)  Grafik banyaknya infrastrutur berupa bank

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur bank pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data bank ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis bank sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan bank perkreditan rakyat, mana yang merupakan bank umum pemerintah, dan mana yang merupakan bank umum swasta.
 
<a>
  <img src="images\bank.png" alt="Bank">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timur memiliki jumlah infrastruktur bank tertinggi. Dilanjutkan oleh Jawa Barat dan Jawa Tengah.

13) Grafik banyaknya infrastrutur berupa pasar
    
Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur pasar pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data pasar ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis pasar sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan pasar dengan bangunan permanen, mana yang merupakan pasar dengan bangunan yang semi permanen, dan mana yang merupakan pasar tanpa bangunan.

<a>
  <img src="images\pasar.png" alt="Pasar">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timur juga memiliki jumlah infrastruktur Pasar tertinggi. Dilanjutkan oleh Jawa Tengah dan Jawa Barat.

14)	Grafik banyaknya infrastrutur berupa koperasi

Pada pembuatan grafik yang satu ini juga bertujuan untuk membandingkan banyaknya infrastruktur koperasi pada tiap provinsi. Dalam pembuatannya dilakukan dengan cara memasukkan data koperasi ke dalam kolom, dan provinsi ke dalam baris. Lalu di masukkan variabel jenis koperasi sebagai colour pada graf tersebut sehingga kita bisa tahu mana yang merupakan koperasi simpan pinjam, mana yang merupakan kopinkra/ milik usaha mikro, mana yang merupakan koperasi unit desa, dan mana yang merupakan koperasi lainnya.
 
<a>
  <img src="images\koperasi.png" alt="Koperasi">
</a>

Dari tampilan di atas, diketahui pahwa provinsi Jawa Timurjuga memiliki jumlah infrastruktur Koperasi tertinggi. Dilanjutkan oleh Jawa Tengah dan Jawa Barat.

15)	Tabel rangkuman data infrastruktur

Tabel ini dibuat untuk menampilkan data tiap variabel infrastruktur. Yang ditampilkan adalah berupa nilai total infrastruktur teresebut. Yang nantinya akan dibuat interaktif sehingga akan berupah tergantung filter provinsi yang dipilih. Table tersebut di buat dengan cara memasukkan measure name ke dalam kolom, dan memasukkan sum nilai semua variabel infrastruktur satu per satu.
 
<a>
  <img src="images\rangkuman.png" alt="Rangkuman">
</a>

<p align="right">(<a href="#top">back to top</a>)</p>

### D. Membuat Fungsi Memilih Grafik

Pada Langkah ini, dibentuk suatu parameter baru bernapa PilihGraph yang nantinya akan digunakan untuk memilih grafik mana yang akan muncul dalam dashboard. Tipe data pada parameter ini diatur sebagai string dan nilainya berupa list. Sehingga kita bisa memasukkan nama grafik yang menjadi pilihan pada parameter tersebut. 
 
<a>
  <img src="images\pilihgraph.png" alt="Pilih Graph">
</a>

Setelah membuat parameter tersebut, dibuatlah sebuah calculation pada Tableau yang nantinya akan dijadikan sebuah filter pada grafik masing masing sehingga pada saat digunakan, yang tampil hanya akan grafik yang diinginkan saja. Berikut merupakan isi dari kalkulasi yang diberi nama PilihGraphCalc. 
 
<a>
  <img src="images\pilihgraph calc.png" alt="Pilih Graph Calc">
</a>

<p align="right">(<a href="#top">back to top</a>)</p>
### E. Membuat Dashboard

Setelah mempersiapkan semua kebutuhan, mulai dari peta, grafik yang dibutuhkan, table rangkuman, dan hingga parameter serta kalkulasi, maka semua sheet tersebut digabungkan menjadi satu dashboard yang memiliki penampilan sebagai berikut
 
<a>
  <img src="images\dashboard.png" alt="Dashboard">
</a>

Untuk mewujudkan dashboard yang iterative, pada dashboard tersebut, peta di atur sebagai filter. Sehingg saat kita memilih suatu provinsi yang ada pada peta, akan memunjulkan graf khusus daerah tersebut dan rangkuman infrastruktur provinsi tersebut. Dengan menggunakan parameter dan kalkulasi yang telah dibuat sebelumnya, pada bagian kanan atas, bisa dilakukan pemilihan grafik mana yang ingin di tampilkan pada dashboard. 
Penyusunan dashboard dilakukan dengan rapi dan terorganisir. Sehingga pembaca bisa melihat informasi yang diinginkan dengan lebih mudah, serta akan memudahkan pengambilan keputusan yang berkaitan dengan infrastruktur Indonesia. Hasil dashboard tersebut bisa di akses melalui [link Tableau Public](https://public.tableau.com/app/profile/kharisma.ayu.pradani/viz/DASHBOARDINFRASTRUKTURINDONESIA2020/Dashboard1).
<p align="right">(<a href="#top">back to top</a>)</p>

### F. Pengujian

Pengujian dilakukan untuk mengecek tidak adanya kesalahan dalam proses interaktif dalam dashboard ini. Pengujian dilakukan dengan melakukan percobaan pada tiap fungsi interaktif.

Hasil dari pengujian tersebut, didapatkan dari 20 skenario yang dilakukan, banyaknya nilai berhasil sebanyak 20 dan gagal sebanyak 0. Sehingga bisa dikatakan bahwa implementasi fungsi yang dijalankan telah memenuhi kebutuhan akan dashboard interaktif.
<p align="right">(<a href="#top">back to top</a>)</p>

## Kesimpulan

Sumber data yang didaptkan dari bps.go.id berupa publikasi infrastruktur Indonesia tahun 2020 dapat divisualisasikan dengan menggunakan bantuan aplikasi Tableau Public menjadi sebuah dashboard interaktif. Dashboard dibuat dengan baik, rapi, sistematis, serta fungsi interaktif dapat dilakukan secara lancar, sehingga pembaca bisa melihat informasi yang diinginkan dengan lebih mudah, serta akan memudahkan pengambilan keputusan yang berkaitan dengan infrastruktur Indonesia.

<p align="right">(<a href="#top">back to top</a>)</p>

#

<!-- CONTACT -->
## Contact

Your Name - Kharisma Ayu Pradani [221911095] - 221911095@stis.ac.id

<p align="right">(<a href="#top">back to top</a>)</p>
