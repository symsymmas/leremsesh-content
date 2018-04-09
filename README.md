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
  $ git checkout master-tmp
  $ git merge --no-commit --no-ff origin/proposition
  $ git reset -- <fileORfolder>  # À appliquer à chaque fichiers et dossiers précédemment cités
  $ git commit -m '<comment>'
  $ git push origin master-tmp  # S'assurer que la configuration du clone git est en adéquation avec le dépôt Github.
```
4. Faire une pull request de master.
5. Une fois que la pull request est réussie, supprimer la branche master-tmp.
