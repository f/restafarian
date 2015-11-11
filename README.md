# Restafarian
Node.js Restful Client in ES6

## Installation

```
npm install restafarian --save
```

## Proposal

```js
import {Client} from 'restafarian';

const {get, post, request} = new Client('http://api.example.com/v1');

class Users {

  @get('/users')
  getUsers(data) {
    return request(data);
  }
  
  @get('/users/:id')
  getUser(data) {
    // {url: "users/1", data: {name: "fatih"}}
    return request(data);
  }
  
  @post('/users')
  createUser(data) {
    return request(data);
  }
}

var users = new Users();
var user = users.getUser({id: 1, name: "fatih"}).then(() => {});
```
