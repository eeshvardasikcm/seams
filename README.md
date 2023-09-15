# seams 0.0.9.beta6
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


## `seamsSimilar` math concept
Above is a small matrix that outlines some possible math for determining where to make the `seamsSimilar` occur between two integers. Therr are 10 points made using the matrix. When looking at the math only, the `seams`, or `seamsSimilar` appear like they will work good closer to one of the integers instead of halfway between. The matrix wws created to simplify the calculations needed when working with unsigned integers, as to avoid bit calculations. One integer may be considered to have a solid part and an empty part. The solid part would be the part of the contigous space between the 1 and the value of the integer. The empty part would be the space after the value of the integer that, perhaps, does not contain any material. When connecting two integers, or materials, together, `seamsSimilar` appears like it maybe will behave as if it is zooming out a camera and then connecting the two materials together, making the resultant integer between the two original integers. The matrix outlined above appears to be showing options of where the `seams` will be if the two integers are able to be created at the same time that the `seamsSimilar` operation is done on them.
## `seamsSimilar` concept
The concept behind `seamsSimilar`, so far, appears to be for connecting two things together, like if there was two cloths that needed to be sown together to make them into one cloth. This concept may potentially apply to textures and materials in Unreal Engine. `seams` will also contain a `seamless` class that will be usable for mixing audio tracks together, and also for mixing other integer based items together.