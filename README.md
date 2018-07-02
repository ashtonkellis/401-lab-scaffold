# 401-Lab-Scaffolding Steps 
### Last Update: Monday July 1 @ 9:30 AM

## CD into your repo, then copy-paste this block of code into your terminal and the magic will happen
```
mv README.md LAB.md

mkdir src 
mkdir src/__test__ 
mkdir src/__test__/lib
mkdir src/lib

touch src/main.js 

npm init -y

curl -o README.md https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/readme-template.md
curl -o src/__test__/fake.test.js https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/fake-test.js
curl -o src/__test__/lib/test.env.js https://raw.githubusercontent.com/ashtonkellis/401-lab-scaffold/master/test.env.js
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
    "scripts": {
    "dev-start": "nodemon index.js",
    "test": "eslint . && jest --coverage",
    "testWatch": "jest --coverage --watchAll",
    "test-nolint": "jest --coverage --detectOpenHandles --forceExit --runInBand",
    "lint": "eslint .",
    "dbon": "mkdir -p ./db && mongod --dbpath ./db",
    "dboff": "killall mongod",
    "build": "babel src -d build",
    "start": "npm run build && node index.js"
  },
  "dependencies": {
    "bcrypt": "^2.0.1",
    "cors": "^2.8.4",
    "express": "^4.16.3",
    "http-errors": "^1.6.3",
    "jsonwebtoken": "^8.3.0",
    "mongoose": "^5.1.8"
  },
 "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-eslint": "^8.2.5",
    "babel-preset-env": "^1.7.0",
    "babel-preset-stage-2": "^6.24.1",
    "babel-register": "^6.26.0",
    "dotenv": "^6.0.0",
    "eslint": "^5.0.1",
    "eslint-config-airbnb-base": "^13.0.0",
    "eslint-plugin-import": "^2.13.0",
    "eslint-plugin-jest": "^21.17.0",
    "eslint-plugin-react": "^7.10.0",
    "faker": "^4.1.0",
    "jest": "^23.2.0",
    "nodemon": "^1.17.5",
    "superagent": "^3.8.3",
    "uuid": "^3.3.2",
    "winston": "^3.0.0"
  },
  "jest": {
    "setupFiles": [
      "<rootDir>/src/__test__/lib/test.env.js"
    ]
  }
```

Then run `npm i`
