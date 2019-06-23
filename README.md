# Data structures
## ring - a cyclic list

```
ring(1,2,3)[0] == 1
ring(1,2,3)[2] == 3
ring(1,2,3)[3] == 1
```

## range - x to y in z steps

```
range(1,3,0.5) == ring(1.0,1.5,2.0,2.5)
```

## ramp - return the last element when list is exhausted

```
ramp(1,2,3)[0] == 1
ramp(1,2,3)[2] == 3
ramp(1,2,3)[3] == 3
```

## Splatting a ring / range
```
*ring(1,2,3) == [1,2,3]
(ramp *range(3,1,0.5)) == (ramp 3.0, 2.5, 2.0, 1.5)
```

## Taking an element from a ramp or ring
```
a=ring(1,2,3)
puts a.tick # 1
puts a.tick # 2
puts a.look # 2
puts knit(1,2,3,4,5,6) # (ring 1, 1, 3, 3, 3, 3, 5, 5, 5, 5, 5, 5)
```
