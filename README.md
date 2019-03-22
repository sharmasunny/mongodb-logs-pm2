## Description

PM2 module to automatically monitor vital signs of your mongodb :

*   Queries, input, updates, deletes
*   Number of connections
*   Used memory space
*   Network speed (input and output)
*   Repl name and status


# mongodb-logs-pm2

## Install

```bash
$ npm install pm2 -g

$ pm2 install mongodb-logs-pm2
```

## Configuration

**NODE** : User should have access to `admin` database to query statistics (see [mongo doc](http://mongodb.github.io/node-mongodb-native/2.2/api/Admin.html))

*   `mongodb_url` (Defaults to `none`) used for mongodb connection
*   `refresh_rate` (Defaults to `5000` in ms): Control the refresh rate of the worker

#### How to set these values ?

 After having installed the module you have to type :
`pm2 set mongodb-logs-pm2: `

e.g: 
- `pm2 set mongodb-logs-pm2:refresh_rate 5000` (every 5 seconds)
- `pm2 set mongodb-logs-pm2:mongodb_url mongodb://localhost:27017` (ip of my mongodb server)

## Uninstall

```bash
$ pm2 uninstall mongodb-logs-pm2
```

# License

MIT
