## Setup NextJS and React

```
mkdir nextjs-bootstrap-with-fibe
yarn init -y
cd nextjs-bootstrap-with-fibe
```

```
curl https://raw.githubusercontent.com/github/gitignore/master/Node.gitignore -o .gitignore
git add .gitignore
git commit -m "Add .gitignore"
```

```
yarn add next react react-dom
```

append following snippet inside _scripts_ of package.json file

```
    "dev": "next",
    "build": "next build",
    "start": "next start"
```

```
git add .
git commit -m "init with nextJs and React"
```

### Setup eslint

```
yarn add -D babel-eslint eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react
touch .eslintrc
touch .eslintignore
```

#### add following snippet inside .eslintrc

```
{
  "parser": "babel-eslint",
  "extends": "airbnb",
  "globals": {
    "document": true,
    "window": true,
    "process": true
  },
  "rules": {
    "import/extensions": 0,
    "import/no-extraneous-dependencies": 0,
    "import/no-unresolved": 0,
    "react/jsx-filename-extension": 0,
    "linebreak-style": 0
  }
}
```

#### add following snippet inside .eslintignore

```
build/*
test_server/*
```

### Setup prettier

```
  yarn add -D prettier eslint-config-prettier eslint-plugin-prettier
```

#### append followng snippet inside .eslintrc

```
 "extends": ["airbnb", "prettier", "prettier/react"],
  "plugins": ["prettier"],
  "env": {
    "browser": true,
    "es6": true
  },
```

#### add followng snippet inside .prettierrc

```
{
  "printWidth": 80,
  "singleQuote": true,
  "trailingComma": "all"
}
```

### add .editorconfig

```
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false
```

### add following inside .vscode/settings.json for vscode config

```
{
  "eslint.enable": true,
  "editor.formatOnSave": true
}
```

### add following snippet inside package.json to support eslit and prettier cli

```
"format": "prettier --write '**/*.{js,jsx}'",
"lint": "eslint '**/*.{js,jsx}' --quiet",
```

### add babel and flow support

```
yarn add -D babel-cli babel-preset-flow flow-bin flow-typed babel-plugin-transform-flow-strip-types
```

### add following snippet to .babelrc

```
{
  "presets": ["next/babel", "flow"],
  "plugins": ["transform-flow-strip-types"]
}
```

### add following snippet to .flowconfig

```
[ignore]
.*/node_modules/.*/\(lib\|test\).*\.json$

[include]

[libs]

[options]
esproposal.class_static_fields=enable
esproposal.class_instance_fields=enable
```

#### append inside scripts in package.json

```
"flow": "flow check",
```

### add following snippet inside pages/index.js to create a sample page

```
import React from 'react';

export default () => <h1>Hello World</h1>;
```

#### run add

```
yarn dev
```

### add following snippet in .nvmrc

```
v9.4.0
```

### add support browsers list support

#### add following snippet inside .browserslistrc

```
{
  "browserslist": [
    "> 1%",
    "last 2 versions"
  ]
}
```

#### add following package

```
yarn add -D @babel/preset-env
```

#### update following snippet to support browers list

```
{
  "presets": ["env", "next/babel", "flow"],
  "plugins": ["transform-flow-strip-types"]
}
```

### move nextjs insdide src

#### update scripts inside package.json

```
"dev": "next src",
"build": "next build src",
"start": "next start src"
```
