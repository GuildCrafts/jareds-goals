# Debugging in JavaScript


## JavaScript in General




The tracing the flow of the program

### logging values
### logging the call stack
### try / catch
### throwing on unexpected cases
### using a complex leveled logger

In complex application you might consider sharing a logger all over you application logging various bits of information at different levels of importance.

For example

```js

const logger = require('../logger')

class BlogPost {
  save(){
    logger.info(`saving BlogPost ${this.id}`)
    try{
      placeholderForDoingTheSave(this)
    catch(error){
      logger.error(`error saving BlogBpost ${this.id}`, error)
      throw error
    }
  }
}
```

## Debugging in Node


## Debugging in Chrome Developer Tools


