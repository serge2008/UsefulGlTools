# Vectors in Custom GL

Vectors are one of the foundational concepts in 3D graphics programming. They are used to represent points in space, directions, velocities, and more. In a custom graphics library, vectors are essential for transformations, camera handling, lighting calculations, and more.

---

## Overview

This section provides the basic operations on vectors that are needed to manipulate objects and perform various mathematical calculations in the rendering pipeline. A vector is simply an array of numbers, typically representing a direction or position in space. These operations are key to how objects are transformed and manipulated in 3D space.

---

## Vector Operations

### Vector Addition
Adding two vectors is performed component-wise. For example, if you have two vectors:
- \( \mathbf{A} = [a_1, a_2, a_3] \)
- \( \mathbf{B} = [b_1, b_2, b_3] \)

The result of adding these vectors is:
- \( \mathbf{A} + \mathbf{B} = [a_1 + b_1, a_2 + b_2, a_3 + b_3] \)

### Vector Subtraction
Vector subtraction is similar to addition, but each component of the vectors is subtracted:
- \( \mathbf{A} - \mathbf{B} = [a_1 - b_1, a_2 - b_2, a_3 - b_3] \)

### Dot Product
The dot product of two vectors \( \mathbf{A} \) and \( \mathbf{B} \) is calculated as:
- \( \mathbf{A} \cdot \mathbf{B} = a_1b_1 + a_2b_2 + a_3b_3 \)

This operation results in a scalar value, which has various uses in lighting calculations, projections, and calculating angles between vectors.

### Cross Product
The cross product of two vectors \( \mathbf{A} \) and \( \mathbf{B} \) gives a new vector that is perpendicular to both:
- \( \mathbf{A} \times \mathbf{B} = [a_2b_3 - a_3b_2, a_3b_1 - a_1b_3, a_1b_2 - a_2b_1] \)

This operation is crucial for computing normals, especially in lighting and surface interaction.

### Normalization
Normalizing a vector means converting it to unit length, which is useful for direction-based calculations. The normalized vector is:
- \( \hat{\mathbf{A}} = \frac{\mathbf{A}}{\|\mathbf{A}\|} \)

Where \( \|\mathbf{A}\| \) is the magnitude of the vector.

---

## Example Code

Here are the basic operations for vectors in C:

- **Vector addition**:
    ```c
    typedef struct {
        float x, y, z;
    } Vector3;

    Vector3 addVectors(Vector3 a, Vector3 b) {
        return (Vector3){a.x + b.x, a.y + b.y, a.z + b.z};
    }
    ```

- **Dot product**:
    ```c
    float dotProduct(Vector3 a, Vector3 b) {
        return a.x * b.x + a.y * b.y + a.z * b.z;
    }
    ```

- **Cross product**:
    ```c
    Vector3 crossProduct(Vector3 a, Vector3 b) {
        return (Vector3){
            a.y * b.z - a.z * b.y,
            a.z * b.x - a.x * b.z,
            a.x * b.y - a.y * b.x
        };
    }
    ```

---

## Conclusion

Understanding vectors and their operations is crucial for building a custom graphics library. These operations are used in nearly every part of 3D graphics, from transformations to camera manipulation to lighting and shading.

The provided code examples can be directly integrated into your project as part of the foundational math utilities.
