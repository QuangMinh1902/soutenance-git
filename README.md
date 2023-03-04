## À propos du projet

Ce projet justifie les comptétence de Git de l'auteur et implique les notions principales :

- Commits signés par la clé GPG
- Créer des issues et issues templates
- Créer des pull request et pull request template
- Comprendre la syntaxe Markdown pour rédiger les fichiers Readme, Contributing, Issue Template et Pull Request Template
- Le fichier .gitignore
- Respecter le Gitflow
- Utiliser le hooks pour automatiser le formatage du code lors du commit
- Synchronisation nôtre dépôt sur Gitlab

### Les applications

- Trois petites apps qui utilisent HTML,CSS,JAVASCRIPT

<span> <img src="image/html.png" alt="css" width="100" height="100"> </span>
<span> <img src="image/css.png" alt="css" width="100" height="100"></span>
<span> <img src="image/js.png" alt="css" width="70" height="100"></span>

1. Digital Clock
2. New Year Countdown
3. Random Colors Generator

## Getting Started

### Configurer les packages git et npm

- Initialiser git and npm

```sh
 git init
 npm init -y 
```

- Et vous devez avoir la bibliothèque ESLint. Il existe une commande pratique pour configurer la configuration ESLint

```sh
npm init @eslint/config
```

- Ajouter npm script dans le fichier package.json

```sh
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "lint": "eslint index.js",
    "lint:fix": "eslint --fix colors.js clock.js countdown.js"
  },
```

- Ajouter les règles dans le fichier .eslintrc.js 
 ```sh 
  rules: {
    'no-param-reassign': 0,
    'no-plusplus': 'off',
  },
 ```

- Définir le hook de pré-commit

```sh
npx husky-init && npm install
```

- Ouvre le fichier .husky/pre-commit et change le contenu par :

```sh
#!/usr/bin/env sh
. "$(dirname -- "$0")/_/husky.sh"

npm run lint:fix
```

- Pour enregistrer le hooks, veuillez add et commit .husky/pre-commit

```sh
git add .husky/pre-commit && git commit -m "Add husky pre-commit"
```

- Reference:
  - [ESLint](https://www.npmjs.com/package/eslint)
  - [Husky](https://typicode.github.io/husky/#/)

### Installation

- Installez Git et définissez votre nom et votre adresse e-mail.
- Ouvrez votre terminal, changez de répertoire pour votre dossier préféré et initialisez votre projet local :

```sh
git clone https://github.com/quangminh-esgi/soutenance-git.git
cd soutenance-git
  # if you have SSH keys setup in your GitHub account:
git remote add origin git@github.com:quangminh-esgi/soutenance-git.git
```

## Contact

* Mon Email : quangminh1575@gmail.com
* Lien du projets : https://github.com/QuangMinh1902

## Remerciements

* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [CSS Reference](https://cssreference.io/)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [Git Hooks](https://dev.to/koich1/how-to-automate-format-your-code-on-commit-acn)
* [Git Flow](http://danielkummer.github.io/git-flow-cheatsheet/#release)
* [Gitflow extension](https://marketplace.visualstudio.com/items?itemName=vector-of-bool.gitflow)