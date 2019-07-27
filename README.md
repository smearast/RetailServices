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
##  Levantar BD
```
docker run --name postgresdb -p 5432:5432 -e POSTGRES_DB=unbound -e POSTGRES_PASSWORD=postgres123 -d postgres
```

## Liquibase
```
cd liquibase/
liquibase --changeLogFile="changesets/db.changelog-master.xml" update
```
## Verificar instalacion

```
http://localhost:8000/
```

## Verificar Servicios

```
Desde Api Manager
http://localhost:8000/api/orders/order/test
http://localhost:8000/api/products/product/test
http://localhost:8000/api/users/user/test

Directo a los servicios
http://localhost:8200/order/test
http://localhost:8300/product/test
http://localhost:8100/user/test
```