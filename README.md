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

<b>Jawaban : nginx/1.10.3 <br>
Display Filter : http.host == monta.if.its.ac.id <br> </b>

Kita bisa mencari web server dengan filter http.host dan juga dengan menyertakan alamat webnya. Kemudian kita hanya perlu mencari web servernya dengan melakukan Follow tcp stream pada salah satu paket dan bisa dilihat hasilnya pada screenshot dibawah ini

![1a](/Screenshot/1a.png)
![1b](/Screenshot/1b.png)

Bisa dilihat bagian atas terdapat informasi servernya yakni nginx/1.10.3

## Soal 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?
<br> Untuk menyelesaikan soal ini dapat menggunakan <br>
<b> Display Filter :  http.request.uri contains "detail" </b>

![2a](/Screenshot/2a.png)
![2c](/Screenshot/2c.png)
Setelah di Follow TCP Stream, terdapat informasi yakni detail topik yang dilihat bisa dibuka dengan memasukkan index.php/topik/detailtopik/194 yang berisikan seperti screenshot dibawah ini
![2b](/Screenshot/2b.png)
<b> Diatas terlihat bahwa detail topik yang dilihat ishaq adalah "Evaluasi unjuk kerja User Space Filesystem (FUSE)"</b>

