# Color Picker Pentagon Challenge

[Challenge Link](https://www.tella.tv/video/color-picker-pentagon-1-3p7x)

> Note: This challenge was solved internally in ~45 minutes with a 50-line kernel function.


## Challenge Description

Build a GPU-accelerated color picker with a pentagon shape.  You'll implement the color computation kernel using GPU.js; the React UI is provided.

**Core Requirements:**

*  Implement a kernel function (`kernelFunction` in `kernel.js`) to generate a color picker gradient.
*   Handle hue transitions across the color spectrum (0-360 degrees).
*   Create horizontal gradients (white to primary color).
*   Apply vertical gradients (white to black).

**Color Computation Features:**

*   RGB calculations based on hue.
*   Smooth transitions between primary colors.
*   Correct alpha channel handling (likely fully opaque).
*   Pixel-perfect gradient rendering.


## Your Task: Implement `kernelFunction`

The `kernelFunction` in `kernel.js` should:

1.  Take `width`, `height`, and `hue` (0-1) as input.
2.  Compute RGB values for each pixel.
3.  Handle color transitions and gradients.
4.  Return the correct RGBA channel values based on thread position.


## Getting Started

1.  **Clone Repository:**
    
    `git clone git@github.com:fringecore/fringecore-frontend-challenge-colorpicker-pentagon.git`
    
2.  **Navigate to Directory:**    
 
    `cd fringecore-frontend-challenge-colorpicker-pentagon`
    
3.  **Install Dependencies:**    
 
    `npm install`

4.  **Run Development Server:**    
 
    `npm run dev`

## Evaluation Points

*   Basic color computation.
*   Correct hue transitions.
*   Proper gradient implementation.
*   Performance optimization (GPU utilization).
*   **Bonus Features:** Smooth color interpolation, custom gradient patterns, further performance optimizations.


## Best Practices

*   Efficient GPU-friendly computations.
*   Normalized values (0-1) for calculations.
*   Proper handling of edge cases.
*   Clean, well-organized code.


## Submission

1.  **Add Remote Repository:** Replace <applicant_id> with your actual ID (case-sensitive).
    
    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-frontend-challenge-colorpicker-pentagon`

2.  **Push to Remote:**    
 
    `git push fringecore main`    (You may need to accept the SSH host key fingerprint.)