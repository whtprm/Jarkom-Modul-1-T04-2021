# lapres Jarkom-Modul-1-T04-2021

**Oleh:**
  * Muhammad Nur Fauzan (NRP)
  * Ghimnastiar Al Abiyyuna (05311940000042)
  * Christopher Bennedict (05311840000024)

---

## **Display Filter**

**1.** Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 

**Solusi**\
Gunakan filter :

```
http.host contains "ichimarumaru.tech"
```
Maka didapat diketahui ichimarumaru.tech menggunakan ngingx/1.18.0
\
![Soal 1-1](https://user-images.githubusercontent.com/73151866/134772737-fef26aee-eb4e-4d44-b805-979191c98b51.png)

\
\
\
**2.** Temukan paket dari web-web yang menggunakan basic authentication method!

**Solusi**
```
http.authbasic
```
Maka dapat terlihat paket yang menggunakan Basic Authentication
\
![Soal 2-1](https://user-images.githubusercontent.com/73151866/134772799-37694739-a1f2-4700-8ee8-cae2db319811.png)



\
\
\
**3.** Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!


```
http.authbasic
```

Maka didapat dicari pada Auhtorization>Credential username dan password basic.ichimarumaru.tech
\
![Soal 3-1](https://user-images.githubusercontent.com/73151866/134772819-e6b13adc-8ec1-4bbc-92b1-4ba9afaccfee.png)
\
Kemudian Menjawab soal sesuai perintah yang ada
\
![Soal 3-2](https://user-images.githubusercontent.com/73151866/134772917-b46dc9d5-f718-4ea6-be1a-d192309d3cf5.png)


\
\
\
**4.** Temukan paket mysql yang mengandung perintah query select!

**Solusi**
```
mysql.query contains "select"
```

Maka didaptkan
\
![Soal 4-1](https://user-images.githubusercontent.com/73151866/134772998-7714d612-0f1c-44fd-9cab-8debc56e5d0e.png)


\
\
\
**5.** Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

**Solusi**
```
mysql.query contains "username"
```
Pertama kita gunakan filter untuk mendapatkan username dan password
\
![Soal 5-1](https://user-images.githubusercontent.com/73151866/134773036-145eecce-3edb-4112-9d53-5061176e22ee.png)
\
Kemudian Menjawab soal sesuai perintah yang ada
\
![Soal 5-2](https://user-images.githubusercontent.com/73151866/134773363-f6fff2bc-3e8e-4ea4-b0e5-0cdcb738363e.png)

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
src port 80
```
![Soal 11-1](https://cdn.discordapp.com/attachments/811534608800677891/891310664734343288/11.png)
\
\
\
**12.** Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Solusi**\
Gunakan filter:

```
port 21
```

![Soal 12-1](https://cdn.discordapp.com/attachments/811534608800677891/891310663136329818/12.png)
\
\
\
**13.** Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

**Solusi**\
Gunakan filter:

```
dst port 443
```

![Soal 13-1](https://cdn.discordapp.com/attachments/811534608800677891/891310667506810960/13.png)
\
\
\
**14.** Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!


**Solusi**\
Gunakan filter:

```
dst host kemenag.go.id
```


![Soal 14-1](https://cdn.discordapp.com/attachments/811534608800677891/891310660401635378/14.png)
\
\
\
**15.** Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Untuk `[private_ip]` dapat dilihat menggunakan command `ipconfig` pada terminal

**Solusi**\
Gunakan filter:


```
src host [private_ip]
```

![Soal 15-1](https://cdn.discordapp.com/attachments/811534608800677891/891310631033135124/15.png)
