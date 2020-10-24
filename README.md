# Secure spring boot REST api with KeyCloak

## Prepare auth server

Start KeyCloak server as Docker container:

	docker container run -d --name auth -p 8080:8080 jboss/keycloak:latest

Add admin account to KeyCloak:

	docker container exec <CONTAINER> /opt/jboss/keycloak/bin/add-user-keycloak.sh -u <USERNAME> -p <PASSWORD>

Restart container:

	docker container restart auth
