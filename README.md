# Siege
Siege merupakan salah satu alternatif yang dapat digunakan untuk menguji load test suatu url(site).
Siege dirancang untuk menguci performansi kode dengan kondisi ekstrim, siege mendukung penggunaan
autentikasi, cookies, http, https,dan penggunaan ftp. Siege menyediakan fasilitas untuk mensimulasikan
jumlah user/client yang akan mengakses suatu http request.

## Langkah Instalasi pada ubuntu

1.Install build-essential
` sudo apt-get update && sudo apt-get install build-essential`

2.cd ~/Downloads
` wget http://download.joedog.org/siege/siege-3.1.0.tar.gz`

![image](https://cloud.githubusercontent.com/assets/19463315/23456214/102ee220-fea5-11e6-9536-df17e953a97d.png)

3.Ekstrak zip file
`lamhot@lamhot-X456URK:~/Downloads$ tar -xvf siege-3.1.0.tar.gz`

![image](https://cloud.githubusercontent.com/assets/19463315/23456310/8d4ea1a0-fea5-11e6-9dc4-9d4530bb2c49.png)

4.Masuk pada folder siege-3.1.0
`cd siege-3.1.0`

5.Lakukan Konfigurasi
`./configure`

![image](https://cloud.githubusercontent.com/assets/19463315/23456406/dc98fe68-fea5-11e6-995d-c94f38efa770.png)

`make` 

![image](https://cloud.githubusercontent.com/assets/19463315/23456428/fd74b636-fea5-11e6-8de6-292586b519a6.png)

` sudo make install`

![image](https://cloud.githubusercontent.com/assets/19463315/23456461/26019d80-fea6-11e6-9ba7-48549738fe80.png)

6.Versi

Untuk memastikan instalasi siege berjalan dengan baik, lakukan pengecekan dengan menggunakan perintah berikut:

`siege -V`

![image](https://cloud.githubusercontent.com/assets/19463315/23456570/8a585512-fea6-11e6-839e-10508c7e69da.png)
## Load testing dengan Siege
### Basic
`siege http://api.staging28.vm/v2/products.json?keywords=mi5 `
![image](https://cloud.githubusercontent.com/assets/19463315/23457031/8f652e34-fea8-11e6-925d-1b7f4041285b.png)

### Simulasi jumlah User/Client  dan delay
`siege http://api.staging28.vm/v2/products.json?keywords=mi5 -c 200 -d 3`

### Report
Untuk menghasilkan report pada console, gunakan keyboard:` ctrl+c`
![image](https://cloud.githubusercontent.com/assets/19463315/23457103/04d70430-fea9-11e6-826e-19912f821bb2.png)

## Uninstall Siege
`cd ~/Downloads/siege-3.1.0/`

`make uninstall`

## Reference
https://drupalize.me/blog/201507/load-testing-your-site-siege
