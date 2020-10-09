# Mining Pool

Stratum Mining pool written in golang

## Difference from NOMP(node-node-open-mining-portal)

This pool software is not a portal, but a standalone stratum server with high performance.

If you want, you can implement the portal page in frontend web.

## Why standalone?

Keep standalone is better to assemble new algorithm/coin to your pool services, without dealing with C lib conflicts or restart the whole site to append new pool, what's more, most pool operators don't need a portal, they just get benefit from few different coins with different algorithms.

So it's obviously that standalone one with more advantages on deploying and maintaining.


## How to use it?

### 0x00 Check

Make sure your algorithm is supported, eg: SHA256D, Scrypt, etc, if not, create an issue. 

### 0x01 Configuration

Edit `config.example.json` and modify the configuration to set your Coin Daemon Settings 

Then rename it to `config.json` 

### Build

go build


### Deploy

Copy `mining-pool` or `mining-pool.exe` and `config.json` to your VPS server and  

You will need Go and Redis-Server
Go - https://golang.org/doc/install
sudo apt install redis-server -y

$ ./mining-pool

or

> mining-pool.exe


## TODO

- Main
- API
- More algorithms
- Web page
- ...

## Donation

**BTC**: 13dQsauPkqSXYnwQedqaLRadtMm1tjCEPx

## Tested Network
- LTC Testnet
- BTC Testnet
