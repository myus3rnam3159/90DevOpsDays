*** Cài đặt *** 

1. Go

	* sudo rm -rf /usr/local/go
	
	* sudo tar -C /usr/local -xzf go1.20.1.linux-amd64.tar.gz
	
	* cd về directory của user: cd ~
	
	* nano .profile
	
	* thêm dòng export PATH="$PATH:/usr/local/go/bin", sau đó save
	
	* source .profile

	* reboot lại máy
