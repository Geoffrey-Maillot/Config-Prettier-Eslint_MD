# Config-Prettier-Eslint_MD

##Installer en global ou en devDependencies:

- prettier
- eslint
- npm install -g install-peerdeps
- install-peerdeps -g eslint-config-airbnb
- npm install -g eslint-config-prettier eslint-plugin-prettier
- Extention VsCode:.
  - Prettier - Code formatter
  - ESLint
  - Prettier ESLint



## Fichier settings.json

*Fichier crée automatiquement quand le paramètres FormatOnSave est cliqué, rajouté ces lignes de configuration*

```jsvascript
{
  "liveServer.settings.port": 5501,
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave":false
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  }
}
```

##Fichier .eslintrc.json

*Modifié au besoin sauf toute les lignes ou il y a prettier*

```javascript
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es2021": true
    },
    "extends": ["airbnb","airbnb/hooks", "prettier"],
    "plugins": ["prettier"],
    "parserOptions": {
        "ecmaVersion": 12
    },
    "rules": {
        "prettier/prettier": "error"
    }
}
```

##Fichier .prettierrc
*Modifier au besoin*

```javascript
{
  "semi": true,
  "tabWidth": 2,
  "singleQuote": true
}
```



