### Build

```
1. git clone https://github.com/sanketh2020/HadoopPlatform.git
2. cd HadoopPlatform/docker
3. docker build .
  
```

### Execute
   
```
docker run --name hadoop-cluster -it -d -p 2122:2122 -p 8030:8033 -p 8040:8040 -p 8088:8088 -p 8042:8042 -p 49707:49707 -p 19888:19888 -p 50020:50020 -p 50010:50010  -p 50075:50075 -p 50090:50090 -p 50070:50070 -p 9000:9000 sequenceiq/hadoop-docker:2.7.1 /etc/bootstrap.sh -bash

```
### Stop

```
docker stop hadoop-cluster
docker rm hadoop-cluster
```


### Run hadoop commands

```
docker exec -t hadoop-cluster /usr/local/hadoop/bin/hdfs dfs -ls /
```

### Test
```
 http://localhost:50070
```
