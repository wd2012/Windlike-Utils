# Number
```js
interface NumberModule {
  createRandomFunction: (min: number, max: number, float: boolean) => () => number;
}
```

## createRandomFunction
#### Describe
Create a function to generate a random number.
```js
(min: number, max: number, float: boolean) => () => number;
```

#### Arguments
  - min(number)
  - max(number)
  - float(boolean)

#### Returns
(```() => number```)

#### Example
```js
const createRandom = utils.number.createRandomFunction(100, 1, true);

createRandom();
```