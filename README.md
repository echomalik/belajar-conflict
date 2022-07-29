# Belajar Conflict dalam git

## Persiapan

Silahkan clone repo ini ke dalam `localhost` kalian dengan cara

```bash
git clone https://github.com/inimalik/belajar-conflict.git
```

## Tahapan

1. Buka folder project `belajar-conflict` di Sublime Text atau Text Editor lain

2. Pada aplikasi `GIT BASH`, JANGAN LUPA UNTUK PINDAH BRANCH DENGAN FORMAT SEPERTI PADA CONTOH
	
	```bash
	git checkout -b nama_conflict
	```

3. Dalam file `index.php` sudah disediakan beberapa variable

	```php
	$nama = "Reza Malik";
	$umur = "29";
	$alamat = "Tangerang";
	```

4. Ubah nilai dari setiap variable yang tersedia dengan data kalian sendiri, kemudian tambahkan **5** variable baru di baris setelahnya untuk menyimpan data pribadi lain, contoh:

	```php
	$nama = "Reza Malik";
	$umur = "29";
	$alamat = "Tangerang";
	$hobi = "Berenang";
	$pekerjaan = "Programmer";
	$dan_lain_lain = "data pribadi";
	...
	...
	...
	```	

5. Lakukan langkah yang sama dari `add` sampai ke `push`

	```bash
	git status

	git add .

	git commit -m "Ahmad menambahkan line baru"

	git push -u origin Ahmad_conflict
	```

	> Note:
	> 
	> Pastikan kalian sudah terdaftar sebagai contributor pada repo https://github.com/inimalik/belajar-conflict. Hubungi saya jika belum menjadi contributor!
	> 
	> Dilarang keras untuk push langsung ke `develop`!!!!!
	> 
	> ~~git push -u origin develop~~
	


6. Masuk ke akun git kalian masing masing dan buka repository `belajar-conflict`, masuk ke menu `pull request`, isi form pesan sederhana saja. Ini dimaksudkan untuk memberitahu `Tech Lead` (Pimpinan Project atau Pemilik Repo) untuk menyatukan script yang sudah dibuat dalam kolaborasi yang ada.

## Penjelasan

Conflict akan terjadi jika:

1. Pada saat contributor melakukan push ke branch masing-masing dan memberitahu pemilik repo melalui menu `pull request`
2. Pemilik repo menerima request tersebut dan melakukan `merge` atau menyatukan scriptnya.
3. Disaat yang bersamaan ada beberapa contributor yang melakukan `push`. Pada tahap inilah terjadi `conflict`, karena:
	
	+ Setiap contributor mengedit file yang sama dan baris yang sama.
	+ Setiap contributor memiliki script awal yang sama, namun karena ada yang sudah melakukan push terlebih dahulu dan dimerge oleh pemilik repo, maka contributor berikutnya mengalami conflict, artinya script awal si contributor kedua berbeda dengan yang dahulu pernah dia dapat pada saat clone.
	

Sehingga conflict tidak akan terjadi kepada semua contributor, tergantung kapan waktu dia clone, kapan dia push dan kapan pull request mereka dimerge

Silahkan dipraktekkan, sehingga bisa dipahami bagaimana bisa terjadi conflict pada saat berkolaborasi.