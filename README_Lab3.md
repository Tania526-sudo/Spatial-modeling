# Lab 3: Fractal Modeling in Spatial Systems

This lab explores **fractal structures** using recursive and iterative methods, highlighting their application in **spatial modeling** and **natural pattern simulation**.

---

## Objectives

- Implement recursive generation of the **Sierpinski triangle**
- Visualize fractals using `matplotlib`
- Study properties of **self-similarity** and **recursive transformations**
- Understand how fractals can model **natural and infrastructure forms**
## Key Concepts

- **Fractal Geometry**
- **Recursive Algorithms**
- **Affine Transformations**
- **Spatial Resolution & Depth Levels**

---

## Examples

### Sierpinski Triangle (Recursive)
```python
def sierpinski(x, y, size, depth):
    if depth == 0:
        draw_triangle(x, y, size)
    else:
        new_size = size / 2
        sierpinski(x, y, new_size, depth - 1)
        sierpinski(x + new_size, y, new_size, depth - 1)
        sierpinski(x + new_size / 2, y + new_size * (3**0.5)/2, new_size, depth - 1)