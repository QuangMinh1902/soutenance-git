## Soumettre une nouvelle fonctionnalité ou un bug fix

- Si vous trouvez un bug que vous souhaitez corriger ou une nouvelle fonctionnalité que vous souhaitez implémenter, veuillez soumettre un pull request via GitHub.

- S'il s'agit d'une fonctionnalité importante, créez d'abord [un issue](https://github.com/QuangMinh1902/soutenance-git/issues) afin qu'il puisse être discuté.

## Utiliser Git et GitHub

### Committing de vos modifications

```sh
git checkout my-new-feature      # To switch to your branch
git status                       # To see the new and changed files
git add FILENAME                 # To select FILENAME for the commit
git status                       # To verify the changes to be committed
git commit                       # To do the commit
git log                          # To verify the commit. Use q to quit the log
```

- Vous pouvez modifier le message ou les changements dans le dernier commit en utilisant :

```sh
git commit --amend
```

* Rebase votre branche au-dessus de la branche main pour obtenir les dernières modifications:

```sh
git checkout main
git rebase my-new-feature
```

* Revenir à un état précédent
```sh 
git log --oneline                         # To count the commits to squash, e.g. the last 2
git reset --hard HEAD~2          # To undo the 2 latest commits
git status                       # To check everything is as expected
```

* sinon, vous pouvez revenir en arrière en utilisant :

```sh 
git reflog                       # To check that HEAD{1} is your previous state
git reset --hard 'HEAD@{1}'      # To roll back to your previous state
```

### Workflow

#### Ce projet utilise gitflow pour norme codage :
- Vous installez gitflow extension: https://marketplace.visualstudio.com/items?itemName=vector-of-bool.gitflow
- Tapez "Ctrl+Shift+P" sur le clavier et cherchez gitflow 
- Il vous faut respecter les ordres de branches ici : http://danielkummer.github.io/git-flow-cheatsheet/#release
- Pour start/finish des feature branches, choisissez Gitflow:Feature:start - Gitflow:Feature:finish et faire pareil pour les autres branches