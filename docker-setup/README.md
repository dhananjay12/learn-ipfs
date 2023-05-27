## IPFS docker setup

You may have to provide access to the temp volumes (ipfs-*). 
Run from docker-compose.yml directory:

```bash
sudo chmod -R 755 ipfs-*
```
Spin up the containers:

```bash
docker-compose up
```

### Upload/Download a file

https://docs.ipfs.tech/reference/kubo/rpc/#getting-started

```bash
curl -F file=@README.md  http://localhost:5001/api/v0/add
```
Where README.md is the file you want to upload. You have to add `@`
Above will return a hash, which you can use to retrive the file.

*Retrive via Gateway*
```bash
curl http://localhost:8080/ipfs/<hash>
```


