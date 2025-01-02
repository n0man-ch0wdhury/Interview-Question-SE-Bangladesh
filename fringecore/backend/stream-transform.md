# Stream Transform Challenge

[Challenge Link](https://tella.video/stream-transform-challenge-1-a5qb)

<aside>
💡 This challenge was solved by one of our engineers internally in ~3 hours. The solution was a single .mjs file, 108 lines long.
</aside>

## Environment Setup

1. **Node.js Version:** Requires Node.js version 20 or higher to run `.mjs` files directly.
2. **Operating System:** Linux is preferred. Windows Subsystem for Linux 2 (WSL2) may also work.


## Challenge Description

1. **Origin Server:** A TCP server (port 3032) provides top-secret information mixed with random data.  It's slow but functional.
2. **Proxy Server (Your Task):** Build a TCP server (port 3031) that connects to the origin server, receives the data, replaces the top-secret information with dashes (`-`), and sends the modified data to clients without waiting for the entire input.


## Details

1. **Single File:**  All code should reside within `challenge.mjs`.  No other files should be modified or created.
2. **No External Libraries:** Do not use any external libraries.
3. **Ports:** Origin server: port 3032; Your proxy server: port 3031.


## Getting Started

1. **Clone the Repository:**
   
    `git clone git@github.com:fringecore/fringecore-backend-challenge-stream-transform.git`
2. **Navigate to Directory:**
   
    `cd fringecore-backend-challenge-stream-transform`
1. **Open in Editor:**  Open the project in your preferred code editor (e.g., VS Code).

2. **Start Origin Server:**
   
    `npm run origin-server`
1. **Start Your Proxy Server:** In a separate terminal tab:
   
   `npm run start`
2. **Run Tests:**
   
    `npm run test`

## Partial Success Milestones

This challenge is difficult.  Consider these milestones as you progress:

1. Challenge started.
2. Connection to the origin server established.
3. Data written to the origin server and output received.
4. Some secret sentences hidden (replaced with dashes).
5. Secret sentences hidden across multiple lines.
6. All secret sentences hidden.


## Submission

1. **Add Remote Repository:** Replace <applicant_id> with your actual ID (case-sensitive).
   
    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-backend-challenge-stream-transform`
1. **Push to Remote:**
   
    `git push fringecore main`
   (You may need to accept the SSH host key fingerprint.)