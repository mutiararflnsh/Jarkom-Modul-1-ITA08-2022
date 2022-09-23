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
