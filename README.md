# WebDollar Miner Tips & Tricks
WebDollar Miner Tips &amp; Tricks, debugging, error explaining and relevant info

#### 1. You get this error on Raspberry Pi or on any other system.
```
Unhandled rejection Error: Unknown system error -117: unknown system error -117 link /home/YOUR_USER/.npm/_cacache/tmp/....etc
``` 
#### You need to run this command:
```
npm cache clear --force
bash install-miner.sh
```
----
#### 2. PushWork errors
```
PushWork raised an error { message: 'WorkDone: Answer is null' }
```
#### You are not connected to the Pool or got disconnected by it. Get in touch with the pool owner.
----
#### 3. Block xxxyyy was not mined...
```
block 696666 was not mined...
```
#### That's just a notification that tells you the block was not mined. You can see a lot of lines like this when CPU_MAX is set to -100 and you're mining only POS
----
#### 4. You get gyp ERR! build error
```
gyp ERR! build error
gyp ERR! stack Error: `make` failed with exit code: 2
.
.
.
.
gyp ERR! node -v v0.10.25
.
.
.
```
#### You don't have the required node version: v8.2.1. You need to remove your local node version and use ```bash install-miner.sh``` to install the correct version.
----
#### 5. You get: ```not enough funds to mine POS. It is required 100 WEBD to mine POS```
#### Your wallet must have a minimum of 100 WEBD to mine POS (stake)
----
#### 6. You get:
```
Error: listen EACCESS 0.0.0.0:80
```
#### Run your WebDollar Miner on another port, e.g.: SERVER_PORT=8080 npm run commands






