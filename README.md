Output of `npm run build` [is correct](./dist/).

Output of `npm run test` shows issue with transforms:
```
 FAIL  __tests__/b.test.js
  ● Test suite failed to run

    Cannot find module './src/./b' from '__tests__/b.test.js'

    > 1 | import b from "@/b";
        |                    ^
      2 |
      3 | it("returns 'boo'", () => {
      4 |     expect(b()).toBe("boo");

      at Resolver._throwModNotFoundError (node_modules/jest-resolve/build/resolver.js:491:11)
      at Object.<anonymous> (__tests__/b.test.js:1:20)

 FAIL  __tests__/a.test.js
  ● Test suite failed to run

    Cannot find module './src/./a' from '__tests__/a.test.js'

    > 1 | import a from "@/a";
        |                    ^
      2 |
      3 | it("returns 'boo'", () => {
      4 |     expect(a()).toBe("boo");

      at Resolver._throwModNotFoundError (node_modules/jest-resolve/build/resolver.js:491:11)
      at Object.<anonymous> (__tests__/a.test.js:1:20)

Test Suites: 2 failed, 2 total
Tests:       0 total
Snapshots:   0 total
Time:        0.324 s
Ran all test suites.
npm ERR! Test failed.  See above for more details.
```