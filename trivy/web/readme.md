# Trivy

## Présentation 

Trivys a permis d'identifier un total de 884 CVEs liées a des packages installés sur la machine superutopios/ecommercefinal
Ces CVEs sont réparties sur 5 groupes : UNKNOWN, LOW, MEDIUM, HIGH, CRITICAL
La répartition de ces failles sur la machines :
    - UNKNOWN : 2
    - LOW :     302
    - MEDIUM :  509
    - HIGH :    66
    - CRITICAL: 5

[Voir le rapport complet Trivy](./bfore)

## Remédiations possiles 

Pour résoudre ces failles, il est possible de :
    - Identifier les packages non utilisés et les supprimer.
    - Mettre, si possible, à jour les versions des packages. 
    - Limiter l'utilisation de certains packages a des utilisateurs spécifiques.
    - Recommencer l'image docker depuis une version alpine et n'installer que les packages nécessaires.

Une premiere partie de la remediation a été faite, l'autre partie restante est laissée aux developpeurs, car il n'y a pas d'informations si certaines versions des packages sont nécessaires pour le bon fonctionnment de l'application, ou il y a eu des doute sur la nécessité de ceux ci.

[Voir le rapport complet Trivy](./after)

La présence de certains packages ont été marqué comme inutiles, comme les gcc, cpp, g++ par exemple.

La suppressions de ces packages a permis de passer de 884 CVEs a un total de 286. 
La nouvelle répartition est la suivante : 
    - UNKNOWN : 2
    - LOW :     200
    - MEDIUM :  66
    - HIGH :    17
    - CRITICAL: 2