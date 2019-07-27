# Proyecto Microservicios Retail Services

## Compilacion
```bash
cd api-manager/
mvn clean package

cd order-service/
mvn clean package

cd product-service
mvn clean package

cd user-service
mvn clean package

```

Levantar BD
````
docker run --name postgresdb -p 5432:5432 -e POSTGRES_DB=unbound -e POSTGRES_PASSWORD=postgres123 -d postgres
```