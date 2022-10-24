https://stackoverflow.com/questions/65581304/rotate-a-pointcloud-in-z-axisimport open3d as o3d 

import numpy as np 

xyz = o3d.io.read_point_cloud("data.pcd")
R = xyz.get_rotation_matrix_from_xyz((0.7 * np.pi, 0, 0.6 * np.pi))
xyz = xyz.rotate(R, center=(0,0,0))