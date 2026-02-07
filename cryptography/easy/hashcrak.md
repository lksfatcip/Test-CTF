# **Write Up**
## 1.	 Identitas Challenge:
-	Nama Challenge: Hashcrack
-	Level: Easy
-	Kategori: Cryptography
2.	 Deskripsi Challenge:
Pada challenge ini peserta diminta untuk mendapatkan flagnya dengan cara mengkonversi kode hash yang akan di berikan netcat(nc) sebanyak 3 kali.
3.	 Tahap Penyelesaian:
-	Launch instance terlebih dahulu untuk mendapatkan nc
-	Jalankan nc menggunakan terminal/whebsell
-	Tampilan setelah di jalankan kurang lebih seperti ini:
	-$ nc verbal-sleep.picoctf.net 56923  (port berbeda setiap launch)
	Welcome!! Looking For the Secret?

	We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
	Enter the password for identified hash:
-	Ubah kode hash menggunakan tool online (MD5,SHA,Hex,dll yg sesuai),lalu masukan ke nc yang sedang berjalan dan enter.
-	Selanjutnya , akan diberikan kode hash lain 2 kali dan tiap hash berbeda
-	Ubah satu persatu kode hash yang akan di berikan, lalu masukan ke nc yang sedang berjalan.
4.	Hasil Flag:
picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}
