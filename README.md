Nama: Reva Aura Ramadhani
NIM: H1H024059

Deskripsi

Praktikum ini bertujuan untuk memahami penggunaan protokol komunikasi pada Arduino Uno, yaitu UART dan I2C. Protokol komunikasi digunakan untuk mengirim dan menerima data antara Arduino dengan komputer maupun perangkat lain seperti LCD.

Percobaan
1. Komunikasi Serial (UART)

Mengendalikan LED menggunakan input dari Serial Monitor.

2. Inter-Integrated Circuit (I2C)

Menampilkan nilai analog dari potensiometer pada LCD.

Penjelasan Program
UART
Serial.begin() → memulai komunikasi
Serial.available() → cek data masuk
Serial.read() → membaca input
digitalWrite() → kontrol LED
I2C
Wire.h → komunikasi I2C
LiquidCrystal_I2C.h → kontrol LCD
analogRead() → membaca potensiometer
map() → konversi ke bar
Hasil dan Analisis
Percobaan 3A (UART)

Berdasarkan hasil percobaan, komunikasi serial UART berjalan dengan baik. Arduino mampu menerima input dari keyboard melalui Serial Monitor, kemudian memproses data tersebut untuk mengontrol kondisi LED. Ketika diberikan input ‘1’, LED menyala, dan ketika diberikan input ‘0’, LED mati.

Penggunaan fungsi Serial.available() memastikan bahwa data tersedia sebelum dibaca, sehingga komunikasi menjadi stabil dan terhindar dari kesalahan. Hal ini menunjukkan bahwa UART efektif digunakan untuk komunikasi sederhana antara komputer dan mikrokontroler.

Percobaan 3B (I2C)

Berdasarkan hasil percobaan, nilai analog dari potensiometer berhasil dibaca oleh Arduino dan ditampilkan pada LCD menggunakan komunikasi I2C. Nilai tersebut ditampilkan dalam bentuk angka dan grafik batang (bar) yang berubah sesuai dengan posisi potensiometer.

Semakin besar nilai potensiometer, maka semakin panjang tampilan bar pada LCD. Hal ini menunjukkan bahwa komunikasi I2C berjalan dengan baik dan mampu mentransfer data secara real-time.

Analisis Umum

Berdasarkan kedua percobaan, dapat disimpulkan bahwa UART digunakan untuk komunikasi dengan komputer secara sederhana, sedangkan I2C digunakan untuk komunikasi antar perangkat dengan lebih efisien.

Kombinasi kedua protokol ini memungkinkan sistem Arduino menjadi lebih fleksibel, di mana input dapat diterima dari komputer dan output dapat ditampilkan ke LCD secara bersamaan.

Jawaban Pertanyaan Praktikum
Percobaan 3A (UART)

1. Proses input hingga LED menyala/mati
Input dari keyboard dikirim ke Arduino melalui Serial Monitor, kemudian dibaca dan diproses untuk mengontrol LED.

2. Fungsi Serial.available()
Untuk memastikan data tersedia sebelum dibaca agar tidak terjadi error.

3. LED berkedip saat input ‘2’
LED akan berkedip terus sampai ada perintah lain.

4. Delay vs Millis
delay() menghentikan program, sedangkan millis() tidak (lebih efisien).

Percobaan 3B (I2C)

1. Cara kerja I2C
Arduino sebagai master mengirim data ke LCD melalui SDA dan SCL.

2. Pin potensiometer tertukar
Nilai tetap terbaca tetapi arah perubahan terbalik.

3. Gabungan UART dan I2C
Data ditampilkan di LCD dan Serial Monitor.

4. Tabel ADC

ADC	Volt (V)	Persen (%)
1	0.00	0%
21	0.10	2%
49	0.24	5%
74	0.36	7%
96	0.47	9%

pertanyaan 3.7

1. UART vs I2C
UART sederhana, I2C lebih efisien dan bisa banyak device.

2. Alamat I2C
Untuk identifikasi perangkat agar tidak konflik.

3. Alur kerja sistem
Input → Arduino → proses → output ke LCD dan Serial Monitor.
