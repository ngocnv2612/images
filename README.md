## Hướng dẫn sử dụng lấy query_id thủ công

**(Nếu đã có file `Profiles.xlsx` ở các kèo trước thì bỏ qua bước 1)**
### 1. Chuẩn bị Profiles.xlsx

#### Tạo file `Profiles.xlsx` gồm `profileName` và `toUrl` lần lượt là tên profile và proxy định dạng: `http://username:pass@ip:port`, nếu profile nào ko chạy proxy thì để trống.

#### Như hình 
![before](images/profile_before.png)

#### Nếu proxy chưa đúng định dạng 
=> Dùng tool convert proxy: https://t.me/W0lfairdrop/235

#### File mẫu: [Profiles.xlsx](Profiles.xlsx)

### 2. Chuẩn bị data.xlsx

#### Tạo ra file `data.xlsx` (cùng cấp với file này) gồm `profileName` và `query_id` (giá trị có thể là `user_id` hoặc `query_id` hoặc `iframe`) nhưng tên cột phải để là query_id như hình:

![after](images/data.xlsx.png)

#### File mẫu: [data.xlsx](data.xlsx)

!!!
Chú ý tên các cột phải để giống như mô tả **(kể cả chữ hoa chữ thường)** và giá trị `profileName` phải giống với `profileName` của file `Profiles.xlsx` để map với nhau.

### 3. CONFIG: Trong config.json 

### 4. Install: Chạy file `install.bat` hoặc ```npm install```

### 5. Chạy tool Chạy file `start.bat` hoặc ```node index.js```


## Contact
🛒 Mua tools - 🐞Report Bug - 🔓 Request Kèo - 🛫 Liên hệ: JoyDadDev (https://t.me/joydaddev)

## 🎁 Donate
![qr_code](tpbank999999.png)

