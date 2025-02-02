💻 snippetbox

My implementation of Alex Edwards' book [Let's Go](https://lets-go.alexedwards.net/)

🎥 Screenshot

![Screenshot from 2024-10-26 13-12-33](https://github.com/user-attachments/assets/172134ef-1904-4f26-a833-9c00a5aefbd7)

🔧 Tools

How to run:

First, you need to install the Go compiler:
```
sudo apt install golang-go
```
Install MySql:
```
sudo apt install mysql-server
```
Create database:
```
CREATE DATABASE snippetbox CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE snippetbox;
```
Create user:
```
CREATE USER 'web'@'localhost';
GRANT SELECT, INSERT, UPDATE, DELETE ON snippetbox.* TO 'web'@'localhost';
-- Important: Make sure to swap 'pass' with your own password.
ALTER USER 'web'@'localhost' IDENTIFIED BY 'pass';
```
How to start the server:
```
make run
```
How to start the database:
```
mysql -D snippetbox -u web -p
```
