# MSSQL DOCKER

```
version: "3.1"
services:
  dbmssql:
    image: "mcr.microsoft.com/mssql/server"
    ports:
      - "3000:1433"
    environment:
      - ACCEPT_EULA=Y
      - SA_PASSWORD=ETxGkUcEZM7M22tP5
      - MSSQL_DB=api-template
      - MSSQL_USER=me
      - MSSQL_PASSWORD=ETxGkUcEZM7M22tP5
    volumes:
      - "./drive:/var/opt/mssql/data"
    restart: always
    container_name: mssql
    build: ./database
volumes:
  db_data: {}
```