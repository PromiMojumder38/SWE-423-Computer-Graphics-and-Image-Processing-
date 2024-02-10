# SWE-423 - Computer Graphics and Image Processing

## Bresenham's Line Drawing Algorithm

This algorithm is implemented using Python with the help of Matplotlib library for graph plotting.

## Algorithm Details

### For Slopes Closer to Horizontal (0 < m < 1), dy < dx:

**What we do?**

1. We check how much we move up and across for each step.
2. If dy < dx, we mainly move across.
3. But if dy becomes bigger than dx, we adjust by moving up a bit.

**Why we do it?**

By doing this, we ensure that our line remains straight and stays close to the ideal slope \( m \) (closer to horizontal) without missing any points.

**Input:**
Case: (1,1), (8,4)

**Output:**
![for horizontal slope](/img1.png)


### For Slopes Closer to Vertical (m > 1), dy > dx:

**What we do?**

1. We check how much we move up and across for each step.
2. If dy > dx, we mainly move up.
3. But if dx becomes bigger than dy, we adjust by moving across a bit.

**Why we do it?**

By doing this, we ensure that our line remains straight and stays close to the ideal slope \( m \) (closer to vertical) without missing any points.

**Inputs:**
Case: (1,1), (4,8)

**Output:**
![for vertical slope](/img2.png)

**Why we didn't apply case 1 for the line between (1,1) and (4,8)?**


If we used Case 1 (0 < m < 1) for the line between (1,1) and (4,8), it would look like we're climbing a hill with tiny steps when we actually need big steps. The line would appear too flat compared to the steepness we want between these two points. So, we adjusted the algorithm to prioritize changes in the x-coordinate. This ensures that the line rises steeply, matching the steeper slope. We also iterated over y-coordinates and calculated corresponding x-coordinates.


![image](https://github.com/PromiMojumder38/SWE-423-Computer-Graphics-and-Image-Processing-/assets/74852911/6d4b6fd5-879b-4563-a05e-27d1746282d8)


