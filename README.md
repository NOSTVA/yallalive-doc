# yallalive.vps Ubuntu 22.04.2 LTS
## MongoDB
1. To check the status of the MongoDB service. run:
```code
systemctl status mongod
```
3. To connect to mongodb shell.
```code
mongo -u admin -p --authenticationDatabase admin
```
> password: admin123
3. verify that you are the authenticated user you created above
``` mongo shell
db.runCommand({connectionStatus : 1})
```
4. To show the list of all databases running:
```mongo shell
 show dbs
```
6. switch to yallalivedb database:
```mongo shell
 use yallalivedb
```
7. To show a list of all collections in yallalivedb
```mongo shell
show collections
```
8. To show content of a particular collection, i.e. **products**
```mongo shell
db.products.find()
```
