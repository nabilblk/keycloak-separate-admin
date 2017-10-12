
* Command to execute Keycloak

```
docker-machine create keycloak-admin --driver=virtualbox
eval $(docker-machine env keycloak-admin)
docker run --name keycloak \
           -d -p 8080:8080 \
           -e KEYCLOAK_USER=admin \
           -e KEYCLOAK_PASSWORD=admin \
           -e KEYCLOAK_LOGLEVEL=DEBUG \
           -e PROXY_ADDRESS_FORWARDING=true \
           jboss/keycloak
open http://$(docker-machine ip keycloak-admin):8080/auth
```



* parameter of startup :

```
$WILDFLY_HOME/bin/standalone.sh -b=0.0.0.0 -bmanagement=0.0.0.0
```
