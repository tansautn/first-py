# Fisrt Step To Python
## Day 1

### Đặc tính cơ bản của python
1. Object
- Mọi dữ liệu của python đều được diễn giải dưới dạng object
- Hay nói 1 cách khác, object là lớp trừu tượng cho mọi loại dữ liệu
- Giống như các ngôn ngữ khác. Object trong python cũng có property và method.
- Trong đó, property phục vụ việc lưu trữ các thuộc tính
- Method là thể hiện các hành động của object đó
- Mỗi object đều có id là bất biến trong python

2. Datatype built-in
- Giống với các ngôn ngữ khác. Python cũng có dạng dữ liệu là hằng số, và biến số
- Sử dụng dữ liệu là việc khai báo 1 hằng hoặc biến với tên nhất định, đi kèm với giá trị
- Các kiểu dữ liệu có sẵn trong py gồm có : Number (Số), String (chữ), Collection (Tập hợp)

### Cài đặt python
1. Homepage : https://www.python.org/
2. Phiên bản sử dụng : 3.x
3. Các phần cài đặt kèm : pip (Python package manager). Tick `install pip` khi thực hiện cài đặt python
4. Virtualenv
- Virtualenv giúp chúng ta quản lý các project 1 cách dễ dàng mà ko phải lo lắng vấn đề conflict.
- Lấy ví dụ ban đầu chúng ta làm việc trên 1 dự án sử dụng django 1.7.x để tạo web.
- Dự án tiếp theo sử dụng django 1.8.x. Với venv chúng ta vẫn có thể cài và sử dụng django 1.8 mà ko ảnh hưởng tới dự án 1.7 trước đó
- Để cài đặt venv. Sau khi cài đặt xong python và pip. Chạy cmd và chạy đoạn lệnh sau : `pip install virtualenv`

### Tạo project mới và triển khai venv
1. Tạo 1 thư mục mới tên : `first-py`
2. Mở cmd, cd vào thư mục vừa tạo.
3. chạy lệnh sau : `virtualenv venv`. Một thư mục mới có tên `venv` sẽ được tạo ra.
4. Active venv: Windows - chạy file : .\venv\Scripts\active.bat hoặc active.ps1 nếu dừng powershell

### Python console
- Python có hỗ trợ interactive shell. Trên interactive shell ta có thể code, và chạy các dòng lệnh ngay lập tức.
- Sử dụng python console giúp test các đoạn code ngắn, hoặc debug trở nên dễ dàng nhất.
- Để khởi động python console từ cmd chạy `python`.
- Python console có 2 kiểu dấu nhắc.
- `>>>` thể hiện console đang chờ đợi 1 dòng hoặc đoạn lệnh mới
- `...` thể hiện console đang chờ đợi các dòng lệnh tiếp theo (đoạn lệnh gồm nhiều dòng). Tương đương với thụt dòng trong script

### Python scripts (*.py)
- Scripts trong python thường được lưu với phần mở rộng`.py`
- Python sử dụng các dấu thụt đầu dòng và 1 dòng trắng để phân chia các đoạn lệnh liên tiếp
- Ví dụ :
```
start = 1
while (start < 5):
    #Bắt đầu statement while: Tụt dòng
    start += 1
    print('Still inside the loop')
    print('Start is ' + str(start))
    if(start % 2 == 0):
    #Bắt đầu statement if: Tụt dòng
        print('Even number')

#Kết thúc các statements trên, dùng 1 dòng trống
start += 10
print('Outside the loop')
print('Start is ' + str(start))
```

Kết quả khi chạy script

```
Still inside the loop
Start is 2
Even number
Still inside the loop
Start is 3
Still inside the loop
Start is 4
Even number
Still inside the loop
Start is 5
Outside the loop
Start is 15
```

### Sắp xếp code trong python
1. Trong python, mỗi file `*.py` đc coi là 1 module
2. Package : nếu 1 thư mục có chứ `__init__.py`. Được hiểu rằng cả thư mục đó là 1 package.
3. Sử dụng package, giúp ứng dụng clear hơn về cấu trúc, và cũng dễ dàng kiểm soát - bảo trì về sau
4. Ví dụ về 1 app và package.

`tree -v example`

```
example/
├── core.py
├── run.py
└── util
    ├── __init__.py
    ├── db.py
    ├── math.py
    └── network.py
```
*Các module: * `core.py` & `run.py`
*Packages: * `util`

So sáng với app chỉ bao gồm các modules

`tree -v files_only`

```
files_only/
├── core.py
├── db.py
├── math.py
├── network.py
└── run.py
```

