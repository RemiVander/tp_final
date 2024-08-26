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


#### 3. Désactiver la réplication pour réduire la surface d'attaque et éviter des configurations non utilisées.
skip-slave-start


#### 4. Configuration d'utilisateurs

- création d'un utilisateur au rang d'amin pour ne pas utiliser l'utilisateur root.
- création d'un utilisateur avec les droits de CRUD pour ne pas donner tous les droits aux utilisateurs qui n'en auraient pas le besoin.

se connecter à mysql (cf ci-dessus)

CREATE ROLE 'admin_role';
CREATE ROLE 'agent_role';
GRANT ALL PRIVILEGES ON *.* TO 'admin_role' WITH GRANT OPTION;
GRANT SELECT, INSERT, UPDATE, DELETE ON *.* TO 'agent_role';
CREATE USER 'admin'@'%' IDENTIFIED BY 'password';
GRANT 'admin_role' TO 'admin'@'%';
CREATE USER 'agent'@'%' IDENTIFIED BY 'password';
GRANT 'agent_role' TO 'agent'@'%';
FLUSH PRIVILEGES;
EXIT;

