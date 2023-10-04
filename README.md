# Exercice un (04/10/2023) 

## Les étapes exécuter : 


- [x] Prendre mon image Ubuntu => docker pull ubuntu
- [x] Créer un container à partir de mon image ubuntu => docker container -it run nomdeImage
      
   **Faire toutes les maj nécessaire** :
- [x] apt upgrade && apt update
- [x] apt install vim
- [x] apt install iputils-ping
- [x] apt install net-tools

- [x] Commit mon container pour creer une nouvelle image avec toute les maj => docker commit IDCONTAINER NOM_DE_MA_NOUVELLE IMG
- [x] Créer un network => docker network create NOM_DU_NETWORK
- [x] Créer un volume => docker volume create NOM_DU_VOLUME
- [x] Créer 3 container => docker container run -it vipingentu(NOM_DE_L'IMG) bash x3
- [x] Sortir du terminal du container => exit
- [x] Rename mes 3 container => docker container rename NOM_ACTUEL NOUVEAU_NOM x3
- [x] Start mes container => docker container start ID_DU_CONTAINER
- [x] Connecter mes 3 container dans mon network net1 => docker network connect net1(NOM_DU_NETWORK) (ID_CONTAINER) x3
- [x] Rentrer à nouveau dans l'un des container => docker exect -it ID_CONTAINER bash
- [x] => ifconfig pour affficher l'IP de mon container, dans mon cas IP : 172.20.0.2 (voir photo)
- [x] => Sortir du terminale avec "exit"
- [x] => entrer dans un autre container  => docker exect -it ID_CONTAINER bash => ping adresse IP de mon container c1
- [x] => Arreter le ping avec "ctrl + c"
- [x] => Resultat voir photo


![Capture d’écran 2023-10-04 114308](https://github.com/AnthoLC77/Docker_xp/assets/84148016/289bc593-fa2b-45df-8be9-65747302e592)


![Capture d’écran 2023-10-04 114650](https://github.com/AnthoLC77/Docker_xp/assets/84148016/4b205f3c-f72d-4c85-8bc2-4065732806d2)


![Capture d’écran 2023-10-04 114714](https://github.com/AnthoLC77/Docker_xp/assets/84148016/3827227f-9f26-4601-adf8-47e86f936c53)


# Exercice deux (04/10/2023) 

## Les étapes exécuter : 

### AVEC VIM INSTALLER : 

- [x] Creer un container à partir d'UBUNTU => docker container run -it ubuntu:latest


**Faire les maj suivante** :
- [x] apt update && apt upgrade
- [x] apt install -y vim

- [x] Creer le ficher script.sh => touch chemin/du/fichier/script.sh
- [x] Ecrire dans le fichier script.sh => apt install iputils-ping          //    apt install net-tools
- [x] Executer le ficher => bash /chemin/du/fichier/script.sh

### SANS VIM INSTALLER : 

- [x] Creer un container à partir d'UBUNTU => docker container run -it ubuntu:latest
- [x] Ce mettre dans bash/windows avec le bon chemin puis creer le fichier script => touch script.sh
- [x] Ecrire dans le fichier.sh => echo "ce qu'on veut ecrire " >> chemin/vers/le/fichier
- [x] Copier un ficher local windows au container qu'on souhaite mettre à jour => docker cp script.sh container_id:/script.sh
- [x] Rentrer dans le container => docker exec -it ID_CONTAINER bash
- [x] Executer le ficher => bash /chemin/du/fichier/script.sh
