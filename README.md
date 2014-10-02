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

Note that your bitcoind instance needs to be running with `-txindex=1`.

To query the database, use the fbq program, provide a location for a config file, then
request a firstbits to addrss with -f, or address to firstbits with -a.

```
$./fbq --config /path/to/fbd.conf -f 1SgtS
address: 1sGtsSJBktENuS4Hu2HccA91uuhERC6RX
firstbits: 1sgts
height: 212718

$./fbq --config /path/to/fbd.conf -a 1sGtsSJBktENuS4Hu2HccA91uuhERC6RX
address: 1sGtsSJBktENuS4Hu2HccA91uuhERC6RX
firstbits: 1sgts
height: 212718
```
