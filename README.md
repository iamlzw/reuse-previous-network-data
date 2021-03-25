# reuse-previous-network-data
reuse previous network data to create an network

clone repo

```bash
git clone https://github.com/iamlzw/reuse-previous-network-data.git
cd reuse-previous-network-data
docker-compose -f docker-compose-simple.yaml up -d 

docker exec -it cli bash

peer chaincode query -n mycc -c '{"Args":["query","a"]}' -C myc

##the result should be 20

## set a 100
peer chaincode invoke -n mycc -c '{"Args":["set", "a", "100"]}' -C myc

```
stop network

```bash
docker-compose -f docker-compose-simple.yaml down
```
now you can copy this project to other host ,when you start this network,the data will not lose and you wil get sam result


