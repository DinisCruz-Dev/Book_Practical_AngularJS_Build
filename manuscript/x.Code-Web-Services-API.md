### Code - Web Services - API

This is the node app which provides the web services consumed by the AngularJS front end (I'm not going to into much detail about this app, since this is a book about AngularJS not Node :) )

**/**

![](images/20291408-3479-11e6-82af-6d5ab8c9d85d.png)

**/data**

![](images/4d017fb0-3479-11e6-9143-1e04d2b536c9.png)

**/src**

![](images/3eb12c9e-3479-11e6-9816-e3a82dc3780d.png)

**/test**

![](images/602074a2-3479-11e6-814a-d7fce332debb.png)


**.travis.yml**

```yml
sudo: required
services:
  - docker

language: node_js

node_js:
  - "5"

git:
    submodules: false

env:
  global:
    - secure: "UnkjMMD5WA19zORlk1LECpO1GZfWvuM0WcVmougiuwlQhTPv697UMA1NEmTXNzMgF5DTEHNaBiIr9Q75woOzXnjJsTizsyUpwAQHP//s6ZTfuof3EUAQg3rX9tGj/KFHG3VuvDOlCnF6R1hc86jLTRL61DiWP/4+Q9Wn8JXeicPS2eI8ga+fVyTvgLtYZ//e+egyYK32dZyqvT0mlfFEpLBnMVmYzzi9SSHBu2otLLTvEray90V2afNamiqvb4Wwc9hGJF4fLZfMF8vuPqFztnA2imOdCtd1D3PZ6tNp3cXalqggn6aqkXwDoCZzmO3CHfLqIEqZuCeas0bwccApu5ZL14b/b618jwU9hoXhFHr+eZZxjoYqD0wRyJFH2fxbOWPzXJ05fpwY2s5Avflh7g1qhDmPsqc/O9SyplKqSvCeXdf+im/fesbZuzU1dDqX8ZXQFY4EK4ye+fORWzda/0Ltc0HMBVB44kz7wXbYlYT+10IqUZH7xidRVTAWRjpvUD1UzrJFr6N/WA2CQXUBr/VHbi23kVPoysZaZxZ2f9frfp0NNfUflMQhiKYiFuPf7D7j4DVLUX0QlUpmhTTGUsdodNpgTbvTszf7+vRHgLa4FbESn/ISbtOaFyIvqYTssezo8KAUrK50ABWKH0kt3VFydRQ61Qab5slVDl+NOBo="
    - secure: "F2TFYlVRGMb7u95e2wO8s1sG2ChZm/R3a2rxymXTcAif6m9ocpI6M7pWhgfLzR+ZHb9AOgCpbn0NcDHHSuBgYQjmwFV9BLcQ18/pKNIyP+Ei6kqJYMv5f7XAIm0/7DlpH28iHuyn5Fe/O027ItPg9fCDkqL2GjMn4dvmEYUAUmGkLmAWKZKz5lLNryLTDsB4ZaLWD+kUpVyYBixIk6cu02VMatc5v26tiRfVQsFvtpsETKGJPtoN+S1VEcB4/OBdodBXKtwAIOLw1x0DcIpTqD/UcTGyrS/P0H+47YuMnZ5d1l+KynCJiOy7OS12/5ViRbt9RAP2H2bit1s/FGZ2dvJAIXEgm9LRO3ewZaJWIQ90H0UywXU2NT42w6t+Brm15+3IxOJzJ1kFxSiule547NtCiookfY8Dypo3RPE33VI+z8W7ZjrgtU08pvzpZmrgHn3vsl8OCoDm4BRs/HUfWkxQAbr3jNVe8uSxsgDLDnAYN3/+luUnZkD7RAsHAiqi4EBFKlvaLYhsN+nD+V/cw5+DqEUyyF+7e3haK/AYzVP5z0r/5C5jqEp1dGGehJZJ1apyclFpMtDGmwt04GeSPldFTHgP2HSyNy2V1/pQMn+TcIHdajAticaXYWF3wSjt3TWxTD6bPxyiYNUTO/SQ780ddbt2hYKT271tNyPFyEQ="
    - secure: "eWiQ3SMI91oYuoHQpCeImDa+X29wbJJCk8LrRdhuKXNanW9eF8zfwBCmycxjSNFl4OcWzEs8EUBym1tj+hzQ41DEFV57svShB6Sw+R5zDwUwd1JigNvbtEZXLY6kURrKEqwMT3zyPi5ndGf6gl12hDByoa0HNBgYeDNs/MepogOmRVpUIlMBMZeq8IxQZOaG3DKP05zPHhSaM/jTt3EGkThUAElXvzpjFCr6z8JzKepxXKK2sctodrRQ8OwR4CPghUkDm9BvNixP06eM8tLsAThVlQg3Dt/fwtCteHhyN+axfBNJr36Sd6xg87g2DTK79L7KXRfKbMrH38gG5W8aCr4NOuer4U+2wHQ8KBJg/HyagdiS1x+Pih01TB9H8scepSx/TLqqtlu/VgFjC5lDclYZiKEkYfWIhDOPoVUq2N/8wCiuPHEDumS5xRcqlkK0+o+0J7Ell/g6GCB28wbJV2kme/AbwGFrlrLdE9SzszaAgFRNbHG6t1o/WuqPfRcyKbyM+L6NrCbGbmxNPwPgKyGYKUfaqdGMLABsc/EXvgKTkt/jUptyjNLPMw5JPYcJxw2frmok8O+IsL3qVcKhqW/6XUmR5LdoaLilNf7DpxkyTqwzC9TFfmc86v2TBuSz4CabkUYI5sIddbLJ1By7BpQrmjxijt/u1ksPYxYF0FY="


before_install:
    - cat .gitmodules
    - sed -i 's/git@github.com:/https:\/\/github.com\//' .gitmodules
    - cat .gitmodules
    - git submodule update --init --recursive

before_script:

  #- npm install -g bower
  #- bower install
  #- npm install -g gulp
  #- cd ui; gulp; cd ..
  - cd ui
  - npm install
  - npm install -g bower
  - npm install -g gulp
  - bower install
  - gulp
  - cd ..


script:
  - echo ">>>>> Running core tests<<<<<"
  - npm test
  - echo ">>>>> Running UI tests<<<<<"
  - cd ui
  - npm test
  - cd ..


after_success:

  - echo ">>>>> Updating Dev fork <<<<<"
  - git remote add upstream https://DinisCruz-Dev:$git_pwd@github.com/DinisCruz-Dev/Maturity-Models.git
  - git push -f upstream

  - echo ">>>>> Building DOCKER IMAGE and pushing it go Docker Hub <<<<<"
  - echo 'building docker image'
  - docker images
  - docker build -t diniscruz/maturity-models .
  - docker images
  - docker login -e $DOCKER_EMAIL -u $DOCKER_USER -p $DOCKER_PASS
  - docker push diniscruz/maturity-models

  - echo ">>>>> Cloning Maturity-Models-QA, adding extra commit and pushing it to Maturity-Models-Dev for  <<<<<"
  - cd ..
  - git clone https://github.com/DinisCruz/Maturity-Models-QA.git
  - cd Maturity-Models-QA
  - git remote add upstream https://DinisCruz-Dev:$git_pwd@github.com/DinisCruz-Dev/Maturity-Models-QA.git

  - git config --global user.email "bot@travis.com"
  - git config --global user.name "Travis Bot"

  - git log -n5 --pretty=oneline > travis-git-log.txt
  - git add .
  - git commit -m "Comming files for $(git rev-parse HEAD)"
  - git push -f upstream master
```

**Dockerfile**

```Dockerfile
FROM    node

RUN 	git clone https://github.com/DinisCruz/Maturity-Models.git
WORKDIR Maturity-Models
RUN     sed -i 's/git@github.com:/https:\/\/<user>:<token>@github.com\//' .gitmodules
RUN     git submodule init
RUN     git submodule update
RUN     git pull origin master
RUN     npm install --quiet

WORKDIR ui
RUN     npm install --quiet
RUN     npm install --quiet -g bower
RUN     npm install --quiet -g gulp
RUN     bower --allow-root install
RUN     gulp
WORKDIR ..

RUN     pwd
RUN     mkdir logs              # node app was failing to create this folder
RUN     ls -la

CMD     npm start


# travis builds image and deploys to docker hub at: diniscruz/maturity-models
# build manually using: docker build -t diniscruz/maturity-models .
```

**package.json**

```json
{
  "name": "maturity-models",
  "version": "0.0.1",
  "description": "Maturity Models",
  "main": "server.js",
  "scripts": {
    "test": "node ./node_modules/mocha/bin/mocha --compilers coffee:coffee-script/register --recursive -R list",
    "start": "node server.js "
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/DinisCruz/Maturity-Models.git"
  },
  "author": "Dinis Cruz",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/DinisCruz/Maturity-Models/issues"
  },
  "homepage": "https://github.com/DinisCruz/Maturity-Models#readme",
  "engines": {
    "node": "5.3.0"
  },
  "dependencies": {
    "async": "^1.5.2",
    "body-parser": "^1.15.1",
    "cheerio": "^0.20.0",
    "coffee-script": "^1.10.0",
    "d3": "^3.5.16",
    "express": "^4.13.4",
    "express-load": "^1.1.15",
    "file-stream-rotator": "0.0.6",
    "fluentnode": "*",
    "mocha": "^2.4.5",
    "morgan": "^1.7.0",
    "pug": "2.0.0-beta2",
    "serve-index": "^1.7.3"
  },
  "devDependencies": {
    "supertest": "^1.2.0"
  }
}
```

**wallaby.js**

```js
module.exports = function () {
    return {
        files: [
            'src/**/*.coffee',
            'views/**/*.pug',
            { pattern: 'data/**/*'              , instrument: false, load: false, ignore: false },
        ],

        tests: [
            'test/**/*.coffee'
        ],

        env: {
            type: 'node'
        }
    };
};
```
