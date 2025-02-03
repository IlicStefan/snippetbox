# SNIPPETBOX


#### My implementation of Alex Edwards' book [Let's Go](https://lets-go.alexedwards.net/)


:camera: Screenshot

![Screenshot from 2024-10-26 13-12-33](https://github.com/user-attachments/assets/172134ef-1904-4f26-a833-9c00a5aefbd7)

🔧 Setup

Install Go compiler:
```
$ sudo apt install golang-go
```
Clone project:
```
$ git clone https://github.com/IlicStefan/snippetbox/
```
Upgrade packages:
```
$ go mod download
$ go mod verify
```
Install MySql:
```
$ sudo apt install mysql-server
```
Create database:
```
$ sudo mysql 
```
```
mysql> CREATE DATABASE snippetbox CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
mysql> USE snippetbox;
```
Create user:
```
mysql> CREATE USER 'web'@'localhost';
mysql> GRANT ALL PRIVILEGES ON snippetbox.* TO 'web'@'localhost';
mysql> FLUSH PRIVILEGES;
mysql> ALTER USER 'web'@'localhost' IDENTIFIED BY 'pass';
```

:steam_locomotive: Run

How to start the server:
```
$ make run
```
How to start the database:
```
$ mysql -D snippetbox -u web -p
```
How to execute migration scripts:
```
$ migrate -database "mysql://web:pass@tcp(localhost:3306)/snippetbox" -path migrations up
```
