# Git Cheat Sheet Complète

## Configuration Initiale
```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre@email.com"
git config --global color.ui true
git config --list                           # Voir la configuration
```

## Création et Clonage
```bash
git init                                    # Initialiser un nouveau dépôt
git clone <url>                            # Cloner un dépôt distant
git clone --depth 1 <url>                  # Cloner avec historique limité
git clone --branch <branche> <url>         # Cloner une branche spécifique
```

## Commandes Basiques
```bash
git status                                 # État du dépôt
git add <fichier>                         # Ajouter un fichier
git add .                                 # Ajouter tous les fichiers
git add -p                                # Ajouter interactivement
git commit -m "message"                   # Créer un commit
git commit --amend                        # Modifier le dernier commit
```

## Branches
```bash
git branch                                # Lister les branches
git branch <nom>                          # Créer une branche
git checkout <branche>                    # Changer de branche
git switch <branche>                      # Changer de branche (nouveau)
git checkout -b <branche>                 # Créer et changer de branche
git branch -d <branche>                   # Supprimer une branche
git branch -D <branche>                   # Forcer la suppression
git branch -m <nouveau-nom>               # Renommer la branche courante
```

## Remote (Dépôt Distant)
```bash
git remote -v                             # Voir les dépôts distants
git remote add <nom> <url>                # Ajouter un dépôt distant
git remote remove <nom>                   # Supprimer un dépôt distant
git fetch <remote>                        # Récupérer sans fusionner
git pull                                  # Récupérer et fusionner
git push <remote> <branche>               # Pousser les changements
git push -u origin <branche>              # Pousser et définir l'upstream
```

## Fusion et Rebase
```bash
git merge <branche>                       # Fusionner une branche
git merge --abort                         # Annuler une fusion
git rebase <branche>                      # Rebase sur une branche
git rebase -i HEAD~<n>                    # Rebase interactif
git cherry-pick <commit>                  # Appliquer un commit spécifique
```

## Historique et Différences
```bash
git log                                   # Voir l'historique
git log --oneline                         # Format condensé
git log --graph                           # Affichage graphique
git diff                                  # Voir les modifications
git diff --staged                         # Diff des fichiers stagés
git blame <fichier>                       # Voir qui a modifié quoi
```

## Annulation et Restauration
```bash
git restore <fichier>                     # Restaurer un fichier
git restore --staged <fichier>            # Désindexer un fichier
git reset HEAD~1                          # Annuler le dernier commit
git reset --hard HEAD~1                   # Annuler et supprimer les changements
git revert <commit>                       # Créer un commit d'annulation
```

## Stash (Remisage)
```bash
git stash                                 # Remiser les modifications
git stash save "message"                  # Remiser avec description
git stash list                           # Lister les remises
git stash pop                            # Appliquer et supprimer la dernière remise
git stash apply                          # Appliquer sans supprimer
git stash drop                           # Supprimer la dernière remise
```

## Tags (Étiquettes)
```bash
git tag                                  # Lister les tags
git tag -a v1.0 -m "Version 1.0"        # Créer un tag annoté
git tag v1.0                            # Créer un tag léger
git push origin v1.0                    # Pousser un tag
git push origin --tags                  # Pousser tous les tags
```

## Maintenance
```bash
git gc                                   # Nettoyer le dépôt
git prune                               # Supprimer les objets orphelins
git fsck                                # Vérifier l'intégrité
git reflog                             # Voir l'historique des références
```

## Configurations Avancées
```bash
git config --global alias.<raccourci> <commande>  # Créer un alias
git config --global core.editor "code --wait"     # Définir l'éditeur
git config --global merge.tool vimdiff            # Définir l'outil de fusion
git config --global pull.rebase true             # Rebase par défaut au pull
```

## Sous-modules
```bash
git submodule add <url>                 # Ajouter un sous-module
git submodule init                      # Initialiser les sous-modules
git submodule update                    # Mettre à jour les sous-modules
git submodule update --recursive        # Mise à jour récursive
```

## Recherche
```bash
git grep "texte"                        # Rechercher dans les fichiers
git log -S "texte"                      # Rechercher dans l'historique
git log --grep="motif"                  # Rechercher dans les messages de commit
```
