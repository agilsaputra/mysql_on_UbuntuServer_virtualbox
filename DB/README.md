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
 - sekarang copy file dari terminal local sebelah kiri punya saya
   ```
   sudo scp DB_karyawan.sql nama_username@ip_address:/file/path/diserver
   ```

![SCHEMA_DB](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/728c66af-f355-4368-84aa-d74e6ed075ab)
