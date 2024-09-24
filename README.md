Command from community:

```
docker run -p 8081:8081 -p 10250:10250 -p 10251:10251 -p 10252:10252 -p 10253:10253 -p 10254:10254 -p 10255:10255 --env AZURE_COSMOS_EMULATOR_ENABLE_DATA_PERSISTENCE=1 --env AZURE_COSMOS_EMULATOR_IP_ADDRESS_OVERRIDE=127.0.0.1 --name cosmos-emulator --pull missing -t -i mcr.microsoft.com/cosmosdb/linux/azure-cosmos-emulator:latest
```



Official command (the read/write operations failed, the endpoints are unreachable)

```
$parameters = @(
    "--publish", "8081:8081"
    "--publish", "10250:10250"
    "--env", "AZURE_COSMOS_EMULATOR_ENABLE_MONGODB_ENDPOINT=4.0"
    "--name", "windows-emulator"
    "--detach"
)
docker run @parameters mcr.microsoft.com/cosmosdb/linux/azure-cosmos-emulator:mongodb
```



Data explorer url:

[Azure Cosmos DB Emulator](https://localhost:8081/_explorer/index.html)
