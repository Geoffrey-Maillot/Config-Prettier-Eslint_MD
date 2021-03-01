# Config-Prettier-Eslint_MD

## Installer les extentions VSCode

  - Prettier - Code formatter
  - ESLint
  - Prettier ESLint


## Installer les modules en devdependencies et les configurer


```javascript
- npm init
- npm install -D prettier eslint
- ./node_modules/eslint/bin/eslint.js --init
- npm install -D eslint-config-prettier eslint-plugin-prettier
```


## Modifier settings VSCode et fichier settings.json

- Dans les settings, cocher la case "FormatOnSave" et activer la sauvegarde auto à "OnFocusChange"
- Un fichier settings.json est créer, copier/coller la config ci-dessous:



```jsvascript
{
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave":false
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  "files.autoSave": "onFocusChange"
}
```

##Fichier .eslintrc.json

*Rajouter ces lignes dans le fichier .eslintrc.json:"

```javascript
{
"extends": ["prettier"]
"plugins": ["prettier"]
"rules": {
"prettier/prettier": "error"
}
}
```

### Exemple

```javascript
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es2021": true
    },
    "extends": [
        "airbnb-base",
         "prettier"
    ],
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



