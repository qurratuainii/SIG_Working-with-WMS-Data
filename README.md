# SIG_Working-with-WMS-Data

*Tutorial Working with WMS Data

1. Buka QGIS dan klik Open Data Source Manager (*Gambar 1*)

2. Pada Data Source Manager beralih ke WMS/WMTS, lalu klik new (*Gambar 2*)

3. Pada new WMS/WMTS Connection dialog, masukkan nama sebagai SEDAC dan tempel URL yang disalin di kotak teks URL. Klik OK, Jika kita mendapatkan kesalahan dengan URL yang disalin, bisa dengan alternatif lainnya dengan https://sedac.ciesin.columbia.edu/geoserver.wms (*Gambar 3*)

4. Selanjutnya pada Data Source Manager dialog, kik Connect. Semua layer yang tersedia akan dimuat. Kita akan melihat ID yang berbeda terdaftar di sebelah layer. ID 0 nerarti kita mendapatkan peta semua layer. Jikakita tidak menginginkan semua layer, kita dapat memperluas daftar dengan mengklik ikon dan memilih layer yang diinginkan (*Gambar 4*)

5. Pada tutorial ini kita akan melihat layer tertentu. Cari Probabilities of Urban Expansiion to 2030. Pilih versi default layer ekspansi perkotaan 2030 (*Gambar 5*)

6. Pada bagian pengkodean gambar, kita harus memilih format gambar. Format gambar itu penting, dan itu tergantung pada kasus penggunaan. Berdasarkan perspektif pengguna berikut adalah 

- Quality: kompresi file untuk PNG adalah lossless, untuk JPEG ini adalah kompresi lossy dan TIFF dapat berupa keduanya. Itu berarti kualitas PNG akan lebih baik dibandingkan dengan JPEG. Jika tujuan utama adalah mencetak peta gunakan PNG

- Speed: karena gambar PNG tidak terkompresi dan dengan demikian ukurannya lebih besar, mereka akan membutuhkan waktu lebih lama untuk dimuat. Jika kita menggunakan lapisan dalam proyek kita sebagai lapisan referensi dan perlu banyak memperbesar/menggeser, gunakan JPEG

- Client support: QGIS mendukung sebagian besar format, tetapi jika kita mengembangkan aplikasi web, browser biasanya tidak mendukung TIFF, jadi kita harus memilih format lain

- Type of data: jika lapisan sebagian besar adalah vektor, PNG akan memberikan hasil yang lebih baik. Untuk lapisan citra, JPEG biasany merupakan pilihan yang lebih baik

7. Sekarang layer Probabilities of Urban Expansion to 2030 akan dimuat ke kanvas. Gunakan zoom/pan untuk menjelajahi lapisan. Cara kerja layanan WMS adalah setiap kali kita memperbesar.menggeser, ia mengirimkan koordinat area pandang kita ke server membuat gambar untuk area pandang tersebut dan mengembalikannya ke client. Jadi, akan ada beberapa penundaan sebelum kita melihat gambar untuk area tersebut setelah kita memperbesar. Oleh karena itu, koneksi internet selalu diperlukan untuk mengakses lapisan ini (*Gambar 6*)

8. Sekarang, perbesar ke tempat yang diketahui dan klik ikon identify Features di toolbar (*Gambar 7*)

9. Klik pada sembarang pixel di kanvas, itu akan muncul kotak dialog dengan nilai value. Ini adalah nilai pixel dalam lapisan yang menunjukkan kemungkinan bahwa pixel akan mengalami urbanisasi pada tahun 2030. Karena layer tidak disimpan secara lokal, nilai-nilai ini diambil dari penyedia layanan. Kita dapat melihat hasilnya lebih baik dengan memilih format HTML dan view tree (*Gambar 8*)

10. Untuk melihat, informasi tambahan tentang layer klik kanan pada layer dan pilih Properties (*Gambar 9*)

11. Pada Layer Properties dialog, alihkan ke tab Information di sini semua informasi seperti penyedia data, proyeksi, jangkauan dapat ditemukan. Klik OK untuk menutup kotak dialog (*Gambar 10*)

12. Pada QGIS browser, cari XYZ Tiles dan klik lalu seret OpenStreetMap ke kanvas (*Gambar 11*)

13. Klik pada ikon panel Open the Layer Styling dan berlih ke Transparency (*Gambar 12*)

14. Atur Global opacity menjadi 50% (*Gambar 13*)

15. Sekarang di kanvas Lapisan Urban dapat dieksplorasi dengan referensi geografis (*Gambar 14*)

16. Untuk mendapatkan lebih banyak akses ke transparency layer, klik kanan pada layer lalu pilih Properties (*Gambar 15*)

17. Pada Layer Properties, alihkan ke tab Legend, di bawah widget yang tersedia pilih penggeser Opacity dan klik tambah ikon widget yang dipilih. lalu klik OK (*gambar 16*)

18. Sekarang widget slider akan tersedia untuk mengontrol opacity layer (*Gambar 17*)
