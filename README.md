# testbot
repo pour botify

L'installation se fait avec Ansible.

# pre-requis
avoir mis la clé ssh pour l'utilisateur root sur la machine cible

# bug constatés
Il faut lancer 2 fois ansible pour le tout soit installé. La commande est la suivante: 
ansible-playbook -i hosts botify.yml
