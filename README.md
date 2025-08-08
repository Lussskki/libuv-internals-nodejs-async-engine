 ## Libuv — Under the Hood with Node.js
  Overview
 - libuv is a multi-platform C library that provides asynchronous I/O capabilities to Node.js.
 - It’s the engine that powers Node’s non-blocking event loop, enabling operations like networking, file I/O, and timers without blocking the main thread.
## Architecture Diagram
```
┌────────────────────────────┐
│  JavaScript (Your Code)    │
└───────────────┬────────────┘
                │ JS bindings (Node C++ layer)
                ▼
┌────────────────────────────┐
│        libuv (C layer)     │
│  - Event Loop              │
│  - Thread Pool             │
│  - TCP/UDP sockets         │
│  - Timers                  │
└───────────────┬────────────┘
                ▼
     OS system calls (epoll, kqueue, IOCP)

```
