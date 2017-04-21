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

## Full dump

```
1> state_adjacency.map( 
     (row,id) => '\n' + states[id] + ' - ' + row.map(a => `${a} ${states[a]}`)
                                                .join(', ')
   ).join('\n');

"
AK -
AL - 25 MS, 42 TN, 10 GA, 9 FL
AR - 24 MO, 42 TN, 25 MS, 18 LA, 43 TX, 36 OK
AZ - 4 CA, 33 NV, 44 UT, 5 CO, 32 NM
CA - 37 OR, 33 NV, 3 AZ
CO - 50 WY, 29 NE, 16 KS, 36 OK, 32 NM, 3 AZ, 44 UT
CT - 34 NY, 19 MA, 39 RI
DC - 20 MD, 45 VA
DE - 20 MD, 38 PA, 31 NJ
FL - 1 AL, 10 GA
GA - 9 FL, 1 AL, 42 TN, 27 NC, 40 SC
HI -
IA - 23 MN, 48 WI, 14 IL, 24 MO, 29 NE, 41 SD
ID - 26 MT, 50 WY, 44 UT, 33 NV, 37 OR, 47 WA
IL - 15 IN, 17 KY, 24 MO, 12 IA, 48 WI
IN - 22 MI, 35 OH, 17 KY, 14 IL
KS - 29 NE, 24 MO, 36 OK, 5 CO
KY - 15 IN, 35 OH, 49 WV, 45 VA, 42 TN, 24 MO, 14 IL
LA - 43 TX, 2 AR, 25 MS
MA - 39 RI, 6 CT, 34 NY, 30 NH, 46 VT
MD - 45 VA, 49 WV, 38 PA, 7 DC, 8 DE
ME - 30 NH
MI - 48 WI, 15 IN, 35 OH
MN - 48 WI, 12 IA, 41 SD, 28 ND
MO - 12 IA, 14 IL, 17 KY, 42 TN, 2 AR, 36 OK, 16 KS, 29 NE
MS - 18 LA, 2 AR, 42 TN, 1 AL
MT - 28 ND, 41 SD, 50 WY, 13 ID
NC - 45 VA, 42 TN, 10 GA, 40 SC
ND - 23 MN, 41 SD, 26 MT
NE - 41 SD, 12 IA, 24 MO, 16 KS, 5 CO, 50 WY
NH - 46 VT, 21 ME, 19 MA
NJ - 8 DE, 38 PA, 34 NY
NM - 3 AZ, 44 UT, 5 CO, 36 OK, 43 TX
NV - 13 ID, 44 UT, 3 AZ, 4 CA, 37 OR
NY - 31 NJ, 38 PA, 46 VT, 19 MA, 6 CT
OH - 38 PA, 49 WV, 17 KY, 15 IN, 22 MI
OK - 16 KS, 24 MO, 2 AR, 43 TX, 32 NM, 5 CO
OR - 4 CA, 33 NV, 13 ID, 47 WA
PA - 34 NY, 31 NJ, 8 DE, 20 MD, 49 WV, 35 OH
RI - 6 CT, 19 MA
SC - 10 GA, 27 NC
SD - 28 ND, 23 MN, 12 IA, 29 NE, 50 WY, 26 MT
TN - 17 KY, 45 VA, 27 NC, 10 GA, 1 AL, 25 MS, 2 AR, 24 MO
TX - 32 NM, 36 OK, 2 AR, 18 LA
UT - 13 ID, 50 WY, 5 CO, 32 NM, 3 AZ, 33 NV
VA - 27 NC, 42 TN, 17 KY, 49 WV, 20 MD, 7 DC
VT - 34 NY, 30 NH, 19 MA
WA - 13 ID, 37 OR
WI - 22 MI, 23 MN, 12 IA, 14 IL
WV - 35 OH, 38 PA, 20 MD, 45 VA, 17 KY
WY - 26 MT, 41 SD, 29 NE, 5 CO, 44 UT, 13 ID"
```
