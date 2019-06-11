---
description: Find below instructions to run eslint + prettier locally
---

# README

## Let's start

Acess

```
package.json
```

and copy all devDependencies. After on your terminal run

```
$ yarn
```

Also copy below script from

```
package.json
```

to yours

```
 "precommit": "pretty-quick --staged"
```

{% hint style="info" %}
you also can use npm
{% endhint %}

Once finish, create a `.eslintrc.json` file and copy whole from code inside .`eslintrc.json` on repo

if you lazy just find below respective above JSON

{% code-tabs %}
{% code-tabs-item title=".eslintrc.json" %}

```javascript

{
  "extends": ["react-app", "plugin:prettier/recommended"],
  "rules": {
    "no-unused-vars": "off"
  }
}


```

{% endcode-tabs-item %}
{% endcode-tabs %}

if you use vscode search for [**EditorConfig for VS Code**](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) \*\*\*\*create a file called `.editorconfig`

```text
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

```

We are almost finishing. Now open vscode JSON settings and paste code below

```text
  {
    "workbench.iconTheme": "material-icon-theme",
    "workbench.colorTheme": "Dracula",
    "editor.fontFamily": "Fira Code",
    "editor.fontLigatures": true,
    "editor.formatOnSave": true,
    "window.zoomLevel": -1,
    "workbench.colorCustomizations": {},
    "[javascript]": {
        "editor.formatOnSave": false
    },
    "eslint.autoFixOnSave": true,
    "eslint.alwaysShowStatus": true,
    "prettier.disableLanguages": [
        "js"
    ],
    "files.autoSave": "onFocusChange"
}
```

last step install Prettier plugin in your vscode [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and [Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

That's it! We finished eslint + prettier to run react and react native projects! But if you want it to node.js. well done, just copy below `.eslintrc.json`

```text
{
  "env": {
    "node": true
  },
  "rules": {
    "array-bracket-spacing": [2, "never"],
    "block-scoped-var": 2,
    "brace-style": [2, "1tbs"],
    "camelcase": 1,
    "computed-property-spacing": [2, "never"],
    "curly": 2,
    "eol-last": 2,
    "eqeqeq": [2, "smart"],
    "max-depth": [1, 3],
    "max-len": [1, 80],
    "max-statements": [1, 15],
    "new-cap": 1,
    "no-extend-native": 2,
    "no-mixed-spaces-and-tabs": 2,
    "no-trailing-spaces": 2,
    "no-unused-vars": 1,
    "no-use-before-define": [2, "nofunc"],
    "object-curly-spacing": [2, "never"],
    "quotes": [2, "single", "avoid-escape"],
    "semi": [2, "always"],
    "keyword-spacing": [2, {
      "before": true,
      "after": true
    }],
    "space-unary-ops": 2
  }
}

```
