# Mining Pool

Stratum Mining pool written in golang


This pool software is not a portal, but a standalone stratum server with high performance.

If you want, you can implement the portal page in frontend web.


## How to use it?

### Check

Make sure your algorithm is supported, eg: SHA256D, Scrypt, etc, if not, create an issue. 

### Configuration

Edit `config.example.json` and modify the configuration to set your Coin Daemon Settings 

 - Under daemons, you can add a primary and a backup Coin Server
 ```
 "daemons": [
    // Primary Server
    {
      "host": "127.0.0.1",
      "port": 19332,
      "user": "litecoinrpc",
      "password": "testnet"
    }
    // Backup Server
    {
      "host": "127.0.0.1",
      "port": 19332,
      "user": "litecoinrpc",
      "password": "testnet",
      "tls": {} // means tls enabled
    }
  ],
 ```
Then rename it to `config.json` 

### Build

go build


### Deploy

Copy `mining-pool` or `mining-pool.exe` and `config.json` to your VPS server and  

You will need Go and Redis-Server
 - Go - https://golang.org/
 - ```sudo apt install redis-server golang-go -y```

$ ./mining-pool

or

> mining-pool.exe

## Help
 - Bitcoind
```
$ bitcoind -rpcuser user -rpcpass password --testnet
```

 - <a href="https://github.com/btcsuite/btcd">BTCD</a>
```
$ ./btcd -rpcuser user -rpcpass password --testnet
```

 - Litcoind
```
$ ./litcoind -rpcuser user -rpcpass password --testnet
```

## TODO

- Main
- API
- More algorithms
- Web page
- ...

## Donation

  - **BTC**: bc1qlr36tpdwctfndcdgzx5ukjkqazl5hclkurw08q
  - **LTC**: M9SbgRV96Pg1rGVAfjvn8tVumio9MpESz5

## Tested Network
- LTC Testnet
- BTC Testnet
