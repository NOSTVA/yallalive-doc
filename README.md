# yallalive.vps Ubuntu 22.04.2 LTS

## Connecting to the VPS
To connect your VPS server, you can use your server IP, you can create a root password and enter the server with your IP address and password credentials. But the more secure way is using an SSH key.
```code
ssh root@<server ip address> 
```

## Project Directory
1. o navigate to the Yallalive project directory, run the following command in your terminal:
```code
cd ~/app/yallalive-hostinger
```
2. To list the contents of the directory, run the following command in your terminal:
```code
ls
```
3. To edit the .env file for either the yallalive-api or yallalive-admin project, run one of the following commands in your terminal:
```code
nano ~/app/yallalive-hostinger/yallalive-api/.env
# or
nano ~/app/yallalive-hostinger/yallalive-admin/.env
```

## NGINX
1. To check the status of the NGINX service, run the following command in your terminal:
```code
systemctl status nginx
```
2. To check the Yallalive NGINX configurations, run the following command in your terminal:
```code
cd /etc/nginx/sites-available/
nano yallalive
```
3. The Yallalive React build files are located in the following directory: `/var/www/yallalive/client`
4. The Yallalive Node.js App runs on port 3000.

## PM2
Yallalive Node.js proccess is managed by PM2 with the name **api** and id **0**
1. To check the status of yallalive process:
```code
pm2 status 0
```
2. To display the logs of yallalive process:
```code
pm2 logs 0 --lines 2000
```
3. To restart yallalive process:
```code
pm2 restart 0
```

## MongoDB
To use MongoDB on your yallalive.vps Ubuntu 22.04.2 LTS server, follow these steps:
1. To check the status of the MongoDB service, run the following command in your terminal:
```code
systemctl status mongod
```
3. To connect to the MongoDB shell, run the following command in your terminal
```code
mongo -u admin -p --authenticationDatabase admin
# When prompted for a password, enter `admin123`.
```
3. To verify that you are authenticated as the user you created above, run the following command in the MongoDB shell
``` mongo shell
db.runCommand({connectionStatus : 1})
```
4. To show a list of all databases running in MongoDB, run the following command in the MongoDB shell:
```mongo shell
 show dbs
```
6. To switch to the yallalivedb database, run the following command in the MongoDB shell:
```mongo shell
 use yallalivedb
```
7. To show a list of all collections in the yallalivedb database, run the following command in the MongoDB shell:
```mongo shell
show collections
```
8. To show the contents of a particular collection, such as the **products** collection, run the following command in the MongoDB shell:
```mongo shell
db.products.find()
```
