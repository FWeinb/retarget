#### This is experimental. I would only use it if you are comfortable with breaking changes.

# retarget

#### selectors via targets


## Install

```bash
npm i retarget -S
```

**or**

```bash
yarn add retarget
```

---

```javascript
import retarget from 'retarget'

const STATE = {
  profile: {
    name: {
      first: 'Waylon',
      last: 'Jennings'
    }
  }
}

const lastNameSelector  = retarget`profile.name.last`

console.log(lastNameSelector(STATE)) // logs "Jennings"

```
## API

#### retarget `function`

```javascript
import retarget from 'retarget'

const selector = retarget`dot.seperated.path.to.value`

const state = {/* Huge object */}
selector(state) // returns the value at "dot.seperated.path.to.value"
```


**Returns**

`retarget` returns a function that when passed an obj, attempts to get the value for the given path.


