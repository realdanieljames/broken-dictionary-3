# Instructions:
- There are 14 errors in this app.
- Do not think you can copy your old app over to the new.
- They do not match.
- Controllers have been included and other changes have been made. So read the code.
- Test to make sure each controller, model, view, router, and file is working using PostMan, Robo 3T and the Browser
- Make a corrected.md file and write each error that you corrected and how you corrected it.
  

node module  
bin www file  
packagelock.json  
index  
user  
<hr>
<hr>
<hr>
<hr>

## 1st error:- `ReferenceError: mongoose is not defined`
![](mdMedia/error1.png)


## 1st fix : `require mongoose in Word.js file`
```javascript
const mongoose = require('mongoose')
```
![](mdMedia/fixed1.png)  

<hr>
<hr>
<hr>
<hr>

## Error 2: `TypeError: Cannot read property 'push' of undefined`

![](mdMedia/error2.png)


## Fixed 2: `Router to Router()` in wordRoutes.js
```javascript
const router = require('express').Router();
```
![](mdMedia/fixed2.png)

<hr>
<hr>
<hr>
<hr>

## Error 3: `ReferenceError: getUpdateWord is not defined`
![](mdMedia/error3.png)


## Fixed 3: include `getUpdateWord` in `require('./controllers/wordController');`  

![](mdMedia/fixed3.png)  
<hr>
<hr>
<hr>
<hr>


## Error 4: `ReferenceError: route is not defined`

![](mdMedia/error4.png)

## Fixed 4: `r` was left out in `router`
![](mdMedia/fixed4.png)

<hr>
<hr>
<hr>
<hr>


## Error 5: `ReferenceError: env is not defined`
![](mdMedia/error5.png)


## Fixed 5 : should be `process.env.MONGODB_URI`
![](mdMedia/fixed5.png)

<hr>
<hr>
<hr>
<hr>
<hr>

## Error 6: `ReferenceError: app is not defined`  

![](mdMedia/error6.png)

## Fixed 6: define `app` using `express()` 

needs:
```javascript
const app = express();
```
![](mdMedia/fixed6.png)

## Error 7: `ReferenceError: wordRouter is not defined`

![](mdMedia/error7.png)

## Fixed 7: misspelled WorRouter change `wordRoutes` to `wordRouter`

![](mdMedia/fixed7.png)  
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>

## Error 8: ` MongooseError: The `uri` parameter to `openUri()` must be a string, got "undefined"`

![](mdMedia/error8.png)


## Fixed 8: include `MONGODB_URI=mongodb://localhost/broken-dictionary-3` string in `.env` file  

![](mdMedia/fixed8.png)  

## and require it in the app.js file
```javascript
require('dotenv').config();
```

<hr>
<hr>
<hr>
<hr>
<hr>
<hr>

## Error 9: `getAllWords` `wordController.js`
![](mdMedia/error9.png)


## Fixed 9: req mistakenly defined in res' space

![](mdMedia/fixed9.png)

```javascript
  getAllWords: (res, req) => {}
```
should be:

```javascript
  getAllWords: (req, res) => {}
```

