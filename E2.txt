import numpy as np

def swap(coords: np.ndarray):
    # Create a copy to avoid in-place modifications
    swapped_coords = coords.copy()
    
    # Swap the coordinates
    swapped_coords[:, [0, 1]] = coords[:, [1, 0]]  # Swap x1 and y1
    swapped_coords[:, [2, 3]] = coords[:, [3, 2]]  # Swap x2 and y2
    
    return swapped_coords

# Test the function with the provided example
coords = np.array([[10, 5, 15, 6, 0],
                   [11, 3, 13, 6, 0],
                   [5, 3, 13, 6, 1],
                   [4, 4, 13, 6, 1],
                   [6, 5, 13, 16, 1]])
swapped_coords = swap(coords)
print(swapped_coords)
