# yallalive.vps
## OS: Ubuntu 22.04.2 LTS
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
6. switvh to yallalivedb databasse:
```mongo shell
 use yallalivedb
```

