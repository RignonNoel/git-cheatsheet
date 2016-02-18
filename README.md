# Rappel Git

## Bases


## Configuration de Git

```$ git config --global user.name "[name]"```

Saisisser le pseudo que vous voulez associer à tout vos commit

```$ git config --global user.email "[email]"```

Saisisser le courriel que vous voulez associer à tous vos commit

## Creer un nouveau dépôt

```$ git init [project-name]```

Creer un nouveau dépôt en local

```$ git clone [url]```

Télécharger un dépôt et tout son historique de version

## Gestion des fichiers

```$ git rm [file]```

Supprime le fichier et notifie la suppresion pour futur commit

```$ git rm --cached [file]```

Supprime le fichier de la liste des fichiers suivi par le gestionnaire de version mais ne touche pas au fichier local

```$ git mv [file-original] [file-renamed]```

Renomme le fichier et notifie le changement pour futur commit

## Sauvegarder des fragments

```$ git stash```

Cache temporairement tout les changements non commité dans un paquet

```$ git stash pop```

Restaure le dernier paquet de changement caché

```$ git stash list```

Liste tout les paquets de changement caché

```$ git stash drop```

Supprime le dernier paquet de changement caché


## Effectuer des changements

```$ git status```

Liste tous les nouveau fichier et tout le fichiers ayant subit un changement qui vont être présent dans la nouvelle version

```$ git add [file]```

Ajoute les changement actuel du fichier à la liste des changements devant être dans la nouvelle version

```$ git reset [file]```

Enlève le fichier de la liste des changement devant être dans la nouvelle version

```$ git commit -m"[descriptive message]"```

Sauvegarde la nouvelle version de maniére permanente dans le gestionnaire de version

## Les branches

```$ git branch```

Liste toutes les branches présente localement sur le dépôt

```$ git branch [branch-name]```

Crée une nouvelle branche

```$ git checkout [branch-name]```

Déplace vers la branche spécifié et met à jour les fichiers présent dans le dépôt

```$ git merge [branch-name]```

Combine la branche spéifié avec la branche courante

```$ git branch -d [branch-name]```

Supprime la branche spécifié

## Visionner l'historique

```$ git log```

Liste tout l'historique de version de la branche courante (donc tout les commits)

```$ git log --follow [file]```

Liste l'historique de version du fichier, incluant les changement de nom

```$ git diff [first-branch]...[second-branch]```

Montre les différences de contenu entre deux branches

```$ git show [commit]```

Montre les métadonnées et les changements contenu dans le commit spécifié

## Redo commits

```$ git reset [commit]```

Supprime tout les commits effectué après le commit spécifié, mais préserve les changements en local

```$ git reset --hard [commit]```

Supprime tout les changements et commits effectué après le commit spécifié

## Synchroniser les changements

```$ git fetch [remote]```

Télécharger tout l'historique du dépôt distant

```$ git merge [remote]/[branch]```

Combiner la branche distante dans la branche locale

```$ git push [remote] [branch]```

Téléverse tous les commits de la branche locale sur le serveur git

```$ git pull```

Télécharge tout les nouveaux changements présent sur le serveur git et les applique en local
