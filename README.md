
* Command to execute Keycloak

```
docker-machine create keycloak-admin --driver=virtualbox
docker run --name keycloak -d -p 8080:8080 -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=admin jboss/keycloak
```
