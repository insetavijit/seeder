# oSeed : master 
    @version : 1.0.0
    @type : documents
    @use : default

> ## INTRODUCTION :
This Porject is created for easy include source codes for rapid devlopment
in this repo we are including seed porject parts as branches and pulling whem when needed
so this is not a repo that you clone and start working on in
this repo is all about pulling small blocks to make your custom workfollow

> ## HOW IT WORKS :
before starting a project we need a good start point , and this seed project is going to 
give you that .
<br/>lets see an example :

**example : 01 : Create a Bootstrap-scss-pug project**
to Create this project we need
- sass
- pug
- javaScript ( in this case : es2015 )
- bootstrap library ( local devlopment )
- jQuery , popper
- popper.js  ( i am also including )
- holder.js  ( for image placeholders )

Now to Setup those things May take A bit Time , <br/>
but we can setit up in secounds with oSeed <br/>
HOW ? lets see

@Step : 1 : include oSeed to Your Project 
```
//this will include oSeed Project as remote
git remote add oseed https://github.com/insetavijit/oSeed.git

//Next : if you don't need to push to oSeed then ,
git remote oseed set-url --push no_push

```

Grate you are all set  . to pull from oSeed

@Step: 2 : Get the Manual
```
// ( NOT REQUIRED ) if you want a living documentration on your project root
git pull oseed master

```
@Step: 2 : Get Required Blocks :

```
//Get the pug thing
git pull oseed pug

//Get sass
git pull oseed sass

//Get js-bable-webpack
git pull oseed js-bable-webpack

//Get a local live Server and other tool sets ( bassic tools )
git pull oseed tools

//Get updates for gulpSetup
git pull oseed gulpSetup
```
**ALL BLOCKS COMES WITH THEIR OWN DOCUMENTRATION**<br/>
So please see the "/DOCUMENTRATION/" dir to know 
more about this blocks so 

Now at the end we have a full `( sass + pug + webpack + bable + es2015 )` workfollow setup . <br/>Reay to Include Bootstrap

@step : 4 : setup bootstrap
now we just need to download and setup bootstrap and its dependencys
```
//Download all the dependencys for ( all the blocks ) [ With npm ]
$ npm i

//Get bootstrap and its dependencys ( with npm )
$ npm i bootstrap jquery popper.js @types/jquery


//Download all the dependencys for ( all the blocks ) [ With pnpm ]
$ pnpm i

//Get bootstrap and its dependencys ( with pnpm )
$ pnpm i bootstrap jquery jquery.appear popper.js holder.js @types/jquery

```
Now , when all the dependencys are installed <br/>
We need to Setup Bootstrap and all it's dependencys
for this we need to configer the `vl.json` file <br/>

Just add this json block to the vl.js file

```
"sft":{
        "libs":{
            "js":[
                "node_modules/jquery/dist/jquery.min.js",
                "node_modules/jquery.appear/jquery.appear.js",
                "node_modules/popper.js/dist/umd/popper.min.js",
                "node_modules/bootstrap/dist/js/bootstrap.min.js",
                "node_modules/holderjs/holder.js"
            ],
            "css":[
                "node_modules/bootstrap/dist/css/bootstrap.min.css"
            ]
        }
    },

```
and now we can run 
```
// copy files from ** to the dist/libs dir
$ gulp sft:libs

```
AND DONE .
**YOU HAVE A MODULER BOOTSTRAP FONTEND DEVLOPMENT WORKFOLLOW**
<br/>
Test It 
Run 
```
// run the every thing in watch mode
$ gulp show:w pug:w sass:w js:w

```
Now you can add this CMND to the package.json file so you can run everytin at once 

```
{
    "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start" : gulp sass:w pug:w js:w show:w
  }
}
```
and then run `npm run start` to start the devlopment stack .