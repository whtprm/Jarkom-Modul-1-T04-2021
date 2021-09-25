# lapres Jarkom-Modul-1-T04-2021

**Oleh:**
  * Muhammad Nur Fauzan (NRP)
  * Ghimnastiar Al Abiyyuna (05311940000042)
  * Christopher Bennedict (NRP)

---

## **Display Filter**

**1.** Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 

**Solusi**\
Gunakan filter :

```
test
```



![Soal 1-1]

![Soal 1-2]


\
\
\
**2.** Temukan paket dari web-web yang menggunakan basic authentication method!

**Solusi**
```
filter e tarok sini
```

![Soal 2-1]


\
\
\
**3.** Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!


```
test
```


![Soal 3-1]


\
\
\
**4.** Temukan paket mysql yang mengandung perintah query select!

**Solusi**
```
filter e tarok sini
```
\
\
\
**5.** Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

**Solusi**
\
```
filter e tarok sini
```
\
\
\
**6.** Cari username dan password ketika melakukan login ke FTP Server!

**Solusi**
```
ftp countains "user" dan ftp countains "pw"
```

Maka akan di dapatkan User
\
![Soal 6-1](https://cdn.discordapp.com/attachments/830775203868573756/891297362713141279/unknown.png)
\
Dan akan di dapatkan Password
\
![Soal 6-2](https://cdn.discordapp.com/attachments/830775203868573756/891297447857496074/unknown.png)
\
\
\
**7.** Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")


**Solusi**

```
ftp-data contains "Real.pdf"
```

Maka didapatkan
\
![Soal 7-1](https://cdn.discordapp.com/attachments/830775203868573756/891298448836542484/unknown.png)
\
Follow TCP stream
\
![Soal 7-2](https://cdn.discordapp.com/attachments/830775203868573756/891298918510510090/unknown.png)
\
Dan Download sebagai .zip file
\
![Soal 7-3](https://cdn.discordapp.com/attachments/830775203868573756/891298874285785119/unknown.png)

\
\
\
**8.** Cari paket yang menunjukan pengambilan file dari FTP tersebut!


**Solusi**

```
ftp-data.command contains "RETR"
```
![Soal 8-1](https://cdn.discordapp.com/attachments/830775203868573756/891299038081712148/unknown.png)

\
\
\
**9.** Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

**Solusi**\
Gunakan filter:

```
ftp-data.command contains "STOR secret.zip"
```
Kemudian follow TCP Stream
![Soal 9-1](https://cdn.discordapp.com/attachments/830775203868573756/891299558322216960/unknown.png)
\
lalu didapatkan
\
![Soal 9-2](https://cdn.discordapp.com/attachments/830775203868573756/891299262430847006/unknown.png)

\
\
\
**10.** Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!

**Solusi**
```
ftp-data.command contains "STOR history.txt"
```

Follow TCP stream
![Soal 10-1](https://cdn.discordapp.com/attachments/830775203868573756/891299611485020190/unknown.png)
\
Kemudian download hystory sebagai file .txt
\
![Soal 10-2](https://cdn.discordapp.com/attachments/830775203868573756/891299642170540032/unknown.png)
---

## Capture Filter

**11.** Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! 

**Solusi**\
Gunakan filter:

```
tarok filter disini
```
![Soal 11-1](foto jawaban)
\
\
\
**12.** Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Solusi**\
Gunakan filter:

```
jghjghjgh
```

![Soal 12-1](foto jawaban)
\
\
\
**13.** Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

**Solusi**\
Gunakan filter:

```
sfsdfsd
```

![Soal 13-1](foto jawaban)
\
\
\
**14.** Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!


**Solusi**\
Gunakan filter:

```
dsfsdfsdfsd
```


![Soal 14-1](foto jawaban)
\
\
\
**15.** Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Untuk `[ip_sendiri]` dapat dilihat menggunakan command `ipconfig` pada terminal

**Solusi**\
Gunakan filter:


```
sdasdsada
```

![Soal 15-1](foto jawaban)
