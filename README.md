# 📺 Retro Terminal: Image to ASCII Converter

<img width="1892" height="1062" alt="Retro Terminal Project" src="https://github.com/user-attachments/assets/f09b90e7-e07b-4146-8d17-348fe2026e22" />

<div align="center">

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

**An immersive web application that transforms images into ASCII art, featuring a realistic CRT monitor simulation.**

[🚀 **Launch Live Terminal**](https://imagetoascii-retro-terminal.netlify.app/)

</div>

---

## Key Features

* **Real-Time ASCII Conversion:** Upload any image and watch it transform into text characters.
* **Dynamic Resolution Control:** Features a slider input to adjust the "pixel" density (font size) from 5px to 20px.
* **High-Fidelity CRT Effect:**
    * **Scanlines:** Animated overlay using linear gradients.
    * **Text Bloom:** Recursive `text-shadow` effects to simulate glowing phosphor.
    * **Screen Flicker:** Complex keyframe animations mimicking voltage instability.
    * **Bezel Overlay:** A retro monitor frame integrated via CSS borders.
* Object-Oriented Design:** Code structured using ES6 Classes (`Cell`, `AsciiEffect`) for maintainability and clean logic.

## Technical Implementation

This project is built with **100% Vanilla JavaScript**—no libraries or frameworks were used, ensuring high performance and a deep understanding of core web technologies.

### The Algorithm
1.  **Image Scanning:** The script draws the uploaded image onto an off-screen canvas to read raw pixel data via `ctx.getImageData()`.
2.  **Grayscale Calculation:** It iterates through the pixel array, calculating the average brightness of each block: $(R + G + B) / 3$.
3.  **Character Mapping:** Based on the brightness value (0-255), a character is assigned from a density string (e.g., `@` for dark, `.` for light).
4.  **Rendering:** The `Cell` class draws each character individually onto the main canvas with specific coordinates.

## 📂 Project Structure

```text
/
├── index.html          # Main DOM structure and CRT container
├── script.js           # Core logic, Canvas API handling, and Event Listeners
├── README.md           # Project documentation
└── assets/
    ├── style.css       # Advanced styling, @keyframes, and responsive design
    ├── images/         # Assets (bezel.jpg, etc.)
    └── fonts/          # Custom retro typography (Apple.ttf / VT323)
```

## 🚀 Local Installation

Since this project has **zero dependencies**, running it is simple:

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/yourusername/retro-ascii-converter.git](https://github.com/yourusername/retro-ascii-converter.git)
    ```

2.  **Navigate to the folder:**

    ```bash
    cd retro-ascii-converter
    ```

3.  **Run it:**
    Simply open `index.html` in your preferred browser (Chrome/Firefox/Edge).


## 📚 References & Inspiration

  * [Coding the Matrix - Image Processing Logic](https://www.youtube.com/watch?v=HeT-5RZgEQY)
  * [Alec Lownes - CRT Display Styles](https://aleclownes.com/2017/02/01/crt-display.html)
