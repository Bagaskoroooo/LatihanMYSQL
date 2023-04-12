# Latihan2 MYSQL
# Pertemuan 5
1. Membuat Database Dengan Nama latihan2

pertama kita membuat database latihan2 dengan perintah seperti dibawah

``` create database latihan2; ```

![ss1](https://user-images.githubusercontent.com/130354090/230882542-1f7ae8e9-e2f4-4605-af57-c5aa9290b334.png)

2. Menampilkan Semua Database

untuk menampilkan semua database yang pernah kita buat kita bisa menggunakan perintah seperti dibawah

``` show databases; ```

![ss2](https://user-images.githubusercontent.com/130354090/230883001-6627b0df-03e1-4621-b36e-fd3f0d388f4c.png)

3. Membuat Tabel Biodata Dengan Kolom Nama dan Alamat didalamnya

Sebelum kita membuat tabel, kita harus masuk terlebih dahulu kedalam database latihan2nya dengan perintah seperti dibawah

``` use latihan2; ```

selanjutnya kita membuat tabel dengan nama biodata dan menambahkan kolom nama dan alamat didalamnya dengan perintah seperti dibawah

``` create table biodata (nama VARCHAR(15), alamat VARCHAR(15)); ```

![ss3](https://user-images.githubusercontent.com/130354090/230884018-faf102c0-4e98-4eb3-9b89-11ffcaa1301c.png)

4. Membuat Kolom id Di Awal Tabel

Kita bisa menambahkan kolom id di awal tabel dengan perintah seperti dibawah

``` alter table biodata ADD id INT(11) FIRST; ```

![ss4](https://user-images.githubusercontent.com/130354090/230884537-9046ad16-8d35-4e82-ae7b-5223a0828302.png)

5. Menambahkan Kolom phone Setelah Kolom alamat

Selanjutnya adalah menambahkan kolom phone setelah kolom alamat dengan perintah seperti dibawah

``` alter table biodata ADD phone VARCHAR(15) AFTER alamat; ```

![ss5](https://user-images.githubusercontent.com/130354090/230884914-80993380-6a62-40bf-ab61-209f5bdf23d2.png)

6. Mengubah Tipe Data Kolom id Menjadi Tipe CHAR(11)

Kita bisa merubah tipe data yang telah kita input dengan cara seperti dibawah ini

``` alter table biodata MODIFY id CHAR(11); ```

![ss6](https://user-images.githubusercontent.com/130354090/230885492-65af822c-4527-4b08-9e3a-4f48f24ce778.png)

7. Mengubah Nama Kolom phone Menjadi hp dengan tipe VARCHAR(20)

Kita juga bisa mengubah nama kolom berserta dengan tipe datanya dengan cara seperti dibawah

``` alter table biodata CHANGE phone hp VARCHAR(20); ```

![ss7](https://user-images.githubusercontent.com/130354090/230885943-06f6176c-5f0f-4924-b5d1-67848c64c3ea.png)

8. Menambahkan Kolom email Setelah Kolom hp

Lalu kita tambahkan lagi kolom email setelah kolom hp dengan pertintah seperti dibawah

``` alter table biodata ADD email VARCHAR(15) after hp; ```

![ss8](https://user-images.githubusercontent.com/130354090/230886242-0d995e8d-ec75-4652-b362-37e501121b82.png)

9. Menghapus Kolom keterangan

Kita juga bisa menghapus salah satu kolom dengan perintah seperti dibawah

``` alter table biodata DROP COLUMN keterangan; ```

![ss9](https://user-images.githubusercontent.com/130354090/230886534-4f33a5d2-944b-4a97-ac66-149bcc70816f.png)

10. Mengganti Nama Dari Tabel Menjadi data_mahasiswa

Selanjutnya kita mengganti nama dari tabel kita dengan perintah seperti dibawah

``` alter table biodata RENAME TO data_mahasiswa; ```

![ss10](https://user-images.githubusercontent.com/130354090/230886837-885169c3-1d61-4b8c-b23d-e56cd17e012f.png)

11. Mengganti Nama Kolom id Menjadi nim

Lalu kita ganti lagi nama dari kolom id menjadi nim dengan perintah seperti dibawah

``` alter table data_mahasiswa CHANGE id nim CHAR(11); ```

![ss11](https://user-images.githubusercontent.com/130354090/230887154-962c5c25-aa82-4866-85b8-4425af79c7b8.png)

12. Menjadikan Kolom nim Sebagai PRIMARY KEY

Selanjutnya kita jadikan kolom nim menjadi PRIMARY KEY dengan perintah seperti dibawah

``` alter table data_mahasiswa ADD PRIMARY KEY (nim); ```

![ss12](https://user-images.githubusercontent.com/130354090/230887436-88df771c-d26f-4a44-bc8e-d90eb9681522.png)

13. Menjadikan Kolom email Sebagai UNIQUE KEY

Lalu kita jadikan kolom email menjadi UNIQUE KEY dengan peritah seperti dibawah ini

``` alter table data_mahasiswa ADD UNIQUE KEY (email); ```

![ss13](https://user-images.githubusercontent.com/130354090/230887696-7a3a1791-4db8-4ecc-8254-45f18d872983.png)

14. HASIL AKHIR OUTPUT DARI DATABASE

![ss14](https://user-images.githubusercontent.com/130354090/230887928-82f64419-b237-4cbc-918d-ef488a7d8052.png)


## Apa Maksud Dari int (11)? 

Yang dimaksud int(11) artinya suatu data yang dipakai atau digunakan menggunakan tipe data int atau integer dengan length atau panjang karakter 11.

## Apa Yang Dimaksud Dengan Kolom Null Yang Berisi Yes Dan No?

Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang berisi Yes dan No. Apa maksudnya? Apabila Null berisi no, maka data tersebut nantinya akan dilakukan pengisian atau penginputan. Sedangkan apabila Null berisi yes, maka artinya data tersebut akan dikosongkan atau tidak dilakukan penginputan.

