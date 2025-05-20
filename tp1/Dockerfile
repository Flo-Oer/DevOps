FROM postgres:17.2-alpine

ENV POSTGRES_DB=db \
   POSTGRES_USER=usr \
   POSTGRES_PASSWORD=pwd

COPY init-scripts/01-CreateScheme.sql /docker-entrypoint-initdb.d/
COPY init-scripts/02-InsertData.sql /docker-entrypoint-initdb.d/