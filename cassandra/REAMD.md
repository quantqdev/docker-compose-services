```bash
docker exec -it cassandra-1 cqlsh
docker exec -it cassandra-1 bash
docker logs cassandra-1
```

```cql
create keyspace mykeyspace with replication={'class':'SimpleStrategy', 'replication_factor':1} and durable_writes=true;
```