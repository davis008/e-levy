# e-levy
e-levy app for levy enforcers and levy compliance officers
##TOOLING
### install prettier for code formating
```npm install -D prettier```
enable it in visual studio code extensions too
You can add ```"format": "prettier --write \"src/**/*.{js,jsx}\"",``` in yours scripts section of package.json file and run the command ```yarn format``` to format
 set ```prettier.requireConfig``` to true and ```editor.formatOnSave``` to true.
 
 add ``.prettierrc``` file and add `{}` to the file
### install eslint for linting
```npm install -D eslint eslint-config-prettier```
enable it in visual studio code extensions too
Create this file called ```.eslintrc.json.``` and add:
```
{
  "extends": ["eslint:recommended", "prettier", "prettier/react"],
  "plugins": [],
  "parserOptions": {
    "ecmaVersion": 2018,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  }
}
```
for eslint and prettier configurations
then add it to package.json scripts ```"lint": "eslint \"src/**/*.{js,jsx}\" --quiet",```

###parcel

we are going to use parcel bundler for this app
 do: ```npm install -D parcel-bundler```
 
 inside scripts in package.json add ```"dev": "parcel src/index.html"```

add the following to ```.gitignore```

```node_modules
.cache/
dist/
.env
.DS_Store
coverage/
.vscode/```

