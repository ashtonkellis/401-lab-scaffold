# 401-Lab-Scaffolding Steps
## copy paste this block of code into bash and the magic will happen

```
mv README.md LAB.md

mkdir src 
mkdir src/__test__ 
mkdir src/lib

touch src/main.js 

npm init -y

npm i -D babel-eslint babel-preset-env babel-register dotenv eslint eslint-config-airbnb-base eslint-plugin-import eslint-plugin-jest eslint-plugin-react jest uuid nodemon superagent

curl -o README.md https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/readme-template.md
curl -o src/__test__/fake.test.js https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/fake-test.js
curl -o src/lib/fake.js https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/fake.js

curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.babelrc 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.env 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.eslintignore 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.eslintrc.json 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.gitignore 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.travis.yml 
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/index.js

code .

```

// this part is not your terminal/bash. you have to open the package.json file and copy paste this JSON into the scripts area. package.json scripts:
```
    "lint": "eslint **/.js",
    "testWatch": "jest --coverage --watchAll",
    "test": "eslint . && jest --coverage",
    "test-nolint": "jest --coverage",
    "dev-start": "node index.js",
    "start": "node index.js"
```
