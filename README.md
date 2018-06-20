# 401-Lab-Scaffolding Steps

rename the lab README.md file (contains lab instructions) to LAB.md
```
mv READMD.md LAB.md
```

make new directories
```
mkdir src src/__test__ src/lib
```

make new files (main.js and a new README which you will fill out to describe your code)
```
touch src/main.js READMD.md
```

makes a .js file with a single function
```
curl -o src/__test__/fake.test.js https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/fake-test.js
```

makes a .test.js file to test this simple fuction. This allows for travis.CI integration (because tests are passing)
```
curl -o src/lib/fake.js https://raw.githubusercontent.com/ashtonkellis/401-Lab-Scaffolding/master/fake.js
```

copy a ton of necessary files from the lab scaffolding template
```
curl -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.babelrc -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.env -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.eslintignore -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.eslintrc.json -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.gitignore -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/.travis.yml -O https://raw.githubusercontent.com/codefellows/seattle-javascript-401d25/master/00-lab-scaffold-template/index.js
```

initialize node
```
npm init -y
```

install all node dependencies for your project
```
npm i -D babel-eslint babel-preset-env babel-register dotenv eslint eslint-config-airbnb-base eslint-plugin-import eslint-plugin-jest eslint-plugin-react jest uuid nodemon superagent
```

copy paste in the node scripts. this part is not your terminal/bash. you have to open the package.json file and copy paste this JSON into the scripts area. package.json scripts:
```
    "lint": "eslint **/.js",
    "testWatch": "jest --coverage --watchAll",
    "test": "eslint . && jest --coverage",
    "test-nolint": "jest --coverage",
    "dev-start": "node index.js",
    "start": "node index.js"
```
