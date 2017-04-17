# state_adjacency_matrix.js
State adjacency matrix for JS

## What?
States have neighbors.  This is a list thereof.

```javascript
const states = ["AK", "AL", "AR", ...];

const state_adjacency = [
  [],
  [25, 42, 10, 09],
  [24, 42, 25, 18, 43, 36],
  ...
];
```

This says:
1. State 0 is `'AK'`.
    1. State 0 has no neighbors.
1. State 1 is `'AL'`.
    1. State 1's neighbors are `25 'MS'`, `42 'TN'`, `10 'GA'`, and `9 'FL'`.
1. State 2 is `'AR'`.
    1. State 2's neighbors are `24 'MO'`, `42 'TN'`, `25 'MS'`, `18 'LA'`, `43 'TX'`, and `36 'OK'`

... and so on.