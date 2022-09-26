Mehdi Meguenani TP4

# Exercice 1. Commandes de base

### 1. Commencez par mettre à jour votre système avec les commandes vues dans le cours.
Afin de mettre a jour le système il faut effectuer 
```
apt update ; apt upgrade 
```

### 2. Créez un alias “maj” de la ou des commande(s) de la question précédente. Où faut-il enregistrer cet alias pour qu’il ne soit pas perdu au prochain redémarrage ?

Afin de créer un alias des commandes qui permettents de mettre a jour le système il faut effectuer la commande :
```
alias maj='sudo apt-get update && apt-get upgrade'
```

Pour que la commande soit enregistré il faut l'écrire dans le .bashrc

### 3. Utilisez le fichier /var/log/dpkg.log pour obtenir les 5 derniers paquets installés sur votre machine.

Pour obtenir les 5 derniers paquets installés sur la machine il faut effectuer la commande : 
```
 grep "installed" /var/log/dpkg.log | tail -n5
```

### 4. Listez les derniers paquets qui ont été installés explicitement avec la commande apt install
```
grep "apt install" /var/log/apt/history.log
```
