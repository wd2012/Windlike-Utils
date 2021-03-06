# String
```js
interface StringModule {
  replace: (match: RegExp | string) => (str: string, substitute: any) => string;
  split: (char: string | RegExp) => (str: string) => string[];
  match: (regexp: RegExp) => (str: string) => string[];
}
```

## replace
#### Describe
```js
(match: RegExp | string) => (str: string, substitute: any) => string;
```

#### Arguments
  - match(RegExp | string)

#### Returns
(```(str: string, substitute: any) => string```)

#### Example
```js
const str = 'I\'m Windlike.';
const replaceWindlike = utils.string.replace('Windlike');

replaceWindlike(str, 'I');  // I'm I.
```

## split
#### Describe
```js
(char: string | RegExp) => (str: string) => string[];
```

#### Arguments
  - char(RegExp | string): 分割符

#### Returns
(```(str: string) => string[]```)

#### Example
```js
const str = 'I And You';
const splitSpace = utils.string.split(' ');

splitSpace(str);  // ['I', 'And', 'You']
```

## match
#### Describe
```js
(regexp: RegExp) => (str: string) => string[];
```

#### Arguments
  - regexp(RegExp)

#### Returns
(```(str: string) => string[]```)

#### Example
```js
const re = /[\w]+/g;
const str = 'I am a string.';
const matchWork = utils.string.match(re);

matchWork(str);  // ['I', 'am', 'a', 'string']
```