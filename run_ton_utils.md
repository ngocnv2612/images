## Hướng dẫn sử dụng tool Ton utils

- Ton utils bao gồm các tools: send ton, check ton balance, gom ton
### 🔓 Yêu cầu: 

#### Cài nodejs
#### Có ton api key

Vào https://t.me/tonapibot để tạo api key

![alt text](/images/ton-apikey.png)

```
API_KEY=da26c544xxxxxxxxxxxx
```

### 1. Tool Send Ton
- Để send gas cho các ví khác
#### 1.1 Chuẩn bị file send-ton.xlsx cùng cấp với file này chứa các địa chỉ muốn gửi ton

##### File mẫu: [send-ton.xlsx](file-mau/send-ton.xlsx)

#### 1.2 Config.json
```
  "numThreads": 10, //không cần config với tool này

  "delayTime": 5, //không cần config với tool này

  "delayTimePerApiCall": 0.5,

  "delayTimeEachBatch": 0.5,

  "API_KEY":"", // ton api key lấy được ở setup

  "TON_VERSION": "v4R2", //ton version, hiện tại chỉ hỗ trợ đến v4R2, ko hỗ trợ version cao hơn như w5

  "AMOUNT_TON": 0.02, // số lượng ton muốn chuyển đến từng ví

  "CHECK_BALANCE":true, // muốn check balance hiện tại của ví nhận không. true/false. nếu điền có thì sẽ kiểm tra balance hiện tại. nếu > AMOUNT_TON thì sẽ skip ví này, không cần chuyển nữa.

  "SENDER_SEED_PHRASE": "", //seed pharse của ví gửi

  "RECEIVER_ADDRESS": "", //không cần config với tool này

  "GAS_FEE": 0.03 //không cần config với tool này
```

#### 1.3 Run tool

##### Install: Chạy file install.bat hoặc `npm install`

##### Chạy tool Chạy file sendTon.bat hoặc `node sendTon.js`


### 2. Tool Check Ton Balance

- Để kiểm tra ton trong từng ví (có thể kiểm tra sau hoặc trước khi chạy tool send ton)

#### 2.1 Chuẩn bị file check_ton_balance cùng cấp với file này chứa các địa chỉ muốn check ton balance

##### File mẫu: [send-ton.xlsx](file-mau/check_ton_balance.xlsx)

#### 2.2 Config.json
```
  "numThreads": 10, //sô lượng ví muốn kiểm tra đồng thời. Nên dựa theo ton api key của bạn cho phép bao nhiêu query đồng thời.

  "delayTime": 5, //không cần config với tool này

  "delayTimePerApiCall": 0.5,

  "delayTimeEachBatch": 0.5,

  "API_KEY":"", // ton api key lấy được ở setup

  "TON_VERSION": "v4R2", //ton version, hiện tại chỉ hỗ trợ đến v4R2, ko hỗ trợ version cao hơn như w5

  "AMOUNT_TON": 0.02, //không cần config với tool này

  "CHECK_BALANCE":true, //không cần config với tool này

  "SENDER_SEED_PHRASE": "", //không cần config với tool này

  "RECEIVER_ADDRESS": "", //không cần config với tool này

  "GAS_FEE": 0.03 //không cần config với tool này
```

#### 2.3 Run tool

##### Install: Chạy file install.bat hoặc `npm install`

##### Chạy tool Chạy file checkTonBalance.bat hoặc `node checkTonBalance.js`

#### 2.4 Sau khi chạy xong sẽ tạo ra file check_ton_balance_report.xlsx để xem kết quả

### 3. Tool Gom Ton

- Sau khi claim token nào đó (Dogs chẳng hạn), bạn muốn gom Ton từ các ví phụ về ví chính.

#### 3.1 Chuẩn bị file gom-ton.xlsx cùng cấp với file này chứa các địa chỉ muốn gom ton

##### File mẫu: [send-ton.xlsx](file-mau/gom-ton.xlsx)

#### 3.2 Config.json
```
  "numThreads": 10, //sô lượng ví muốn gom đồng thời. Nên dựa theo ton api key của bạn cho phép bao nhiêu query đồng thời.

  "delayTime": 5,

  "delayTimePerApiCall": 0.5,

  "delayTimeEachBatch": 0.5,

  "API_KEY":"", // ton api key lấy được ở setup

  "TON_VERSION": "v4R2", //ton version, hiện tại chỉ hỗ trợ đến v4R2, ko hỗ trợ version cao hơn như w5

  "AMOUNT_TON": 0.02, //không cần config với tool này

  "CHECK_BALANCE":true, //không cần config với tool này

  "SENDER_SEED_PHRASE": "", //không cần config với tool này

  "RECEIVER_ADDRESS": "", //địa chỉ ví chính muốn nhận ton từ các ví phụ

  "GAS_FEE": 0.03 //phí gas ước tính để đảm bảo số Ton trong ví phụ phải > con số này để transaction thành công.
```

#### 3.3 Run tool

##### Install: Chạy file install.bat hoặc `npm install`

##### Chạy tool Chạy file gomTon.bat hoặc `node gomTon.js`

#### 3.4 Sau khi chạy xong sẽ tạo ra file gom_ton_report.xlsx để xem kết quả

## Contact
🛒 Mua tools - 🐞Report Bug - 🔓 Request Kèo - 🛫 Liên hệ: JoyDadDev (https://t.me/joydaddev)

## 🎁 Donate
![qr_code](tpbank.png)