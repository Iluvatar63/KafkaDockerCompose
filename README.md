# KafkaDockerCompose
This project is used to simulate a Kafka environment close to the production one.

## Composition
3 Brokers
1 Schema registry
1 Zookeeper
1 Kafka-connect
1 Kafka-rest
1 Control center
1 AKHQ
~~1 NS4Kafka~~

# How to use it?
## Michelin Docker Artifactory
If you are trying to get an image from Michelin Artifactory, use this command lines in PowerShell and authenticate using your account:
```
docker login https://docker.artifactory.michelin.com -u fXXXXX -p MyPass
```

## wslconfig
Configure Docker with enough memory to run this sample.
### Stop WSL
Stop Docker, then run
```
wsl --shutdown
```
### Create the file
Create a file in C:\Users\<yourUserName>\.wslconfig
```
[wsl2]
memory=6GB # Limits VM memory in WSL 2 up to 3GB
processors=4 # Makes the WSL 2 VM use two virtual processors
```

### Restart WSL instance
Run Docker.

## Docker compose command
```
docker-compose -f "docker-compose.yaml" up -d --build
```