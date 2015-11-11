# Restafarian
Node.js Restful Client in ES6

## Installation

```
npm install restafarian --save
```

## Proposal

```
import {Client} from 'restafarian';

const {base, get, post} = new Client('http://api.example.com/v1');

@base('/users')
class Users {

  @get('/')
  getUsers() {
    return (request, response) => {
      this.users = response;
    }
  }
  
  @get('/:id')
  getUser(id) {
    return {id};
  }
  
  @post('/')
  createUser(data) {
    return {data};
  }
}

var users = new Users();
var user = users.getUser(1);
```
