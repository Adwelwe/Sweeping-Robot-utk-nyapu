# Sweeping-Robot-utk-nyapu
robotnya nanti bisa menyapu di tempat manapun, asalkan ada sample yang bisa diproses sama robotnya. dan sample nya harus jelas memperlihatkan lingkungan dari tempat yang akan disapu sama robotnya.

jadi,
  ini kita buat dlu library nya apa aja guna manipulasi symtaxnya utk memudahkan kita dalam ngoding;
  #include <iostream>
  #include <vector>
  #include <fstream>
  #include <cmath>
  #include <string> ohya jangan lupa pake "using namespace std;" sekalian:)

next,
1. tentukan mekanisme robot nya, bagaimana dia bisa menyapu dan pengontrolan sistem sebelum dia menyapu

2. buat class berdasarkan mekanisme robot yang telah kita analisa (ada 5 analisis yaitu vektor utk kontrol arahnya, sendi pd robot, sistem pd robot itu sendiri, deteksi alat sapu, dan deteksi lingkungan yg akan disapu)

3. lanjut, di vektor ini kita buat grid nya berdasarkan prediksi bagaimana dia mengatur jarak dan arah yg berkaitan nanti dengan kegiatan menyapunya.

4. pd class sendi, kita buat bagaimana ketika dia menyapu nanti perubahan panjang dari ruas lengan nya dan perputaran sendi pada radian yang akan terproses sesuai kalkulasinya.

5. pd class sweeper, kita buat bagaimana dia nanti bisa deteksi alat sapu nya. nah ketika berhasil, nanti dia bakal menjalankan perintah utk menyapu (pokoknya disesuaikan dengan semua program yg lainnya)

6. pd class robot, kita buat inv. kinematik, pergerakan, dan file handling (pd void load_config) utk memproses mekanisme nya.
   - inv. kinematik, menggunakan inv. kinematik sederhana dan menghitung sudut sendi robot agar mencapai titik            tujuan tertentu.
   - pergerakan, mempertimbangkan kesesuaian presisi dari semua pergerakan pd robot yg terlibat, dan memproses utk        aksi menyapu.
   - (pd void load_config) file handling, dia akan menyimpan, mengelola dan mentransfer semua sitem mekanismenya          utk diproses nanti di akhir kode "return..."

7. pd class environment, kita buat grid utk peta pd lingkungannya. lalu input "void load_map" utk mengidentifikasi pada petanya (akan dijalankan sesuai dengan operasi yg telah kita input). dan jangan lupa pakai "void tampilkan" utk
menampilkan lingkungannya.

8. terakhir, kita proses 5 analisa tsb dengan "int main()" dan input operasi serta statement yang akan menjalankan robot tersebut utk menyapu.
  
