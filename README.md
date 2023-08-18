# seams 0.0.9.beta5
Used for creating seams loops within any integers starting with 8-bit unsigned integers
## `seamsSimilar`
`seams` is now becoming a `Similar`, like many other <b>AyurProject Language</b> classes. `seamsSimilar` is like having seams as part of a process or texture, but `seamsSimilar` is not exactly like a seaming process.
## `seamsSimilar` loop matrix outline
```
100/2+50/2 200 
100        150 
150        175 
175        182 
182        191 
191        196
196        198 <-- seams like a border
198        199 <-- seams like a border
199        200 <-- seams like a border
200        200 <-- seams like a border
 ^          ^
 |          |   
```
```
y[1,1]  = (x/2 + a/2) * 2
y[1,2]  = (x/2 + b/2) * 2
y[2,1]  = (y[1,1]/2 + a/2) * 2
y[2,2]  = (y[1,2]/2 + b/2) * 2
y[3,1]  = (y[2,1]/2 + a/2) * 2
y[3,2]  = (y[2,2]/2 + b/2) * 2
y[4,1]  = (y[3,1]/2 + a/2) * 2
y[4,2]  = (y[3,2]/2 + b/2) * 2
y[5,1]  = (y[4,1]/2 + a/2) * 2
y[5,2]  = (y[4,2]/2 + b/2) * 2
y[6,1]  = (y[5,1]/2 + a/2) * 2
y[6,2]  = (y[5,2]/2 + b/2) * 2
y[7,1]  = (y[6,1]/2 + a/2) * 2 <-- seams like a border
y[7,2]  = (y[6,2]/2 + b/2) * 2 <-- seams like a border
y[8,1]  = (y[7,1]/2 + a/2) * 2 <-- seams like a border
y[8,2]  = (y[7,2]/2 + b/2) * 2 <-- seams like a border
y[9,1]  = (y[8,1]/2 + a/2) * 2 <-- seams like a border
y[9,2]  = (y[8,2]/2 + b/2) * 2 <-- seams like a border
y[10,1] = (y[9,1]/2 + a/2) * 2 <-- seams like a border
y[10,2] = (y[9,2]/2 + b/2) * 2 <-- seams like a border
```
## `seamsSimilar` like a border
As opposed to `seamlessSimilar` loops, `seamsSimilar` can be used to mark a bordering area around looping sections.