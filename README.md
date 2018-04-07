# Boilerplate using NextJS & React-Fiber

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

append following snippet inside *scripts*  of package.json file

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

