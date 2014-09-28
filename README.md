firstbits
=========

daemon and query scripts to create, update, query the firstbits for a bitcoin address


 * Reads data from a bitcoind instance and inserts it into a mysql db
 * currently requires a lot of memory!
 * python dependencies:
   * python2.7
   * mysql.connector
   * time, requests, json, datetime

To run:

```
$ ./fbd path/to/fbd.conf
```

fbd.conf should be a plain-text file with key-value pairs for the following keys:

```
mysqluser=MYSQLUSER
mysqlpassword=MYSQLPASSWORD
mysqlhost=MYSQLHOST
rpcuser=BITCOINDRPCUSER
rpcpassword=BITCOINDRPCPASS
rpcport=8332
```

More info soon!
