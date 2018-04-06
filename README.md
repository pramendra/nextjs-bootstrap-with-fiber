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