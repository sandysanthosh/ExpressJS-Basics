Welcome to the ExpressJS-Basics wiki!


pusher   
->  real time applciation
-> dataanalitics
-> 200 message / 100 mx communicaiton

traffic:

49 dollar
unlimitted


MLAB:

->free mangodb


javascript
nodejs

real time pooling app



express
connect
socket.io
pug
mongo
coffee
redis



mean

mongodb
express
angular
node


express:
https://www.youtube.com/watch?v=gnsO8-xJ8rs&t=3302s 
open source web framework
build powerful web app
node.js
uses mvc

.
express:

->middleware of application


middleware
routing
template engine-ejs,handlebars,jade
forms & input
models, orm ,database-  mongodb
express generator

npm init
npm install express --save
npm install body-parser --save

To start server:
--> node app

save to package JSON

package.json:

"main" : "app.js",
},
"dependencies":{
  "express":"*"    
   "body-parser" : "*"    // *current version
},


create a new app.js entry file:

app.js:

step 1:

console.log("hello world");

step 2:

var express = require('express');
var bodyparser =  require('body-parser');
var path =  require('path');
var expressValidator = require('express-validator');

var app = express();

var logger= function(req, res, next){
   console.log('Logging...');
   next();
}

 app.user(logger);   // going to use logger methods  in console


app.get('/', function(req, res){
   res.send('Hello world');
});


 app.get('/', function (req, res){
   db.users.find(function (err, docs) {
res.render('index',{
      title : 'customers',
      users:  users,
      errors: errors
    });
    
    })
});
  


app.post('/user/add' ,function (req, res){

 req.checkBody('first_name' , 'First_name is Required').notEmpty();   // name not empty
 req.checkBody('last_name' , 'last_name is Required').notEmpty();   // name not empty
 req.checkBody('email' , 'email is Required').notEmpty();   // name not empty

  var errors = req.validationErrors();

if(errors){
    res.render('index',{
      title : 'customers',
      users:  users,
      errors: errors
    });
}
else{
var newUse r= {
  first_name : req.body.first_name,
  last_name: req.body.last_name,
  email : req.body.email
}
   console.log('SUCCESS');
});

db.users.insert(newUsers, function(err, response){

 if(err){
 console.log(err);
  }); 
  }
});

app.listen(3000, function() {  // uses listen sever
   console.log('server started on port 3000...');
})



index.html:

<form action="/users/add" method="POST">  
First Name: <input type="text" name="first_name">  <br>  
Last Name: <input type="text" name="last_name">   <br> 
email: <input type="text" name="email">   <br> 
<input type="submit" value="Submit">  
</form>  


moduels:
 
express validator:

->npm install express-validator --save


middle ware options:


//Express validator Middleware
-->add this in app.js

req.checkBody({
  email: {
    notEmpty: true,
    isEmail: true
  },
  password: {
    notEmpty: true,
    matches: {
      // more than one options must be passed as arrays
      options: ['someregex', 'i'],
      // single options may be passed directly
      // options: /someregex/i
    },
    errorMessage: 'Invalid password'
  },
  // Wildcards and nested paths are supported as well
  'name.first': {
    optional: {
      options: { checkFalsy: true }
    }
  },
  termsAndConditionsAgreement: {
    isBoolean: {
      errorMessage: 'should be a boolean'
    }
  }
});

https://www.npmjs.com/package/mongojs

-->npm install mongojs --save

insert in app.js:

var mongojs = require('mongojs')
var db = mongojs(customapp, [collections])


jquery CDN: 
http://code.jquery.com/

-> uncompressed format click
<script
  src="http://code.jquery.com/jquery-migrate-3.0.1.js"
  integrity="sha256-VvnF+Zgpd00LL73P2XULYXEn6ROvoFaa/vbfoiFlZZ4="
  crossorigin="anonymous"></script>


 