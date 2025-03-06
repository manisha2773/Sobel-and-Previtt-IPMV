# EXP5 Sobel-and-Previtt-IPMV
Sobel Operator

It is named after Irwin Sobel and Gary Feldman. Like the Prewitt operator Sobel operator is also used to detect two kinds of edges in an image:
Vertical direction
Horizontal direction
The difference between Sobel and Prewitt Operator is that in Sobel operator the coefficients of masks are adjustable according to our requirement provided they follow all properties of derivative masks.
Sobel-X Operator = [-1 0 1; -2 0 2; -1 0 1]
Sobel-Y Operator = [-1 -2 -1; 0 0 0; 1 2 1]


Prewitt Operator

The Prewitt operator was developed by Judith M. S. Prewitt. Prewitt operator is used for edge detection in an image. Prewitt operator detects both types of edges, these are:
Horizontal edges or along the x-axis,
Vertical Edges or along the y-axis.
Wherever there is a sudden change in pixel intensities, an edge is detected by the mask. Since the edge is defined as the change in pixel intensities, it can be calculated by using differentiation. Prewitt mask is a first-order derivative mask. In the graph representation of Prewitt-mask’s result, the edge is represented by the local maxima or local minima.
Both the first and second derivative masks follow these three properties:
More weight means more edge detection.
The opposite sign should be present in the mask. (+ and -)
The Sum of the mask values must be equal to zero.
Prewitt operator provides us two masks one for detecting edges in the horizontal direction and another for detecting edges in a vertical direction.
Prewitt Operator [X-axis] = [ -1 0 1; -1 0 1; -1 0 1]
Prewitt Operator [Y-axis] = [-1 -1 -1; 0 0 0; 1 1 1]

EXP 5A Sobel

This code applies the Sobel operator to detect edges in a grayscale image. It first loads the image, then computes the gradients in the x and y directions using the Sobel operator with a 3x3 kernel. The magnitude of the gradients is calculated using the Pythagorean theorem. The result is converted to an 8-bit image for visualization. Finally, the original image, Sobel edge magnitude, and Sobel gradients in the x-direction are displayed using Matplotlib. The output shows the original image, edge detection result (magnitude), and edge detection in the x-direction, highlighting edges and transitions in intensity.

EXP 5B Prewitt

This code applies the Prewitt operator to detect edges in a grayscale image. It loads the image using OpenCV and defines two Prewitt kernels for detecting edges in the x and y directions. The cv2.filter2D function convolves the image with these kernels to compute the gradients in both directions. The magnitude of the gradient is calculated using the Pythagorean theorem. The result is converted to an 8-bit image for visualization. Finally, it displays three images using Matplotlib: the original image, the magnitude of the Prewitt edge detection, and the gradient in the x-direction.
