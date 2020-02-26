# testbot
repo pour botify

L'installation se fait avec Ansible (que j'ai appris sur le tas).


# pre-requis
avoir mis la clé ssh pour l'utilisateur root sur la machine cible

# bug constatés
Il faut lancer 2 fois ansible pour le tout soit installé. La commande est la suivante: 
ansible-playbook -i hosts botify.yml

Le service ecoute sur le port 5000. Il n'est pas possible de changer ce port

# amélioration  1
On peut installer un service Web (apache ou nginx) et definir un proxy qui requete le port 5000 et qui ecoute en http/https. 
Pour le https il faut definir l'URL (nom de machine et domaine ) afin de creer les certificats
# amélioration 2
La definition du service peut être améliorée
creer un user flaskr pour faire tourner les services améliorera la sécurité
# amélioration 3
La sauvegarde de l'application pourra se faire dans un repertoire /Backup monté sur un disque iscsi Distant
# amélioration 4
pour minimiser l'impact lors du deploiement un simple 'at' pourra être utiliser
# amélioration 5
une machine load balancer pourra être mis en front de plusieurs serveur. Dans ce cas le HTTPS pourra être installé sur le load balancer le http pourra être rétablit sur les autres machines.  
