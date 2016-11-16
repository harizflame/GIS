GIS-PERTEMUAN KELIMA



Latar Belakang


Pada pertemuan kelima matakuliah GIS dijelaskan tentang membuat data geospasial. Bagaimana cara membuat data geospasial? Karena itu akan dijelaskan bagaimana cara melakukannya.



Pembahasan


Untuk membuat data geospasial, kita bisa melakukannya melalui python. Caranya adalah dengan melakukan dulu import shapefile lalu writing data shapefile-nya. Di bawah adalah cara membuat data geospasial melalui python.


-->membuat terlebih dahulu instance untuk class Writer

import shapefile
s = shapefile.Writer()


-->menambahkan geometri

s.point(x, y)

contoh:

s.point(1, 5)


# x dan y adalah sumbu, x adalah horizontal dan y adalah vertikal.


-->atau

s.point(x, y, z, m)

contoh: 

s.point(137, 27, 4, 8)


#z adalah elevasi dan m adalah measure.


-->melihat data yang dibuat

s.shapes()[0].points


# 0 di sini adalah urutan dari data yang kita buat, jadi 0 adalah data yang kita buat pertama tadi. Nanti akan menghasilkan point/koordinat [1,5]


--> membuat file dbf

s. field('nama', 'tipedata', 'panjang tipedata')

s.record('isi')


-->menyimpan file

s.shp('namafile.shp')

   save('namafile')



Kesimpulan


Jadi, kita dapat membuat data geospasial melalui python. Caranya adalah dengan meng-import shapefile terlebih dahulu lalu writing shapefile.