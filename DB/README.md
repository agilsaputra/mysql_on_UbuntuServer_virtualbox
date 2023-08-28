### konfigurasi mysql di server serta konesi ke dbeaver dan mysql workbench

#### instalasi mysql
 - setelah melakukan instalasi dan koneksi ssh [instalasi dan koneksi ssh](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/blob/master/README.md)
 - install mysql seperti biasa di server ubuntu kalian
   ```
   sudo apt update
   sudo apt install mysql-server
   ```
 - setelah itu masuk mysql
   ```
   sudo mysql -u root
   ```
 - download DB_karyawan.sql di git saya atau bisa di clone 
   ```https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/tree/master/DB```
 - setelah itu move file dari local ke server
 - cek ip server terlebih dahulu 
   ```
   ssh username@localhost -p 2222
   ```
 - setelah login ketik ifconfig
 - buka terminal lagi untuk jadi tampilah seperti dibawah
   ![Screenshot from 2023-08-28 20-12-32](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/d1d0b532-d25c-4a12-8b6f-83f4143519b0)
 - yang kanan adalah terminal server saya ip nya yaitu ```10.0.2.15```
 - masuk di directory ```DB_karyawan.sql``` yang kalian download tadi
 - masuk terminal di directory dan copy file dari terminal local ke server
   ```
   sudo scp -P 2222 DB_karyawan.sql nama_username@ip_address:/file/path/diserver
   ```
   ```
   scp -P 2222 DB_karyawan.sql gandalfserver@localhost:~
   ```
![Screenshot from 2023-08-28 22-06-38](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/20bae750-cf74-4c0f-b26f-78bdb6ae0025)
 - setelah itu restore sql dari server
 - create database baru lalu restore
   ```
   create database nama_database
   ```
   ```
   mysql -u username -p nama_database < DB_karyawan.sql
   ```
 - sekarang mysql sudah berada di server

#### akses mysql dengan dbeaver dan mysql workbench
 #### konfigurasi dbeaver
 - install dbeaver
   ```
   sudo apt install dbeaver-ce
   ```
 - setelah berhasil install dbeaver buat koneksi dengan mysql server
   ![Screenshot from 2023-08-28 22-24-40](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/4886f4e7-3d2c-4b08-bf68-24ea517d11b6)
![Screenshot from 2023-08-28 22-25-28](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/4cf4d887-407f-4dcc-8d33-7f300c5898c0)

 - setting ip host server, port, database_username, database_password serta username_server dan password
 - setelah itu kalian bisa melakukan query dengan mudah di dbeaver
   
![Screenshot from 2023-08-28 22-30-55](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/f0a0e520-9697-40c1-b854-a010b6d272c1)

 #### konfigurasi mysql workbench melihat schema database
 - install mysql workbench 
  ```
  sudo apt install mysql-workbench
  ```
  - setelah install selesai jalakan mysql workbench lalu buat koneksi
  - pilih connection method standard TCP/IP over SSH
    ![Screenshot from 2023-08-28 22-35-20](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/a0a449cf-c4ca-4ab1-941f-a4cd20fa5195)

  - isikan  ip host server, port, database_username, database_password serta username_server dan password
  - setelah berhasil akan muncul seperti ini
    ![Screenshot from 2023-08-28 22-42-17](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/d3dc9714-7ed5-4cbf-98c8-55b26c9bcbce)
    - untuk melihat schema database kalian bisa klik database lalu reverse engineer
    - koneksikan seperti tadi dan pilih database
    - berikut schema yang akan didapatkan
   
![SCHEMA_DB](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/728c66af-f355-4368-84aa-d74e6ed075ab)
