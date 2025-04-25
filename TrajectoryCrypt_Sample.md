# TrajectoryCrypt Simulation Example

## Input
```
User input: 57803426
```

### Step 1: Bitstream generation
- Convert to binary:
  ```
  5 = 0101
  7 = 0111
  ...
  Full 32-bit stream = 01010111100000000011010000100110
  ```

### Step 2: Rearrangement
- Split into 1s and 0s
- Form 2n-bit stream: all 1s (doubled) + all 0s (doubled)

### Step 3: Logic latch output (under noise)
- a0 = 0.18, a1 = -0.32, a2 = 0.56 → A = (0.56, -0.32, 0.18)
- b0 = 0.01, b1 = 0.77, b2 = -0.09 → B = (-0.09, 0.77, 0.01)
...

### Step 4: Form trajectory
- Vectors A, B, C summed in 3D space
- Fitted to function f(x)

### Step 5: Encrypt
- Input original x into f → y

### Step 6: Decrypt by identifying:
- Tangent match
- Projection area between curve and line match

Only x with matching behavior is accepted as original.
