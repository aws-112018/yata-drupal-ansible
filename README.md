# Exercice Ansible : Inclusions, imports et rôles

## Consignes

Sur base du livre de jeu proposé et du document [Inclusions, imports et rôles](https://ansible.goffinet.org/ansible-linux/14-includes-imports-roles-ansible.html), veuillez :

1. mettre en place l'environnement en machine virtuelle avec les scripts [virt-scripts](https://github.com/goffinet/virt-scripts) actualisés (voir démarrage rapide)
2. soumettre dans une branche `dev-test-votre_nom` un livre de jeu qui réalise les tests adéquats de la disponibilté de l'application 
    * adresse ip récupérée comme en tant que fact
3. organiser le livre de jeu différents fichiers de tâches logiques appelés par des `include_tasks` ou des `import_tasks` dans une branche "dev-import-votre_nom"
    * documenter en français votre proposition dans la suite du fichier `README.md`
    * soumettre votre travail dans cette branche
4. organiser le livre de jeu en rôles réutilisables avec les directive `import_playbook`, `roles`, `include_role`/`tasks_from` dans une branche "dev-role-votre_nom"
    * documenter en français votre proposition dans la suite du fichier `README.md`
    * soumettre votre travail dans cette branche
5. faire évoluer votre livre de jeu en ajoutant le support du nom de domaine, de TLS, des mots de passe aléloire, de la sécurisation de mysql
    * soumettre votre travail dans cette branche
6. faire évoluer votre livre de jeu pour qu'il soit fonctionnel sur un hébergement "Centos 7"
    * soumettre votre travail dans cette branche

Remarques : idempotence, gestion des erreurs, ansible-lint

## Exercice 1

Veuillez mettre en place l'environnement en machine virtuelle avec les scripts [virt-scripts](https://github.com/goffinet/virt-scripts) actualisés.

```
git clone https://github.com/goffinet/virt-scripts
cd virt-scripts
less README.md
sudo ./define-guest-images.sh drupal01
```

## Exercice 2

Veuillez soumettre dans une branche `dev-test-votre_nom` un livre de jeu qui réalise les tests adéquats de la disponibilté de l'application

* adresse ip récupérée comme en tant que fact
* test HTTP 200 OK
* trouver l'occurence 'Powered by Drupal'
* Tester l'interface de connexion (option)
 
## Simple Drupal Development VM

**For a fully-featured VM environment for Drupal, please check out [Drupal VM](http://www.drupalvm.com/).**

This project makes local Drupal test/development environment management quick and easy. It installs the following on an Ubuntu 16.04 linux VM:

  - Apache
  - PHP
  - MySQL
  - Drush
  - Drupal

## About the Author

This project was created by [Jeff Geerling](https://www.jeffgeerling.com/) as an example for [Ansible for DevOps](https://www.ansiblefordevops.com/).
