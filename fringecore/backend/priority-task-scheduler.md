# Priority Task Scheduler Challenge

[Challenge Link](https://www.tella.tv/video/priority-task-scheduler-6lao)

<aside>
💡 This challenge was solved by one of our engineers internally in ~1 hour. The solution was a single .mjs file, 57 lines long.
</aside>

## Environment Setup

1.  **Node.js Version:** Requires Node.js version 20 or higher to run `.mjs` files directly.
2.  **Operating System:** Linux is preferred. Windows Subsystem for Linux 2 (WSL2) may also work.

## Challenge Description

The goal is to modify the `processTask()` function in `challenge.mjs` to handle tasks with priorities, following these rules:

*   **Single Task Processing:** Only one task can be processed at a time.
*   **Task Duration:** Each task must be processed for exactly 5 seconds.
*   **Priority Handling:**
    *   When a higher-priority task arrives, the currently running task must be paused.
    *   The higher-priority task must be processed immediately.
    *   Once the higher-priority task is done, the paused task should resume from where it left off.
*   **Task Management:**  Implement a smooth process to prevent task loss or indefinite delays.

## Details

1.  **Single File:** Work only in the `challenge.mjs` file. Do not modify or create other files.
2.  **No External Libraries:** Do not use any external libraries.
3. **Server:** Use `node server.mjs` to start the server, it will listen on port 42069.

## Getting Started

1.  **Clone Repository:**
 
    `git clone git@github.com:fringecore/fringecore-backend-challenge-priority-task-scheduler.git`

2.  **Navigate to Directory:**    
 
    `cd fringecore-backend-challenge-priority-task-scheduler`

3.  **Open in Editor:** Open the project in your preferred code editor (e.g., VS Code).
4.  **Edit challenge.mjs**
5.  **Start the Server:**    
 
    `node server.mjs`

## Partial Success Milestones

This challenge is recognized as difficult. Consider these milestones as indicators of progress:

1.  Challenge started.
2.  Each task can be processed for 5 seconds.
3.  The response can be sent.

## Submission

1.  **Add Remote Repository:** Replace <applicant_id> with your actual ID (case-sensitive).
 
    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-backend-challenge-priority-task-scheduler`
    
2.  **Push to Remote:**

    `git push fringecore main`    (You may need to accept the SSH host key fingerprint.)