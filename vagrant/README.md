*** Cài đặt ***

1. Tài Vagrant trên ubuntu

    * cd về home
    * sudo apt update
    * wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
    * echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
    * sudo apt update && sudo apt install vagrant

2. Tải VirtualBox

    * Vào trang web của virtualbox, tài phiên bản dành cho ubuntu 20.04
    * dpkg -i <tên package virtualbox đã tải về>
    * thêm dependency còn thiếu sudo apt --fix-broken install

*** Sử dụng ***

Lên chat gpt giải thích mã vagrant

1. Tạo môi trường vagrant

    * cd vào thư mục chứa vagrantfile
    * vagrant init
    * chỉnh sủa vagrantfile
    * vagrant up: bật máy ảo
    * truy cập vào terminal máy ảo đã setup trong file: vagrant ssh
    * tài khoản máy ảo lúc này:
        a. username & password đều là vagrant

2. Chú ý khi thêm bộ mạng bắc cầu trong Virtual Box

    * Nhớ để ý mục Name
    * Vào máy host lấy ip trỏ tới adapter mới tạo: lệnh: ip addr
    * Để ý Ip có Name tương ứng

*** Học liệu ***

    * https://vntechies.dev/courses/90-ngay-devops/ngay-14-buc-tranh-lon-devops-va-linux