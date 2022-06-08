# Laravel-SSO(Idp)

## 安裝

### 安裝相依套件
`composer install && npm install`

### 產生key
`php artisan key:generate`

### 建立所需資料表
`php artisan migrate`

### 安裝passport
`php artisan passport:install --uuids`
[yes]

### 啟動服務並新增一位使用者
`php artisan serve`

### 設定client
`php artisan passport:client`
[1, sp, http://localhost:8080/callback]

### 將產生出來的Client ID及Client secret貼到Sp的.env[CLIENT_ID, CLIENT_SECRET]

## 新增/修改sp
1. 修改config/auth.php的sps
2. 在app/Providers/AuthServiceProvider.php中修改權限Passport::tokensCan
3. 在routes/api.php中修改傳回的使用者資料


## Done!