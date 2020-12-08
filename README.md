# typescript-missing-nounusedlocals-error-for-react-with-new-jsx-transform
https://github.com/microsoft/TypeScript/issues/41882
## Steps

1. Run `yarn`
2. Run `yarn typecheck`

```
Done in 1.98s.
```

3. Replace `index.tsx` file content with the following code:

```ts
import React from "react";

export function Foo() {
  return <div />;
}
```

4. Run `yarn typecheck`

```
index.tsx:1:1 - error TS6133: 'React' is declared but its value is never read.

1 import React from "react";
  ~~~~~~~~~~~~~~~~~~~~~~~~~~


Found 1 error.
```

## Result
The first run does not throw the error unlike the second one.
