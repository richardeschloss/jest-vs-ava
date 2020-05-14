# Jest vs Ava -- the ultimate showdown!

Who can run the test the fastest?

```
const msg = 'Hello'

// Q: Expect msg to be 'Hello'
```

## Jest

```
// <-- minor DX improvement here...I didn't have to import anything
test('Hello', () => {  // <-- I can just write my tests asap
  const msg = 'hello'
  expect(msg).toBe('hello')
})
```

> npm run test:jest

![Jest Perf](results/jest_perf.png)

## Ava

```
import test from 'ava'  // <-- Minor foul: I had to write an extra line here

test('hello', (t) => { // <-- I wanted this to be my first line...
  const msg = 'hello'
  t.is(msg, 'hello')
})
```

> npm run test:ava

![Ava Perf](results/ava_perf.png)


###

Winner as of: (Update as perf tests change)

05/13/2020 - Ava