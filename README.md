
<h1 align="center">
  <br>
  <a><img src="https://i.ibb.co/t4c363X/20240305-125417.png" width="200"></a>
  <br>
  <b>EveloDB</b>
  <br>
</h1>
<h3 align="center">An awesome local database admin with nodejs.<br>Made by EveloCore</h3>
<br>
<hr>

## Requirements
> Nodejs

## npm packages
> "fs" (inbuild package)

### About this
- ✓ Manage with json.
- ✓ Fast and easy.
- ✓ Only nodejs required.

## Easy Installation
Get started:
- Download the <b>evelodb.js</b>
- Paste it where do you want to create database.
- First time it will be create a directory './evelodb/' automatically.
- require evelodb.js to your main script.

## [Download EveloDB.js](https://github.com/prabhasha2006/eveloDB)

<hr>

### Link your EveloDB

> Put in to main javascript file
```js
const eveloDB = require('./evelodb')
```
## Main functions of eveloDB

<hr>

- Create a data as a object in the collection.
```js
// Structure
eveloDB.create('collection', 
  [
    ['key','value']
  ]
)
```
```js
eveloDB.create('accounts', 
  [
    ['username','evelocore'],
    ['name', 
      {
         firstname: 'Kumuthu',
         lastname: 'Prabhasha'
      }
    ],
    ['developer','K.Prabhasha'],
    ['email','example@gmail.com']
  ]
)
```

<hr>

- Find object by value (one or more...)
```js
// Structure
const user = eveloDB.find('collection', 
  [
    ['key','value'],
    ['key2','value2']
  ]
)
console.log(user)
```
```js
const user = eveloDB.find('accounts', 
  [
    ['username','evelocore']
  ]
)
console.log(user)
```
> Output
```bash
[
  {
  username: 'evelocore',
  name: 'EveloCore',
  developer: 'K.Prabhasha',
  email: 'example@gmail.com'
  }
]
```

<hr>

- Check avalability (is any object includes the keys/values)
```js
// Structure
const user = eveloDB.check('collection', 
  [
    ['key','value'],
    ['key2','value2']
  ]
)
console.log(user)
```
```js
const user = eveloDB.check('accounts',
  [
    ['username','evelocore']
  ]
)
console.log(user)
// Return a boolean value ( true/false )
```
> Output
```bash
true
```

<hr>

- Update an object
```js
// Structure
eveloDB.edit('collection', 
  [
    ['key','value'] // find() object witch one wants to update
  ],
  [
    ['key','value'],  // replace or add 
    ['key2','value2'],
    ['newKey','new value']
  ]
)
```
```js
eveloDB.edit('accounts', 
  [
    ['username','evelocore'],
    ['email','example@gmail.com']
  ],
  [
    ['name','EveloCore Official'],
    ['developer','Kumuthu Prabhasha'],
    ['email','evelocore@gmail.com']
  ]
)
// The object includes username='evelocore' and email='example@gmail.com' is successfully updated with second array's values
```

<hr>

- Delete an object
```js
// Structure
eveloDB.delete('collection', 
  [
    ['key','value'] // find() object witch one wants to delete
  ]
)
```
```js
eveloDB.delete('accounts', 
  [
    ['username','evelocore']
  ]
)
// The object includes username='evelocore' is fully deleted
```

<hr>

- Reset collection
```js
// Structure
eveloDB.reset('collection')
```
```js
eveloDB.reset('accounts')
// 'accounts' collection has been deleted!
```

<hr>


<p align="center">
<a href="#"><img title="Creator" src="https://img.shields.io/badge/Creator-EveloCore-red.svg?style=for-the-badge&logo=github"></a>
  <br><br>
  Copyright 2024 © EveloCore developers - All rights reserved
</p>

