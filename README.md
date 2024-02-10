# SWE-423 - Computer Graphics and Image Processing

## Bresenham's Line Drawing Algorithm

This algorithm is implemented using Python with the help of Matplotlib library for graph plotting.

## Algorithm Details

### For Slopes Closer to Horizontal (0 < m < 1), dy < dx:

**What we do:**

1. We check how much we move up and across for each step.
2. If dy < dx, we mainly move across.
3. But if dy becomes bigger than dx, we adjust by moving up a bit.

**Why we do it:**

By doing this, we ensure that our line remains straight and stays close to the ideal slope \( m \) (closer to horizontal) without missing any points.

**Input:**
Case: (1,1), (8,4)

**Output:**
![for horizontal slope](/img1.png)


### For Slopes Closer to Vertical (m > 1), dy > dx:

**What we do:**

1. We check how much we move up and across for each step.
2. If dy > dx, we mainly move up.
3. But if dx becomes bigger than dy, we adjust by moving across a bit.

**Why we do it:**

By doing this, we ensure that our line remains straight and stays close to the ideal slope \( m \) (closer to vertical) without missing any points.

**Inputs:**
Case: (1,1), (4,8)

**Output:**
![for vertical slope](/img2.png)
