[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)


#Start
First You need to download repos (both are public) ->

### 1
 [ajaskolski/microservices-demo-cypress](https://github.com/ajaskolski/microservices-demo-cypress)
 I forked front end repository and push my own docker image to introduce cypress to
 ajaskolski/front-end
 to start just run docker containers:
 
  `docker-compose -f deploy/docker-compose/docker-compose.yml up -d`
  
  after work just clean containers:
  
  `docker-compose -f deploy/docker-compose/docker-compose.yml down`
### 2 
  [ajaskolski/front-end](https://github.com/ajaskolski/front-end) 
 All the sweets of cypress and new code can be found in this repo.
 You can run cypress tests by 
 
 `cypress run` 
 
 or use gui 
 
 `cypress open`
  

#Summary

Added docker image of front-end service with cypress tests.

To easier locate elements without id I mostly add custom data attributes in html.
For modern projects in react/vue there should shared file beetween src code and test code for updated values of locators.

Application got some bugs so I choose sample paths viable to automate.

Add whole configuration contains eslint, prettier and tsconfig.

There is case using hardcoded data and case that creates its own user data and clean it afterwards with api methods.

Showed one of possible approaches to the topic. Used piece of page object patern, add some custom method to cy, add plugin with faker to create data in test.

Every push to front-end repository master branch will trigger update of docker image on dockerhub as latest tag.

Next step would be adding database for clean DDT firebase/mysql, linking pushes to CI/CD, put some visual testing with Percy or any similiar.
