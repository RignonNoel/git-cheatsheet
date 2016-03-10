# Rappel Git
[![PDF Status](https://www.sharelatex.com/github/repos/MaisonLogicielLibre/git-cheatsheet/builds/latest/badge.svg)](https://www.sharelatex.com/github/repos/MaisonLogicielLibre/git-cheatsheet/builds/latest/output.pdf)

## Configuration initial

```$ git config --global user.name "[name]"```

Configure le nom d’utilisateur associer au futur commits.

```$ git config --global user.email "[email]"```

Configure le courriel associer au futur commits.

## Créer un nouveau dépôt (repository).

```$ git init [project-name]```

Crée un nouveau dépôt (repository) en local.

```$ git clone [url]```

Télécharge un dépôt (repository) et tout son historique de version.

## Gestion des fichiers

```$ git rm [file]```

Supprime le fichier et notifie la suppression pour le prochain commit.

```$ git rm --cached [file]```

Supprime le fichier de la liste des fichiers suivis par git, mais ne touche pas au fichier local.

```$ git mv [file-original] [file-renamed]```

Renomme le fichier et notifie le changement pour le prochain commit.

## Supprimer/Restaurer temporairement des changements

```$ git stash```

Cache temporairement tous les changements non commités dans un paquet.

```$ git stash pop```

Restaure le dernier paquet de changement caché.

```$ git stash list```

Liste tous les paquets de changement caché.

```$ git stash drop```

Supprime le dernier paquet de changement caché.


## Effectuer des changements

```$ git status```

Liste tous les nouveaux fichiers et tous les fichiers ayant subi un changement qui vont être présents dans la nouvelle version.

```$ git add [file]```

Ajoute les changements actuels du fichier à la liste des changements devant être dans la nouvelle version.

```$ git reset [file]```

Enlève le fichier de la liste des changements devant être dans la nouvelle version.

```$ git commit -m"[descriptive message]"```

Sauvegarde la nouvelle version de manière permanente dans le gestionnaire de version.

## Les branches

```$ git branch```

Liste toutes les branches présentes localement sur le dépôt (repository)

```$ git branch [branch-name]```

Crée une nouvelle branche

```$ git checkout [branch-name]```

Déplace l'utilisateur vers la branche spécifiée et mets à jour les fichiers présents dans le dépôt.

```$ git merge [branch-name]```

Combine la branche spéifiée avec la branche courante.

```$ git branch -d [branch-name]```

Supprime la branche spécifiée.

## Analyser l'historique de version

```$ git log```

Liste tout les commits de la branche courante.

```$ git log --follow [file]```

Liste tous les commits relatifs au fichier, incluant les changements de nom.

```$ git diff [first-branch]...[second-branch]```

Montre les différences de contenu entre deux branches.

```$ git show [commit]```

Montre le détail du commit spécifié (changement, nom, heure, auteur, ..).

## Modifier des commits

```$ git reset [commit]```

Annule tous les commits effectués après le commit spécifié, cela préserve donc les changements.

```$ git reset --hard [commit]```

Supprime tous les commits effectués après le commit spécifié, les changements sont donc supprimés

## Synchroniser les changements

```$ git fetch [remote]```

Synchronise en local l'historique du dépôt (repository) distant.

```$ git merge [remote]/[branch]```

Combine la branche distante avec la branche locale.

```$ git push [remote] [branch]```

Téléverse tous les commits de la branche locale sur le dépôt (repository) distant.

```$ git pull [remote] [branch]```

Télécharge tout les nouveaux changements présent sur le dépôt et les applique en local.
