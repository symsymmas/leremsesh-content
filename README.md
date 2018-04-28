# leremsesh-content
Cette branche récupère les modifications faites sur le site Web de partage d'informations.

Les fichiers sont modifiés sur le *site Web de partage d'informations* puis transférés à la branche *proposition* automatiquement. Pour que les prpopositions soient visibles par tous, il faut faire une pull request de *proposition* vers *master*.

## Liste des fichiers et dossiers qui ne doivent pas être pris en compte lors d'une « Pull request » :
* leremsesh/* ;
* README.md ;
* home.md.

## Comment appliquer les modifications :
1. Faire une branche master-tmp qui a pour origine master.
2. Cloner en local
3. Saisir les commandes suivantes :
```
  $ cd /emplacement/du/clone/en/local/
  $ git checkout master-tmp
  $ git merge --no-commit --no-ff origin/proposition
  $ git mergetool  # En cas de problème pour effectuer la fusion, il est possible d'utiliser l'outil graphique.
  $ git commit -m '<comment>'  # Mettre un commentaire explicite, par exemple : Ajout des information de PARTAGE.LEREMSESH datant du <date du commit>.
  $ git push origin master-tmp  # S'assurer que la configuration du clone git est en adéquation avec le dépôt Github.
```
4. Faire une pull request de master.
5. Une fois que la pull request est réussie, supprimer la branche master-tmp.
