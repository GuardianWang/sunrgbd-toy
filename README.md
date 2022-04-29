In SUNRGBD, y is in/out-ward, 

# calib

- row1: rotation by column, rotation is camera to world, for [x, z, y]
- row2: intrinsic by column: [[fx, 0, 0], [0, fy, 0], [cx, cy, 1]]

# image

- width: 730
- height: 530

# depth

- row: x(column), z(depth), y(row), r, g, b
- x: right is positive
- y: up is positive
- x, y, z range: meter
- r, g, b range: [0, 1]

# label

- name
- 2d bbox top left x, int
- 2d bbox top left y, int
- 2d bbox bottom right x, int
- 2d bbox bottom right y, int
- 3d bbox center x, meter
- 3d bbox center y, meter
- 3d bbox center z, meter
- 3d bbox radius x, meter
- 3d bbox radius y, meter
- 3d bbox radius z, meter
- 3d bbox orientation x
- 3d bbox orientation y

