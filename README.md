#Why?

When you use a web service which requires user name and password, mostly it is stored in your app JS code. But the javascript code is not encrypted and can easily be accessed by unzipping the APK. But if you try opening config.xml you will realise that this file is encrypted and cannot be read easily.

#What?
This plugin allows you to store your sensitive data such as passwords, usernames etc. in config.xml. This is stored by creating custom parameters in config.xml. In the runtime, these parameters can be read from config.xml and used in javascript code. This really helps in creating next level of security for cordova based apps.

#How?


var paramkeyArray=["mypluginurl","getdyddefaultpref","authname"];
CustomConfigParameters.get(function(respo){
  console.log('DydFetchConfigPreference respo',respo);
},function(err){
  console.log('DydFetchConfigPreference err',err);
},paramkeyArray);