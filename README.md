Bài tập của sinh viên: HOÀNG ĐỨC HỘI - MSV K225480106085 
Môn: Hệ quản trị CSDL 

BÀI TẬP VỀ NHÀ 02 - MÔN HỆ QUẢN TRỊ CSDL:

DEADLINE: 23H59 NGÀY 25/03/2025

ĐIỀU KIỆN: (ĐÃ LÀM XONG BÀI 1)
1. Đã cài đặt SQL Server 2022 Dev.
2. Đã cài đặt SQL Managerment Studio bản mới nhất.
3. Đã kết nối từ SQL Managerment Studio vào SQL Server.
4. Đã có tài khoản github, biết cách tạo repository(kho lưu trữ) cho phép truy cập public.

BÀI TOÁN:
- Tạo csdl quan hệ với tên QLSV gồm các bảng sau:
  + SinhVien(#masv,hoten,NgaySinh)
  + Lop(#maLop,tenLop)
  + GVCN(#@maLop,#@magv,#HK)
  + LopSV(#@maLop,#@maSV,ChucVu)
  + GiaoVien(#magv,hoten,NgaySinh,@maBM)
  + BoMon(#MaBM,tenBM,@maKhoa)
  + Khoa(#maKhoa,tenKhoa)
  + MonHoc(#mamon,Tenmon,STC)
  + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
  + DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)

YÊU CẦU:
1. Thực hiện các hành động sau trên giao diện đồ hoạ để tạo cơ sở dữ liệu cho bài toán:
  + Tạo database mới, mô tả các tham số(nếu có) trong quá trình.
  + Tạo các bảng dữ liệu với các trường như mô tả, chọn kiểu dữ liệu phù hợp với thực tế (tự tìm hiểu)
  + Mỗi bảng cần thiết lập PK, FK(s) và CK(s) nếu cần thiết. (chú ý dấu # và @: # là chỉ PK, @ chỉ FK)
2. Chuyển các thao tác đồ hoạ trên thành lệnh SQL tương đương. lưu tất cả các lệnh SQL trong file: Script_DML.sql

Mô tả chi tiết bài tập:

- Bước 1: Kết nối tài khoản SQL Server

![Image](https://github.com/user-attachments/assets/fc515a51-1d20-436c-af47-c92675f64dc6)

- Bước 2: Tạo Database

 - Sau khi kết nối thành công, nhấp chuột phải vào Cơ sở dữ liệu --> Cơ sở dữ liệu mới

![Image](https://github.com/user-attachments/assets/4117e850-d615-467d-9332-7e0884d07778)

- Đặt tên cho Cơ sở dữ liệu và nhấn 'Ok':

![Image](https://github.com/user-attachments/assets/cbae8ee9-04b8-4e5b-8b02-60d848b80756)

- Bước 3: Tạo Bảng
  
 - Nhấn vào dấu '+' tại Cơ sở dữ liệu vừa tạo,  ta sẽ tìm thấy 'Bảng' :

![Image](https://github.com/user-attachments/assets/e21a20d7-bd63-421a-9714-1d5336661cc6)

- Nhấn chuột phải vào Tables --> New ---> Table:

![Image](https://github.com/user-attachments/assets/88f99a20-2320-4c67-ab7c-4c3def73a39b)

Thực hiện bổ sung các thuộc tính theo yêu cầu vào mỗi bảng với loại dữ liệu phù hợp với thuộc tính đó ---> Ctrl S để lưu bảng và đặt bảng tên

![Screenshot 2025-04-09 002756](https://github.com/user-attachments/assets/9f3df95b-6dde-4143-8b77-24be677ac4d2)

![Screenshot 2025-04-11 220550](https://github.com/user-attachments/assets/1f335c5b-49ea-4024-b4c5-cbb8bfcf2ad3)


![Screenshot 2025-04-11 220736](https://github.com/user-attachments/assets/328ce39c-e3d1-4173-8770-c8070f82cc17)


![Screenshot 2025-04-11 220901](https://github.com/user-attachments/assets/5f2e6c03-a8cd-461b-9e68-293948c2ef95)


![Screenshot 2025-04-11 221129](https://github.com/user-attachments/assets/fa49a0de-7a2e-4398-a1b0-857002afedc9)



![Screenshot 2025-04-11 221259](https://github.com/user-attachments/assets/b2ca9e29-8924-493d-aaa1-367b91e8607e)




![Screenshot 2025-04-11 221343](https://github.com/user-attachments/assets/741108a4-17fa-481a-b0b3-771cebcf9b75)


![Screenshot 2025-04-11 221742](https://github.com/user-attachments/assets/207dfbdf-1fc1-4b29-aa12-9ac77405f3f8)


![Screenshot 2025-04-11 221944](https://github.com/user-attachments/assets/8f927a4a-2df7-4890-b1a2-8ab21107d207)

![Screenshot 2025-04-11 222145](https://github.com/user-attachments/assets/ff9f8aeb-370d-4229-bd75-bf172d2418d3)

- Bước 4: Thêm cưỡng bức vào những bảng có thuộc tính cần thiết buộc phải cưỡng bức

Click chuột phải vào khoảng trống bất kỳ trong mục 'Design' của bảng ---> Kiểm tra ràng buộc

![Screenshot 2025-04-11 222326](https://github.com/user-attachments/assets/bee44020-b5c5-4b08-b278-b1b49aee2fa9)

Thêm ----> Biểu thức (điều kiện khô ráo)

![Screenshot 2025-04-11 223718](https://github.com/user-attachments/assets/4522abbc-0bc0-4dcd-801e-eadc1f6db540)

![Screenshot 2025-04-11 224010](https://github.com/user-attachments/assets/fa37d7d6-5379-4be3-a80c-bcc4c6bb3290)

- Bước 5: Cài khóa chính cho các thuộc tính trong bảng:

Có 2 cách để cài đặt thuộc tính trở thành khóa chính:
Cách 1: Bấm chuột phải thuộc tính ---> đặt khóa chính


![Screenshot 2025-04-11 225719](https://github.com/user-attachments/assets/daf49a35-3c6a-4656-898a-22417ec7db81)

![Screenshot 2025-04-11 231014](https://github.com/user-attachments/assets/d2434bb3-f4d7-4389-a71e-af3d9449b020)

- Bước 5.1: Cài đặt khóa ngoại(FK) cho các thuộc tính:

Chỉ có thể cài đặt ngoại khóa khi thuộc tính đó là khóa chính tại một bảng mà chúng tôi muốn liên kết tới

Click chuột phải vào bất kỳ kỳ hạn nào trong bảng 'Thiết kế' ---> Mối quan hệ

![Screenshot 2025-04-12 233129](https://github.com/user-attachments/assets/2147352f-9c7a-40e5-b621-aabc299fa348)

- Add(thêm khóa ngoại) ----> Nhấn vào '...' tại Đặc tả bảng và cột ( liên kết khóa chính của bảng này với khóa ngoại lệ của bảng kia)

- Tại Insert And Update đặc tả ----> chọn Update Rule : CASCADE ( CASCADE để bảo đảm tính chất tối đa của dữ liệu, nếu dữ liệu của khóa thuộc tính chính bị thay đổi thì dữ liệu của khóa ngoại tại liên kết bảng cũng sẽ thay đổi)

![anh1](https://github.com/user-attachments/assets/95d7b8a7-c7b6-420e-8805-383959a81827)

![anh2](https://github.com/user-attachments/assets/5ba132c4-882b-4593-b228-d46a0e630cb7)

![anh3](https://github.com/user-attachments/assets/b6c157e6-4e06-4bd8-b4f0-bb51d1f76b53)

![anh4](https://github.com/user-attachments/assets/e865a810-ba61-473d-b018-ca5ca2a87772)

![anh5](https://github.com/user-attachments/assets/638b5d3f-1291-4d85-a888-2b9dfd3d9993)

![anh6](https://github.com/user-attachments/assets/2842c896-1752-49ee-9b15-c10e7859f32e)

![anh7](https://github.com/user-attachments/assets/3369f81f-de6f-454f-aa6e-a6bb1f46acd3)

![anh8](https://github.com/user-attachments/assets/a1017d6d-e2c9-4b48-aef0-fe134d62c687)

![anh9](https://github.com/user-attachments/assets/4a517ae0-74fc-4fe7-8001-49d5084b2ad1)

![anh10](https://github.com/user-attachments/assets/5e9df6af-09c6-49a8-b78d-cf833c4a5135)

![anh11](https://github.com/user-attachments/assets/d21846ce-aa74-4c46-a2f8-d6750ceca89d)

![anh12(1)](https://github.com/user-attachments/assets/7c5a1217-96fa-42f1-9e8d-f63e7f4e2e40)


- Lệnh SQL sau khi chuyển từ thao tác đồ họa:

Nhấn chuột phải vào bảng tên(dbo. Name Table) ----> Scrip Table ----> CREATE To ----> New Query Editor WindowWindow:

![Screenshot 2025-04-12 235033](https://github.com/user-attachments/assets/f8601574-8ade-49b0-a630-bbd0c4ca97da)




