# 1. leremsesh-content
Cette branche récupère les modifications faites sur le site Web de partage d'informations.

Les fichiers sont modifiés sur le *site Web de partage d'informations* puis transférés à la branche *proposition* automatiquement. Pour que les prpopositions soient visibles par tous, il faut faire une pull request de *proposition* vers *master*.

## 2. Liste des fichiers et dossiers qui ne doivent pas être pris en compte lors d'une « Pull request » :
* leremsesh/* ;
* README.md ;
* home.md.

## 3. Comment appliquer les modifications :
1. Faire une branche master-tmp qui a pour origine master.
2. Cloner le dépôt dans deux dossiers distincts.
3. Appeler l'un des dossiers clone_master-tmp (contient un clone de la branche master-tmp) et l'autre clone_proposition (contient un clone de la branche proposition).
4. Exécuter les commandes suivantes :
```
$ cd /emplacement/de/clone_master-tmp            # Accéder au dossier de la branche temporaire.
$ git checkout master-tmp                        # Passer ce dossier sur la branche master-tmp.
$ cd /emplacement/de/clone_proposition           # Accéder au dossier de la branche contenant les propositions.
$ git checkout proposition                       # Passer ce dossier sur la branche proposition.
$ rm -rf README.md home.md leremsesh             # Supprimer le contenu non souhaité pour une fusion (cf. : second chapitre)
$ cp -r * /emplacement/de/clone_master-tmp/.     # Copier tout le contenu restant vers la branche temporaire.
$ cd /emplacement/de/clone_master-tmp            # Accéder à la branche temporaire.
$ git add *                                      # Ajouter toutes les mises à jour au prochain commit.
$ git commit -m 'Fusion de <date_de_la_fusion>'  # Générer le commit.
$ git push origin master-tmp                     # Pousser la mise à jour (effectuer « git config -e », si nécessaire).
```
4. Faire une pull request depuis master-tmp.
5. Effectuer relectures + corrections rigoureuses avant de valider la pull request.
6. Une fois que la pull request est réussie, supprimer la branche master-tmp.
