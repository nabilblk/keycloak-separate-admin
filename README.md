
* Command to execute Keycloak

```
docker-machine create keycloak-admin --driver=virtualbox
eval $(docker-machine env keycloak-admin)
docker run --name keycloak \
           -d -p 8080:8080 \
           -e KEYCLOAK_USER=admin \
           -e KEYCLOAK_PASSWORD=admin \
           jboss/keycloak
```
