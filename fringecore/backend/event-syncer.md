# Event Syncer Challenge

[Challenge Link](https://www.tella.tv/video/collision-course-416j)

<aside>
💡 This challenge was solved internally in ~40 minutes with a 73-line `challenge.mjs` file.
</aside>

## Challenge Description

Build a server that combines aspects of long polling and a queue system for event synchronization.

### Event Life Cycle

*   Events are automatically cleared after 2 minutes.
*   Each event is associated with a specific key.

### Consumption Mechanism

*   Each unique `key` and `groupId` combination defines a consumer group.
*   A consumer group receives *all* unconsumed events for its specific key.
*   Consumed events are marked and not returned again.
*   Only one consumer in a group receives events per request.

### Endpoint Behaviors

1.  `GET /blocking-get?key=meow&groupId=3`:
    *   Waits up to 30 seconds for an event with `key=meow`.
    *   If unconsumed events exist for `key=meow` and `groupId=3`, returns them.
    *   Returns `[]` if no events arrive within 30 seconds.
2.  `POST /push?key=meow`:
    *   Adds a new event to the `meow` event queue.
    *   Doesn't specify the consumer group.
    *   Multiple events can be pushed for a single key.

## Details

1.  **Single File:** Modify only `challenge.mjs`. Do not modify other files.
2.  **No External Libraries:** Do not use external libraries.

## Getting Started

1.  **Clone Repository:**
    

    `git clone git@github.com:fringecore/fringecore-backend-challenge-event-syncer.git`
    
2.  **Navigate to Directory and Install:**
    
    `cd fringecore-backend-challenge-event-syncer`
    `npm install`
    
3.  **Open in Editor:** Open the project in your code editor.
4.  **Start the Server:**
    
    `node index.mjs`

## Partial Success Milestones

This challenge is considered difficult.  These milestones indicate progress:

1.  Challenge started.
2.  `/blocking-get` returns [] after 30 seconds if no events are pushed.
3.  `/blocking-get` receives data immediately after a POST `/push`.
4.  Group-based event consumption implemented.
5.  Event life-cycle management (2-minute timeout) implemented.


## Submission

1.  **Add Remote Repository:** Replace <applicant_id> with your ID (case-sensitive).
    

    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-backend-challenge-event-syncer`
    
2.  **Push to Remote:**
    
    `git push fringecore main`    (You may need to accept the SSH host key fingerprint.)