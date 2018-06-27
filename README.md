# 401-Lab-Scaffolding Steps 
### Last Update: Wednesday June 27 @ 9:45 AM

## CD into your repo, then copy-paste this block of code into your terminal and the magic will happen
```
mv README.md LAB.md

mkdir src 
mkdir src/__test__ 
mkdir src/__test__/lib
mkdir src/lib

touch src/main.js 

npm init -y

npm i -D babel-cli babel-eslint babel-preset-env babel-register dotenv eslint eslint-config-airbnb-base eslint-plugin-import eslint-plugin-jest eslint-plugin-react faker jest uuid nodemon superagent winston@next

npm i cors express http-errors mongoose

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

this part is not your terminal/bash. 
you have to open the package.json file and copy paste this JSON directly nested in the object
```
// add this snippet of json to add a pointer to the environment variables for testing
  "jest": {
    "setupFiles": [
      "<rootDir>/src/__test__/lib/test.env.js"
    ]
  },
```

this part is not your terminal/bash. 
you have to open the package.json file and copy paste this JSON into the scripts area. package.json scripts: 
```
// Scripts
    "dev-start": "nodemon index.js",
    "test": "eslint . && jest --coverage",
    "testWatch": "jest --coverage --watchAll",
    "test-nolint": "jest --coverage --detectOpenHandles --forceExit --runInBand",
    "lint": "eslint .",
    "dbon": "mkdir -p ./db && mongod --dbpath ./db",
    "dboff": "killall mongod",
    "build": "babel src -d build",
    "start": "npm run build && node index.js"
```
