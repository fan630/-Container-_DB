### 基礎操作
1. 在Azure中 建立ｍysql instance, 並建立Table和schemma
2. 從本地csv文件中讀取資料, 並匯入到DB中
3. 更改display app裡面的connection string

### DB container
1. 透過dockerfile建立image
2. docker 指令如下

- sudo docker build -t appsqlimage .
- sudo docker login appregistry344343.azurecr.io -u appregistry344343 -p 8sgM6QTLp+n28F1zoxpiesuJZ54TW/PgqzeJlKtCk3+ACRAmiRl+ (log into the container registry)
- sudo docker tag appsqlimage appregistry344343.azurecr.io/appsqlimage
- sudo docker push appregistry344343.azurecr.io/appsqlimage
