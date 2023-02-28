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
	
		a. Thay đổi $GOPATH - làm mỗi lần trong terminal session

			- lấy đường dẫn folder project.
			- export GOPATH=<đường dẫn folder project>
		
		b. go install <file .go muốn dịch thành file nhị phân>

	* Sau đó muốn chạy nhị phân thì vô bin: ./<tên file>

3. Tạo một module và quản lý module trong folder src của project Go

	* Tạo folder mới trong src

	* cd vào folder source (hoặc nơi nào bên ngoài có thể thấy hết các module)

	* go mod init <tên module>: ví dụ: go mod init github.com/tienanng/go-Twitter-bot

4. Khai báo biến môi trường trên hệ điều hành linux sử dụng lệnh export

	* export TÊN_BIẾN=giá_trị

5. Tải package trên github băng go get

	* cd vào thư mục chứa file go.mod

	* got get <link package trên github>
	
	* các gói được tải về sẽ ở trog folder pkg (vì trong trong GOPATH)

6. Biên dịch phần mềm cho các ghệ hiều hành khác nhau

	* Chỉnh sửa môi trường trong Go cho phù hợp với hệ điều hành muốn biên dịch ra (GOOS VÀ GO ARCH)