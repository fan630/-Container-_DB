## 基礎操作
1. 在Azure中 建立ｍysql instance, 並建立Table和schemma
2. 從本地csv文件中讀取資料, 並匯入到DB中
3. 更改display app裡面的connection string

## DB container
透過mac dockerfile建立image, 確保terminal在這裡

## docker 指令如下
sudo docker build -t appsqlimage .

### Azure 作法
- sudo docker login appregistry344343.azurecr.io -u appregistry344343 -p 8sgM6QTLp+n28F1zoxpiesuJZ54TW/PgqzeJlKtCk3+ACRAmiRl+ (log into the container registry)
- sudo docker tag appsqlimage appregistry344343.azurecr.io/appsqlimage
- sudo docker push appregistry344343.azurecr.io/appsqlimage

### Aliyun 作法
<img width="1028" alt="截圖 2024-01-07 下午6 36 45" src="https://github.com/fan630/Container_DB/assets/48875309/387789fa-bc11-4c1b-935e-d94143ea4ddc">

成功會像是這樣, 可以看到tag

<img width="711" alt="截圖 2024-01-07 下午6 37 35" src="https://github.com/fan630/Container_DB/assets/48875309/6ca48b4d-f4df-42f3-9a3e-6e1526a38ef6">

透過這個自定義的image, 啟動一個ECI, 並賦予一個外部ip

<img width="712" alt="截圖 2024-01-07 下午6 39 36" src="https://github.com/fan630/Container_DB/assets/48875309/3c845faa-a088-45b9-bc3c-bc84630247ac">
