
### Uygulama Güncelleme

Terminal ekranını açıyoruz (Ctrl + Alt + T) ve `sudo su` komutu ile root oluyoruz.

`cd/etc/apt` komutu ile dizine geçiş yapıyoruz

`ls` komutu ile dizisini listeliyoruz

`mouepad source.list` komutu ile dosyayı açıyoruz.

İlgili dosyada bulunan 2. ve 5. satırdaki # işaretini kaldırıp kaydediyoruz. (Ctrl+S)

Daha sonra yine terminal ekranında

`apt update` komutu ile güncelleme yapıyoruz.

Eğer hata alırsanız
	`sudo apt update` şeklinde kullanabilirsiniz.
		
### Sistem Güncelleme
	`sudo apt upgrade`

### Sistem Tam Güncelleme Komutu
Terminalda root oluyoruz

	`sudo su`
	
daha sonra

	`apt-get update && apt-get -y full-upgrade`
