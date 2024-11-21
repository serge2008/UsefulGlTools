# Useful Math for Custom GL

This section provides the mathematical foundations required to build your own custom graphics library (GL). The core concepts here include vectors, matrices, transformations, and quaternions—critical components for implementing a 3D rendering pipeline.

---

## Overview

The **UsefulMaths** folder includes implementations and explanations of essential math operations that form the backbone of graphics programming. These are the building blocks used to handle geometric transformations, 3D object manipulation, and efficient rendering.

---

## Contents

### 1. [Vectors](Vectors/README.MD)
- **Vector Basics**: Introduction to vectors, their operations (addition, subtraction), and their use in 3D graphics.
- **Dot Product**: How the dot product is used for calculating angles, lighting, and more.
- **Cross Product**: The cross product, its geometrical meaning, and use for computing normals.
- **Normalization**: Converting a vector to unit length, used in normalization of direction vectors.

### 2. Matrices
- **Matrix Representation**: Understanding matrices as 2D arrays and their application in transformations.
- **Transformation Matrices**: How to build matrices for translating, rotating, and scaling objects in 3D space.
- **Projection Matrices**: Explanation of perspective projection, orthographic projection, and how they are used to simulate 3D depth on a 2D screen.
- **View Matrices**: Setting up camera transformations, handling the position and orientation of the viewer.

### 3. Transformations
- **Translation**: Moving objects in 3D space using translation matrices.
- **Rotation**: How rotation matrices or quaternions are used to rotate objects around axes.
- **Scaling**: Scaling objects uniformly or non-uniformly in 3D.

### 4. Quaternions
- **Quaternion Basics**: Introduction to quaternions as an alternative to Euler angles for smooth rotations.
- **Quaternion Operations**: How to perform basic operations like multiplication and inverse with quaternions.
- **Rotation with Quaternions**: Applying quaternions for efficient and stable rotations in 3D graphics.
- **Quaternion vs. Euler Angles**: A comparison of both methods for rotating objects, highlighting the advantages of quaternions.

---

## Example Code and Implementations

1. **Vector Operations:**
   - Code for vector addition, dot product, and cross product.
   - Sample code to normalize vectors.

2. **Matrix Operations:**
   - Code for creating translation, rotation, and scaling matrices.
   - Sample implementation of projection and view matrices.

3. **Quaternion Rotation:**
   - Example code showing how to rotate an object using quaternions.

---

## Usage

To use the math utilities in your custom GL library, include the appropriate files from this folder into your project. You can then call functions for vectors, matrices, or quaternions to handle the mathematical operations required for your 3D rendering.

For example, to apply a translation to an object, use the provided transformation matrix functions to modify the object's position in space.

---

## Next Steps

Once you are familiar with the math in this section, you can start integrating these concepts into your custom graphics pipeline. These building blocks will help you implement features like object manipulation, camera control, and scene rendering.

---

Feel free to check the specific files in the **UsefulMaths** folder for detailed implementations, or refer to the main project `README.md` for further guidance.
