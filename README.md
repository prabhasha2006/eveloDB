
<h1 align="center">
  <br>
  <a><img src="https://i.ibb.co/t4c363X/20240305-125417.png" width="200"></a>
  <br>
  <b>EveloDB</b>
  <br>
</h1>
<h3 align="center">A Local Database Management System with Node.js featuring B-Tree Implementation</h3>
<br>
<hr>

## Requirements
- Node.js

## Installation

### Via npm
```bash
npm i evelodb
```

### Manual Installation
- Download `evelodb.js`
- Place it in your project directory
- First run creates `./evelodatabase/` automatically

### Import
```js
const eveloDB = require('evelodb')
const db = new eveloDB();
```

## Operations

### Create
```js
// Structure
db.create('collection', {
    key: 'value'
});

// Example
db.create('collection', {
    token: 'unique_id',
    username: 'evelocore',
    name: {
        firstname: 'Kumuthu',
        lastname: 'Prabhasha'
    },
    email: 'example@gmail.com'
});
```

### Find
```js
// Structure
const result = db.find('collection', {
    key: 'value'
});

// Example
const user = db.find('collection', {
    username: 'evelocore'
});
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

### Search
```js
// Structure
const result = db.search('collection', {
    key: 'partial_value'
});

// Example
const user = db.search('collection', {
    username: 'evelo'
});
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

### Get All
```js
// Structure
const result = db.get('collection');

// Example
const users = db.get('accounts');
console.log(users)
```

### Check Existence
```js
// Structure
const exists = db.check('collection', {
    key: 'value'
});

// Example
const exists = db.check('accounts', {
    username: 'evelocore'
});
console.log(exists)
```
> Output
```bash
true
```

### Update
```js
// Structure
db.edit('collection', 
    { key: 'value' },     // find condition
    { key: 'new_value' }  // new data
);

// Example
db.edit('accounts', 
    { username: 'evelocore' },
    {
        name: 'EveloCore Official',
        email: 'updated@gmail.com'
    }
);
```

### Delete
```js
// Structure
db.delete('collection', {
    key: 'value'
});

// Example
db.delete('accounts', {
    username: 'evelocore'
});
```

### Reset Collection
```js
// Structure
db.reset('collection');

// Example
db.reset('accounts');
```

## Features
- ✓ JSON-based storage
- ✓ B-Tree indexing
- ✓ Fast retrieval
- ✓ Node.js only

<p align="center">
Copyright 2024 © EveloCore - All rights reserved
</p>
