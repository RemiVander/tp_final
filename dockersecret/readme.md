# Creation d'un secret :
echo "admin" | docker secret create ps_db_base

# Run docker-compose pour recup secrett :
docker stack deploy --compose-file .\docker-compose-tp-final.yaml test
## me demande pas comment et pk ca fonctionne, mais ca passe 