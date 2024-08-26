### se connecter au conteneur
docker exec -it romantic_visvesvaraya bash

### Se connecter à mysql
mysql -u root -p 

password:admin


#### 2. Chiffrement en transit (mysql)
- copier le fichier à modifier:

    docker cp romantic_visvesvaraya:/etc/mysql/my.cnf 

- Dans le fichier my.cnf, on ajoute la configuration pour les certificats ssl

ssl-ca = /path/ca-cert.pem
ssl-cert = /path/server-cert.pem
ssl-key = /path/server-key.pem

-  copier le fichier modifié dans le container

docker cp my.cnf romantic_visvesvaraya:/etc/mysql/my.cnf

- redémarrer le container
docker restart romantic_visvesvaraya


#### 3. Désactiver les fonctionnalités non utilisées

- Désactiver la réplication, on ajoute dans le fichier conf
skip-slave-start
