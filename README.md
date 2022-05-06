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
- 2d bbox bias to bottom right x, int
- 2d bbox bias to bottom right y, int
- 3d bbox center x, meter
- 3d bbox center y, meter
- 3d bbox center z, meter
- 3d bbox radius x, meter
- 3d bbox radius y, meter
- 3d bbox radius z, meter
- 3d bbox orientation x
- 3d bbox orientation y

# _pc.npz

- (N, 6)
- (x, y, z, r, g, b)
- x: right is positive
- y: inward is positive
- z: up is positive

# _bbox.npy

- (K, 8)
- (center_x, center_y, center_z, radius_x, radius_y, radius_z, heading_angle, class_int)
- heading_angle: rotation from x to -y

# _votes.npz

- (N, 10)
- (mask, v1x, v1y, v1z, v2x, v2y, v2z, v3x, v3y, v3z)
- mask: 0: point is not in any bbox, vixyz = 0
- mask: 1: point is in at least one bbox
- point + vote = bbox center
- if point is only in one bbox, 3 votes are the same
