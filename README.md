## Hướng dẫn sử dụng lấy query_id thủ công

**(Nếu đã có file `Profiles.xlsx` ở các kèo trước thì bỏ qua bước 1)**
### 1. Chuẩn bị Profiles.xlsx

#### Tạo file `Profiles.xlsx` gồm `profileName` và `toUrl` lần lượt là tên profile và proxy định dạng: `http://username:pass@ip:port`, nếu profile nào ko chạy proxy thì để trống.

#### Như hình 
![before](images/profile_before.png)

#### Thêm tính năng xoay vòng proxy:

+ field useProxyTxt: true or false //có dùng file proxy.txt hay không, có sẽ bỏ qua proxy trong profiles, dùng xoay vòng trong file proxy.txt
+ cột toUrl trong file Profiles có thể để trống, khi đó sẽ dùng proxy trong file proxy.txt xoay vòng.
+ Thêm proxy.txt file để xoay vòng nếu trong profile không config toUrl (proxy)
Hoặc khi proxy hiện tại bị lỗi sẽ thử lần lượt các proxy này. Nếu hết danh sách mà vẫn lỗi thì sẽ báo lỗi và dừng chạy acc hiện tại

+ Định dạng proxy: http://username:pass@ip:port

#### Nếu proxy chưa đúng định dạng 
=> Dùng tool convert proxy: https://t.me/W0lfairdrop/235

#### File mẫu: [Profiles.xlsx](file-mau/Profiles.xlsx)

### 2. Chuẩn bị data.xlsx

#### Tạo ra file `data.xlsx` (cùng cấp với file này) gồm `profileName` và `query_id` (giá trị có thể là `user_id` hoặc `query_id` hoặc `iframe`) nhưng tên cột phải để là query_id như hình:

![after](images/data.xlsx.png)

#### File mẫu: [data.xlsx](file-mau/data.xlsx)

!!!
Chú ý tên các cột phải để giống như mô tả **(kể cả chữ hoa chữ thường)** và giá trị `profileName` phải giống với `profileName` của file `Profiles.xlsx` để map với nhau.

### 3. CONFIG: Trong config.json 

### 4. Install: Chạy file `install.bat` hoặc ```npm install```

### 5. Chạy tool Chạy file `start.bat` hoặc ```node index.js```


## Contact
🛒 Mua tools - 🐞Report Bug - 🔓 Request Kèo - 🛫 Liên hệ: JoyDadDev (https://t.me/joydaddev)

## 🎁 Donate
![qr_code](tpbank999999.png)

