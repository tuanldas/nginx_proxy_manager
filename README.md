# Chuẩn bị môi trường

```
cp .env.example .env
cp compose-prod.yml compose.override.yml
```

# Tạo các volume

```
docker volume create ${VOLUME_NPM_DATA}
docker volume create ${VOLUME_LETSENCRYPT_DATA}
docker volume create ${VOLUME_DB_DATA}
```

# Tạo network

```
docker network create ${CLOUD_NETWORK}
```

# Bật docker container

```
docker compose up -d
```
