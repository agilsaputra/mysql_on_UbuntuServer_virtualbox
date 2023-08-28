### ▶️ Setting Mysql UbuntuServer di Virtualbox dan koneksi dengan local menggunakan SSH 👨‍💻

 - OS yang saya gunakan yaitu linux mint cinammon
 - Install virtualbox di linux lalu download UbuntuServer di sini [UbuntuServer](https://ubuntu.com/download/server)
 - Setelah itu create new virtual machine lalu pilih file iso yang di download tadi
   ![Screenshot from 2023-08-28 15-23-38](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/e52af51f-46f9-400b-a261-6aa4c9638c4f)
 - next lalu tentukan spec server yang kalian inginkan
 - karena hanya untuk practice mysql saya menggunakan 3.5 gb ram, 2 cpu dan 10 gb disk
 - lakukan instalasi sampe selesai.
 - setelah itu kalian start ubuntuserver kalian
   ![Screenshot from 2023-08-28 15-29-25](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/deac1b0b-668a-4eb4-baf7-f1b2f123c1c7)
 - dan lakukan installasi ubuntuserver
 - pilih try ubuntu server
 - pilih bahasa english
 - pilih ubuntu server
 - network default dan tidak pakai proxy
 - tunggu configurasi sampe selesai
 - isikan username dan password user server
 - lalu pada menu shh centang koneksi pakai ssh
 - lalu kalian akan mendapatkan tampilan terminal seperti ini
   ![Screenshot from 2023-08-28 15-43-14](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/79b03a5d-6622-46f0-84e5-504262284383)
 - login dengan username dan password yang kalian bikin
 - cek ssh kalian dengan perintah
   ```
   systemctl status ssh
   ```
 - lalu jika belum aktif lalukan instal ssh
   ```
   sudo apt install openssh-server
   sudo systemctl start ssh
   ```
 - dan cek juga di terminal pc kalian lakukan seperti diatas
 - setting port di virtualbox, klik menu setting lalu network, advanced, port forwading, setelah itu set port seperti dibawah ini
   ![Screenshot from 2023-08-28 15-51-08](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/470c86b1-4142-45c9-ab58-fe61c3a9c007)

 - lalu coba koneksikan dengan terminal local kalian
   ```
   ssh username@localhost -p 2222
   ```
 - lalu masukan password kalian
 - jika berhasil maka nama terminal depan kalian berubah menjadi ```username@namaserver```
   ![Screenshot from 2023-08-28 15-55-14](https://github.com/agilsaputra/mysql_on_UbuntuServer_virtualbox/assets/22126819/f087dc61-a955-4c41-beb3-88b17917f96f)

   
   

   

