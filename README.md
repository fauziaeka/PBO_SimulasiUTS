# 🗓️ Pertemuan Ketujuh - SIMULASI UTS NO 6 
## 📚 Topik Utama 
Langkah-langkah membuat CRUD dengan Java Swing untuk entitas Buku dengan atribut: ISBN, Judul Buku, Tahun Terbit, Penerbit 

## 📑 Daftar Isi 
Tidak dapat memuat bentuk
- [Java Swing Buku](https://github.com/fauziaeka/PBO_SimulasiUTS/blob/main/FrameBuku.java)
- [Buku DB](https://github.com/fauziaeka/PBO_SimulasiUTS/blob/main/BukuDB.java) 
- kesimpulan 

## Langkah- Langkah 
1. Buat project baru dengan nama "PBO_SimulasiUTS
   
   ![GetImage](https://github.com/user-attachments/assets/3da403a7-e2f0-430f-94b6-618e84a89f8b)]
2. Membuat class JFrame Form pada project "PBO_SimulasiUTS"
   
   ![GetImage (1)](https://github.com/user-attachments/assets/a13e64da-1021-4858-9406-fbc7680f46de)
   ![GetImage (2)](https://github.com/user-attachments/assets/b5d8b926-63c1-45cb-b345-3ad6b77562f6)

3. Membuat Desain pada JFrame Form. Gunakan JLable pada judul tampilan “DATA BUKU”, ISBN, Judul Buku, Tahun Terbit, Penerbit. Gunakan JTextField untuk mengisi atau menginput data ISBN, Judul Buku, Tahun Terbit, dan Penerbit. Gunakan JButton pada tombol Insert, Update, Delete, Clear, dan Exit. Gunakan JTable untuk menampilkan Table Data Buku yang berisi 4 kolom yakni ISBN, Judul Buku, Tahun Terbit, dan Penerbit.

   ![GetImage (3)](https://github.com/user-attachments/assets/f7f3b506-7182-4985-b152-b6b9f1bfc8e6)

4. Mengisi class BukuDB. Class ini berfungsi untuk mengonversi ResultSet pada database menjadi TableModel agar dapat ditampilkan pada JTable di GUI Java Swing sehingga saat pengisian data kita tidak perlu menulis kodenya secara manual.



5. Membuat Table pada postgreSQL 

   ![GetImage (4)](https://github.com/user-attachments/assets/9b5dc71c-8a04-4a8f-a5c0-01a16d6025da)
 
6. Menyambungkan Netbeans dengan Database 

- Ketuk ‘Services’ , pilih ‘Databases’ kemudian pilih ‘New Connection’ 

![GetImage (5)](https://github.com/user-attachments/assets/18121277-e900-45b3-bf50-b370c3213327)

- Pilih PostgreSQL

![GetImage (6)](https://github.com/user-attachments/assets/ff4859ae-bdf8-4a00-b517-d2aac9f9587b)

- Isi kolom Database sesuai dengan nama Database pada PostgreeSQL, kemudian isi password sesuai dengan password PostgreeSQL

![GetImage (7)](https://github.com/user-attachments/assets/62169171-4586-4208-b219-7f1967387ed7)

- Select schema menjadi ‘public’

![GetImage (8)](https://github.com/user-attachments/assets/bec9db0d-e7e0-4f2f-bd83-cbd9fdd1f41c)

- Pada kolom input connection ini akan otomatis terisi, klik Finish

![GetImage (9)](https://github.com/user-attachments/assets/07a9f25a-fb5e-4671-a590-63d8890c8a36)

- Klik ‘Drive’ pilih ‘New Driver’

![GetImage (10)](https://github.com/user-attachments/assets/50bc3e6f-1607-4365-aa16-c9e7634fc655)

- Kembali pada bagian ‘Project’, klik ‘Library’ setelah itu klik ‘Add Library’

![GetImage (11)](https://github.com/user-attachments/assets/4ba0d532-d609-4736-ba30-b5206a73cd2b)

- Pilih ‘PostgreeSQL JDBC Driver’ kemudian klik ‘Add Library’

![GetImage (12)](https://github.com/user-attachments/assets/6c4fa933-19e2-49ec-b181-444c8ea539bd)

7. Pada JFrame Form klik source, maka akan muncul source code dari desain secara otomatis. Isikan bagian tombol-tombol yang di desain agar bisa bekerja 

a. Mendeklarasikan import kelas-kelas yang diperlukan untuk database, pengolahan input, antarmuka pengguna dengan swing serta menyimpan detail koneksi database. 

b. Membuat method tampil untuk membuat koneksi ke database dengan menggunakan perintah DriverManager.getConnection dan menampilkan informasi tersebut dalam sebuah JTable dengan menggunakan perintah "SELECT * FROM Buku;" 

c. Mengisi code pada btnInsert yang berfungsi untuk menambahkan data. Button ini berfungsi untuk menambahkan data pada 'Data Buku'. Sebagai pengguna, kita diminta untuk mengisi informasi mengenai ISBN, judul buku, tahun terbit buku serta penerbit buku. Setelah dimasukkan, kita bisa menekan button Insert. Jika berhasil, akan muncul pesan 'Data Berhasil disimpan'. 

d. Mengisi code pada btnUpdate yang berfungsi untuk memperbarui data. Pertama-tama masukkan ISBN yang ingin diubah, kemudian masukkan informasi mengenai judul buku, tahun terbit buku serta penerbit buku baru. Jika berhasil, sistem akan mencetak pemberitahuan bahwa 'Data berhasil diupdate'. 

e. Mengisi code pada btnDelete yang berfungsi untuk menghapus data pada 'Data Buku'. Pengguna bisa memasukkan data yang ingin dihapus atau bisa juga dengan mengeklik data yang ingin dihapus pada kolom list. Kemudian akan muncul pesan konfirmasi apakah pengguna ingin menghapus data atau tidak. Jika 'iya' data otomatis akan dihapus dan jika 'tidak' maka data akan batal dihapus. 

f. Mengisi code pada btnExit yang berfungsi untuk keluar dari halaman yang menampilkan GUI dengan kembali ke halaman awal. 

g. Mengisi code pada program tblBukuMouseClicked yang berfungsi untuk menampilkan data dalam bentuk tabel selain itu, pengguna juga dapat mengedit data tersebut. 

h. Mengisi code pada program bersih() yang berfungsi untuk memastikan bahwa setelah data dimasukkan atau operasi selesai, semua input dari pengguna direset untuk memudahkan pengguna memasukkan data baru tanpa harus menghapusnya secara manual. 

8. Hasil eksekusi Insert data

![GetImage (13)](https://github.com/user-attachments/assets/aba143ce-d14c-49d6-b1b2-7d15547482c4)

9. Hasil eksekusi Update data

![GetImage (14)](https://github.com/user-attachments/assets/4b6a7afe-b076-4f37-b318-61fff5dfb571)

10. Hasil eksekusi Delete data

![GetImage (15)](https://github.com/user-attachments/assets/568b1f4e-8786-4d8f-8116-6ba588ecc760)

11. Hasil eksekusi Exit

![GetImage (16)](https://github.com/user-attachments/assets/ef65f596-fa1e-41a9-adf9-fc8f889f71ec)

![GetImage (17)](https://github.com/user-attachments/assets/4665aff5-1a83-4a3d-a58c-c098fa6fa78b)


 

 
 

  
