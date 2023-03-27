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

9.	Saat file berbahaya sedang transit R1, IDS, Snort, dapat memeriksa muatannya. Payload cocok dengan setidaknya satu tanda tangan yang dikonfigurasi di Snort dan memicu peringatan di jendela terminal R1 kedua (tab tempat tail -f berjalan). Entri peringatan ditunjukkan di bawah ini. Stempel waktu Anda akan berbeda:

![Picture9](https://user-images.githubusercontent.com/99699435/227877477-5fc83339-7cc1-4c9b-941f-3679b0216932.png)

## Soal 3: 
a.	Berdasarkan peringatan yang ditunjukkan di atas, apa alamat IPv4 sumber dan tujuan yang digunakan dalam transaksi?

b.	Berdasarkan alert di atas, port sumber dan tujuan apa yang digunakan dalam transaksi?

c.	Berdasarkan peringatan yang ditunjukkan di atas, kapan pengunduhan dilakukan?

d.	Berdasarkan peringatan yang ditunjukkan di atas, apa pesan yang direkam IDS signature? 

## Penyelesaian:
a.	Alamat IP sumber adalah: 209.165.200.235 dan alamat IP tujuan adalah: 209.165.202.133

b.	Port sumber adalah: 52804 dan port tujuan adalah 666 

c.	Pengunduhan dilakukan pada tanggal 21 Maret 2023, pukul 11:29

d.	Pesan yang direkam IDS signature adalah Malicious Server Hit!

10.	Pada H5, gunakan perintah tcpdump untuk merekam peristiwa dan mengunduh file malware lagi sehingga Anda dapat merekam transaksi. Keluarkan perintah berikut di bawah ini mulai pengambilan paket:

![Picture10](https://user-images.githubusercontent.com/99699435/227878918-3acebd2f-6a33-4e68-9862-f9210ec9d800.png)

11.	Sekarang tcpdump menangkap paket, unduh malware lagi. Pada H5, jalankan kembali perintah atau gunakan panah atas untuk memanggilnya kembali dari fasilitas riwayat perintah.

![Picture11](https://user-images.githubusercontent.com/99699435/227878934-05dd8403-8722-4ae8-a308-df2786284344.png)

12.	Hentikan pengambilan dengan membawa tcpdump ke latar depan dengan perintah fg. Karena tcpdump adalah satu-satunya proses yang dikirim ke latar belakang, PID tidak perlu ditentukan.

![Picture12](https://user-images.githubusercontent.com/99699435/227878945-9f1f4ebf-b0ad-48ac-9439-9d68478f5c6a.png)

13.	Pada H5, Gunakan perintah ls untuk memverifikasi file pcap sebenarnya disimpan ke disk dan memiliki ukuran lebih besar dari nol.

![Picture13](https://user-images.githubusercontent.com/99699435/227878961-f52519e7-5796-4e8d-8c81-81e19aec5f79.png) 

## Soal 4: 
Bagaimana file PCAP ini berguna bagi analis keamanan?

## Penyelesaian:
File PCAP berisi paket-paket yang terkait dengan lalu lintas yang dilihat oleh NIC yang menangkap. Dengan begitu, PCAP sangat berguna untuk menelusuri kembali peristiwa jaringan seperti komunikasi ke titik akhir yang berbahaya. Alat seperti Wireshark dapat digunakan untuk memfasilitasi analisis PCAP.
