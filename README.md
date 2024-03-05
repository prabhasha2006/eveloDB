# eveloDB
### The best local database admin nodejs

 *From EveloCore*


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
- Download the <b>eveloDB.js</b>
- Paste it where you want to create database.
- First time it will be create a directory './evelodb/' automatically.
- require evelodb.js to your main script.

## [Demo here](https://evelocore-chat-app.onrender.com)


### Link your eveloDB

> Put in to main javascrip file
```js
const eveloDB = require('./evelodb')
```
### Main functions of eveloDB
- Create a data as a object in the collection.
```js
// Structure
eveloDB.create('collection', [
    ['key','value']
])
```
```js
eveloDB.create('accounts', [
    ['username','evelocore'],
    ['name','EveloCore'],
    ['developer','K.Prabhasha'],
    ['email','kumuthuprabhasha@gmail.com']
])
```
- Find object by value (one or more...)
```js
// Structure
var user = eveloDB.find('collection', [
    ['key','value'],
    ['key2','value2']
])
console.log(user)
```
```js
var user = eveloDB.find('accounts', [
    ['username','evelocore']
])
console.log(user)
```
> Output
```bash
[
  {
    username: 'evelocore',
    name: 'EveloCore',
    developer: 'K.Prabhasha',
    email: 'kumuthuprabhasha@gmail.com'
  }
]
```


<p align="center">
<a href="#"><img title="Creator" src="https://img.shields.io/badge/Creator-EveloCore-red.svg?style=for-the-badge&logo=github"></a>
</p>
<p align="center">
<a href="https://github.com/prabhasha2006?tab=followers"><img title="Followers" src="https://img.shields.io/github/followers/prabhasha2006?color=green&style=flat-square"></a>
<a href="https://github.com/prabhasha2006/chat-application/stargazers/"><img title="Stars" src="https://img.shields.io/github/stars/prabhasha2006/chat-application?color=white&style=flat-square"></a>
<a href="https://github.com/prabhasha2006/chat-application/network/members"><img title="Forks" src="https://img.shields.io/github/forks/prabhasha2006/chat-application?color=yellow&style=flat-square"></a>
<a href="https://github.com/prabhasha2006/chat-application/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/prabhasha2006/chat-application?label=Watchers&color=red&style=flat-square"></a>
<a href="https://github.com/prabhasha2006/chat-application"><img title="Open Source" src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103"></a>
<a href="https://github.com/prabhasha2006/chat-application/"><img title="Size" src="https://img.shields.io/github/repo-size/prabhasha2006/chat-application?style=flat-square&color=darkred"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FAlipBot%2Fchat-application%2Fhit-counter&count_bg=%2379C83D&title_bg=%23555555&icon=probot.svg&icon_color=%2304FF00&title=hits&edge_flat=false"/></a>
<a href="https://github.com/prabhasha2006/chat-application/graphs/commit-activity"><img height="20" src="https://img.shields.io/badge/Maintained-No-red.svg"></a>&nbsp;&nbsp;
</p>
