GIS-PERTEMUAN KETIGA


Latar Belakang

Pada pertemuan ketiga matakuliah GIS disampaikan materi tentang retrieve data geospasial. Apakah itu retrieve data geospasial? Dan bagaimana melakukannya?


Pembahasan

Retrieve data geospasial adalah melakukan select/view data record dari file shapefile.  Caranya adalah dengan meng-import file-nya dan membaca file tersebut.


Membaca file dbf: 

sf.records()  -> membuka semua data record

sf.record(n)  -> membuka data record ke-n


Membaca file shp:

sf.shapes()  -> membuka semua geometri record

sf.shape(n)  -> membuka geometri record ke-n


Shape memiliki berbagai attribute, yaitu:

1) bbox atau boundary box adalah batas view melihat peta

2) parts adalah bagian-bagian dari shape.

3) points adalah koordinat. Nantinya akan menampung (x,y).

4) shapeType  adalah represnatasi dari tipe/jenis dari shape. Nantinya akan direpresentasikan dengan nomor.


Kesimpulan


Retrieve data geospasial adalah melakukan select/view data record dari file shapefile.  Kita dapat melakukannya dengan Cara meng-import file-nya terlebih dahulu dan membaca file tersebut. Kita dapat melakukannya di Python.