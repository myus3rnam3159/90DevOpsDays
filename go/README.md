*** Cài đặt(cho Ubuntu) *** 

1. Go

	* sudo rm -rf /usr/local/go
	
	* sudo tar -C /usr/local -xzf go1.20.1.linux-amd64.tar.gz
	
	* cd về directory của user: cd ~
	
	* nano .profile
	
	* thêm dòng export PATH="$PATH:/usr/local/go/bin", sau đó save
	
	* source .profile

	* reboot lại máy

2. Chuyển file nhị phân được biên dịch sang folder bin trong project go

	* Thủ công: go build -o <đường dẫn folder bin>/<tên file nhị phân mới> <đường dẫn file go muốn dịch>

	* Tự động
	
		a. Thay đổi $GOPATH

			- lấy đường dẫn folder project.
			- echo GOPATH=<đường dẫn folder project>
		
		b. go install <file .go muốn dịch thành file nhị phân>

	* Sau đó muốn chạy nhị phân thì vô bin: ./<tên file>