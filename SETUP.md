# Perintah Setup Backend (sesuai urutan bab di ebook)

## Membuat Project Golang
Buat folder `backend-golang`, buka terminal di dalamnya, lalu jalankan:

```
go mod init santrikoding/backend-api
go get -u github.com/gin-gonic/gin@v1.10.0
```

Uji coba aplikasi (buka http://localhost:3000):

```
go run main.go
```

## Konfigurasi File .env

```
go get github.com/joho/godotenv@v1.5.1
```

## Konfigurasi Database

```
go get -u gorm.io/gorm@v1.25.12
go get -u gorm.io/driver/mysql@v1.5.7
```

Buat database baru bernama `db_golang` di MySQL (phpMyAdmin: http://localhost/phpmyadmin) sebelum menjalankan aplikasi, supaya tidak error saat auto migrate.

## Installasi dan Membuat Middleware Auth

```
go get github.com/golang-jwt/jwt/v5@v5.2.2
```

Tambahkan `JWT_SECRET=` di file `.env`. Isinya dibuat (generate) lewat https://jwtsecret.com/generate.

## Membuat Helper Validator

```
go get github.com/go-playground/validator/v10@v10.26.0
```
