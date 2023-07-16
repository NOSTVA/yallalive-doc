# yallalive.vps Ubuntu 22.04.2 LTS
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
