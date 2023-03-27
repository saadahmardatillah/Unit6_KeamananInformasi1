# Unit6_KeamananInformasi1 
## Snort dan Firewall Rules 

1. Konfigurasi jaringan dengan menjalankan skrip configure_as_dhcp.sh.

![Picture1](https://user-images.githubusercontent.com/99699435/227873410-77375fbe-5da1-4436-91bb-878fddedaf82.png)

2. Melakukan ping ke www.cisco.com.

![Picture2](https://user-images.githubusercontent.com/99699435/227873838-077c2bcd-1319-4d36-b371-016ef2b319de.png)

3.	Menjalankan skrip miniset. 

![Picture3](https://user-images.githubusercontent.com/99699435/227874038-8020fa4c-6d36-4905-9c0a-f05e737b9519.png)

4.	Menjalankan perintah dari prompt miniset untuk buka shell R1.

![Picture4](https://user-images.githubusercontent.com/99699435/227874430-9268f8dc-b415-4b07-b439-744be06e1c1b.png) 

## Soal 1: 
Shell R1 terbuka di jendela terminal dengan teks hitam dan latar belakang putih. 
Pengguna apa yang masuk ke shell itu? Ini indikatornya apa??

## Penyelesaian:
Pengguna yang masuk ke shell adalah pengguna root. Ditunjukan oleh tanda # setelah prompt. 

5.	 Membuka shell host H5 dan H10. 

![Picture5](https://user-images.githubusercontent.com/99699435/227876129-53117f83-948f-4d55-9431-9e9e50bac973.png)

6.	H10 melakukan simulasi server di internet yang melakukan hosting malware.

![Picture6](https://user-images.githubusercontent.com/99699435/227876161-49cd428b-1461-42e3-9ef9-dc4dc693dbbc.png)

7.	Pada tab terminal R1 yang baru, menjalankan perintah tail dengan opsi -f untuk memantau file /var/log/snort secara real-time.

![Picture7](https://user-images.githubusercontent.com/99699435/227876182-709a0ae7-c552-4297-91d4-e7df3b87b594.png)

8.	Pada terminal H5, menggunakan perintah wget untuk mengunduh file Bernama W32.Nimda.Amm.exe.

![Picture8](https://user-images.githubusercontent.com/99699435/227876220-5a59b4e0-a0aa-4043-aa86-e245a49dc0b4.png)

## Soal 2: 
a.	Port apa yang digunakan saat berkomunikasi dengan server web malware? Apa indikatornya?
b.	Apakah file telah diunduh sepenuhnya?
c.	Apakah IDS menghasilkan peringatan yang terkait dengan unduhan file?

## Penyelesaian:
a.	Port 666. Port ini ditentukan dalam URL, setelah tanda pemisah (:)
b.	File sepenuhnya telah diunduh
c.	IDS telah mengasilkan peringatan yang memiliki kaitan dengan unduhan file
