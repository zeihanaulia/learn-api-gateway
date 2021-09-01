# Build & Running Service

Running script on root projects

## Docker Compose

```cmd
docker-compose up
```

## Build Accounts Service

```cmd
docker build -t lag-accounts-service -f ./deployments/Dockerfile.accounts .
docker tag lag-accounts-service zeihanaulia/lag-accounts-service:1.0.0
```

## Build Catalogs Service

```cmd
docker build -t lag-catalogs-service -f ./deployments/Dockerfile.catalogs .
docker tag lag-catalogs-service zeihanaulia/lag-catalogs-service:1.0.0
```

## Build Orders Service

```cmd
docker build -t lag-orders-service -f ./deployments/Dockerfile.orders .
docker tag lag-orders-service zeihanaulia/lag-orders-service:1.0.0
```
