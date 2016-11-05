GIS-PERTEMUAN KEEMPAT


Latar Belakang


Pada pertemuan keempat matakuliah GIS dijelaskan kembali tentang Retrieve data geospasial. Terdapat tambahan materi tentang coding di python dan terdapat beberapa tambahan materi tentang geospasial , yaitu Polyline. Apakah itu Polyline?



Pembahasan


Untuk pembahasan tentang Retrieve data geospasial dapat dilihat di GIS-PERTEMUAN KETIGA. 


Tambahan materi:

Polyline adalah garis yang memiliki titik awal dan titik akhir akan tetapi kedua titik tersebut tidaklah bertemu sehingga tidak membentuk daerah. Contoh dari polyline adalah batas negara, batas, provinsi, dan batas daerah. Perbedaannya dengan line adalah bahwasanya polyline adalah segmen-segmen garis atau kumpulan berbagai titik(point) yang saling terhubung sedangkan line hanyalah memiliki satu segmen garis dan hanya memiliki dua titik saja. Polyline juga bisa disebut dengan polygonal chain.


Sedangkan polygon adalah garis yang memiliki titik awal dan titik akhir dan kedua titik tersebut bertemu sehinga membentuk daerah. Contoh dari polygon adalah daerah, pulau, dan negara.


Lalu untuk me-retrieve data geospasial, kita bisa melakukannya menggunakan python. Caranya adalah dengan melakukan import shapefile terlebih dahulu lalu select/view record data shapefilenya.


--> membaca semua geometri record

import shapefile

baca = shapefile.Reader("cultural.shp")

baca.shapes()


-->membaca geometri record ke-n (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

baca.shape(0)


--> membaca record atribut shapefile, shapeType (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

atribut = baca.shape(0)

atribut.shapeType


--> membaca record atribut shapefile, parts (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

atribut = baca.shape(0)

atribut.parts


--> membaca record atribut shapefile, bbox (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

atribut = baca.shape(0)

atribut.bbox


--> membaca record atribut shapefile, points (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

atribut = baca.shape(0)

atribut.points


--> membaca semua data record

import shapefile

baca = shapefile.Reader("cultural.shp")

baca.records()


--> membaca data record ke-n (sebagai contoh kita gunakan record ke-0)

import shapefile

baca = shapefile.Reader("cultural.shp")

baca.record(0)



--> mencari data record tertentu 

import shapefile

baca = shapefile.Reader("cultural.shp")

for a in sf.records():

if a[8] == "Indonesia":

print a


# code di atas akan mencari data record yang bernama "Indonesia", dan jika ada maka akan ditampilkan data record "Indonesia".





--> mengetahui urutan data record 

import shapefile

baca = shapefile.Reader("cultural.shp")

1=0

for a in sf.records():

if a[8] == "Indonesia":

print i

i = i+1


# code di atas akan memperlihatkan urutan keberapa data record "Indonesia" berada



Kesimpulan

Polyline adalah garis yang memiliki titik awal dan titik akhir akan tetapi kedua titik tersebut tidaklah bertemu sehingga tidak membentuk daerah sedangkan Polygon adalah garis yang memiliki titik awal dan titik akhir dan kedua titik tersebut bertemu sehinga membentuk daerah. Kita dapat membaca record shapefile menggunakan python dengan shapes() dan records().