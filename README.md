<div align="center">

# The Bank — Contactless ATM Interface

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

*Contactless ATM machine software — a virtual on-screen keyboard rendered with OpenCV for touchless PIN entry, designed for public safety.*

</div>

---

## Overview

A computer vision-based virtual keyboard that renders a numeric keypad using OpenCV. Designed as the input interface for a contactless ATM system — users interact with the on-screen keys without physically touching a surface, reducing germ transmission in public ATM machines.

## Architecture

```mermaid
graph TD
    A[OpenCV Canvas<br/>600×600 px] --> B[Virtual Keyboard Renderer]
    B --> C[10-Key Numeric Grid]
    C --> D[Key Detection Logic]
    D --> E[PIN Input Buffer]
    E --> F[ATM Transaction Flow]

    subgraph Keyboard Layout
        C --> G["0-9 keys in 3×4 grid"]
        G --> H[cv2.rectangle per key]
        G --> I[cv2.putText per digit]
    end
```

## How It Works

1. Creates a blank 600×600 NumPy canvas
2. Renders a 3-column numeric keypad using `cv2.rectangle` and `cv2.putText`
3. Each key is positioned on a 200×200 grid with proper text centering
4. Displays the keyboard via `cv2.imshow` for user interaction

## Getting Started

```bash
pip install opencv-python numpy
jupyter notebook "Keyboard OpenCV.ipynb"
```

## Built With

- Python 3 — Core language
- OpenCV — Keyboard rendering and display
- NumPy — Canvas array manipulation

---

<div align="center">

Built by [Akhila Susarla](https://github.com/Akhila-Susarla)

</div>
