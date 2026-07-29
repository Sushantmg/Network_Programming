# Network Programming

## Labs

| Lab | Topic | Description |
|-----|-------|-------------|
| 1 | TCP Client-Server | Basic TCP socket programming — one client connects, sends message, server replies |
| 2 | UDP Client-Server | Connectionless UDP socket programming using `sendto` / `recvfrom` |
| 3 | Fork Server | Concurrent TCP server using `fork()` — each client gets a child process |
| 4 | Select Server | I/O multiplexing with `select()` — single process handles multiple clients |
| 5 | Multithread Server | Concurrent TCP server using `pthread` — each client gets a thread |
| 6 | I/O Models | Demonstrates blocking, non-blocking, multiplexing (`select`), and signal-driven I/O |
| 7 | Signal Handling | TCP server that handles `SIGINT` for graceful shutdown |
| 8 | Daemon Process | Creates a background daemon process using `fork` + `setsid` |

## How to Run

Each lab has its own folder with source files. Compile and run:

```bash
cd Lab-<N>
# Compile
gcc server.c -o server    # add -lpthread for Lab-5
gcc client.c -o client
# Run (two terminals)
./server   # terminal 1
./client   # terminal 2
```

For Lab-6, programs are standalone — run directly with `./blocking`, `./nonblocking`, etc.
For Lab-8, run `./daemon` — it forks and exits, leaving a daemon in the background.

## Port

All TCP/UDP labs use port `8080`. Change `#define PORT` in the source files if needed.
