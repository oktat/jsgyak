# JavaScript gyakorlatok

## NodeJS projekt struktúra

```txt
app01/
  |-.git/
  |-node_modules/
  |  `-bootstrap/
  |      `-dist/
  |         |-css/
  |         |  `-bootstrap.css
  |         `-js/
  |            `-bootstrap.js
  |-src/
  |  |-index.html
  |  `-style.css
  |-.gitignore
  |-package-lock.json
  |-package.json
  `-README.md
```

## NodeJS projekt létrehozása

```cmd
npm init -y
```

packages.json

```json
{
  "name": "kocsi_js",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

## Bootstrap telepítése

```cmd
npm install bootstrap
```

## Lite-Server kinfiguráció

bs-config.json:

```json
{
    "server": [
        "src",
        "node_modules/bootstrap/dist/css",
        "node_modules/bootstrap/dist/js"
    ]
}
```

## Lite-server telepítése

```cmd
npm install lite-server --save-dev
```

## Start script írása

```json
  "scripts": {
    "start": "lite-server"
  },
```

## A lite-server indítása

```cmd
npm start
```

## Git tároló

```cmd
git init
```

### A .gitignore

Készítsünk a projekt gyökérkönyvtárában egy .gitignore nevű fájlt a következő tartalommal:

```txt
node_modules/

```

### Git bemutatkozás

Szükség lehet a Git számára bemutatkozni:

```cmd
git config --global --unset user.name
git config --global --unset nagy@zold.lan
```

```cmd
git config --global user.name "Nagy János"
git config --global user.email nagy@zold.lan
```

### Állapot tárolása

```cmd
git status -u
git add --all
git commit --message "Kezdés"
```

### Feltöltés távoli szerverre

Állítsuk be hol van a távoli szerver:

```cmd
git remote add origin http://github.com/janos/reponev.git
```

Feltöltés:

```cmd
git push origin master
```
