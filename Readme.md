## Trouble installation

sudo sysctl -w vm.max_map_count=262144


## Lancer les containers docker

docker-compose up -d

## Accéder au server sonar

http://localhost:9000/projects [admin/admin]

## Lancer le scanner

docker container inspect sonar-001_sonarqube_1 pour obtenir l'adresse ip

docker run \
--rm \
-e SONAR_HOST_URL="http://172.18.2.153:9000" \
-e SONAR_LOGIN="3e81797cd391f36acef8cf5493d0e154c921ea97" \
-v "/home/dtraore/meetups/app-001/app/sf_app:/usr/src" \
sonarsource/sonar-scanner-cli

