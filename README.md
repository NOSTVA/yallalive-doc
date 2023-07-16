# yallalive.vps
## OS: Ubuntu 22.04.2 LTS
## MongoDB
1. To check the status of the MongoDB service. run:
`systemctl status mongod`
2. To connect to mongodb shell.
`mongo -u admin -p --authenticationDatabase admin`
> password: admin123
3. verify that you are the authenticated user you created above
`db.runCommand({connectionStatus : 1})`
4. To show the list of all databases running:
`show dbs`
5. switvh to yallalivedb databasse:
`use yallalivedb`
