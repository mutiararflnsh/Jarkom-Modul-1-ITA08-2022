# Jarkom-Modul-1-ITA08-2022

Pengerjaan soal shift jarkom modul 1 oleh ITA08

# Anggota

| Nama                           | NRP          | 
| -------------------------------| -------------| 
| Axellino Anggoro A.              | `5027201040` | 
| Mutiara Nuraisyah Dinda R            | `5027201054` | 
| Brilianti Puspita S.  | `5027201070` |

## Soal 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 
<b> Penyelesaian : </b> <br>
<b>Jawaban : nginx/1.10.3 <br> </b>
```Display Filter : http.host == monta.if.its.ac.id``` <br> 

Kita bisa mencari web server dengan filter http.host dan juga dengan menyertakan alamat webnya. Kemudian kita hanya perlu mencari web servernya dengan melakukan Follow tcp stream pada salah satu paket dan bisa dilihat hasilnya pada screenshot dibawah ini

![1a](/Screenshot/1a.png)
![1b](/Screenshot/1b.png)

Bisa dilihat bagian atas terdapat informasi servernya yakni nginx/1.10.3

## Soal 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?
<b> Penyelesaian : </b> <br>

```Display Filter :  http.request.uri contains "detail" ```

![2a](/Screenshot/2a.png)
![2c](/Screenshot/2c.png)
Setelah di Follow TCP Stream, terdapat informasi yakni detail topik yang dilihat bisa dibuka dengan memasukkan index.php/topik/detailtopik/194 yang berisikan seperti screenshot dibawah ini
![2b](/Screenshot/2b.png)
<b> Diatas terlihat bahwa detail topik yang dilihat ishaq adalah "Evaluasi unjuk kerja User Space Filesystem (FUSE)"</b>

## Soal 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! <br>
<b> Penyelesaian : </b> <br>
```Display Filter :  tcp.dstport == 80```

![3](/Screenshot/3.png)

## Soal 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21! <br>
<b> Penyelesaian : </b> <br>
``` Display Filter :  tcp.srcport == 21 ```

![4](/Screenshot/4.png)

## Soal 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443! <br>
<b> Penyelesaian : </b> <br>

``` Display Filter :  tcp.srcport == 443 ```

![5](/Screenshot/5.png)

## Soal 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id <br>
<b> Penyelesaian : </b> <br>
``` Display Filter :  http.host == lipi.go.id ```

![6a](/Screenshot/6a.png)
![6b](/Screenshot/6b.png)
Saat di Follow TCP Stream maka akan terlihat benar host yang dituju adalah "lipi.go.id"

## Soal 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian! <br>
<b> Penyelesaian : </b> <br>

``` Display Filter :  ip.src == ip ``` <br> Untuk IP masukkan IP sesuai dengan IP kalian, caranya bisa dengan membuka command prompt dan ketik ipconfig

![7a](/Screenshot/7a.png)
![7b](/Screenshot/7b.png)

## Soal 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.
<br> <b> Penyelesaian : </b> <br>
Untuk soal ini ditemukan 3 buah percakapan yang masing masing berada pada <br> 

``` Display Filter :  tcp.stream eq 12``` <br>
![8a](/Screenshot/8a.png)

``` Display Filter : tcp.stream eq 41 ``` <br>
![8b](/Screenshot/8b.png)

``` Display Filter :  tcp.stream eq 90 ```
![8c](/Screenshot/8c.png)

## Soal 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.
<br> <b> Penyelesaian : </b>
<br>
Setelah ditelusuri berdasarkan percakapan yang ditemukan telah dikirim sebuah file melalui "9002" dan ditemukan sebuah salted file dalam packet tersebut yang perlu untuk disimpan bentuk raw nya dengan format [nama_kelompok].des3 dan di decrypt menggunakan bantuan command openssl pada linux. 
Berikut adalah command openssl nya : 

```openssl des3 -d -salt -in ITA08.des3 -out flag.txt ```

![9a](/Screenshot/9a.png)
![9b](/Screenshot/9b.png)
![9c](/Screenshot/9c.png)

## Soal 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas! <br>
<b> Penyelesaian : </b> <br>
Dari hasil decrypt diatas ditemukan sebuah flag seperti screenshot dibawah ini pada flag.txt
![9d](/Screenshot/9d.jpg)







