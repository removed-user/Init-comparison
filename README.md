
| Repo Name (Author/Project) | Project Type | Core Architecture & Primary Purpose |
| :--- | :--- | :--- |
| **Yelp/dumb-init** | Container Micro-Init | Acts as PID 1, forks the target application to PID 2, and focuses strictly on signal proxying and reaping zombies. |
| **krallin/tini** | Container Micro-Init | A transparent micro-init (Docker's native choice) that handles `waitpid` and forks/reaps an entry application with minimal overhead. |
| **suckless/sinit** | Bare-Metal Minimalist Init | Under 100 lines of pure C. Forks a single startup file (like an rc script) to spawn the rest of the system while handling basic hardware/reboot signals. |
| **nshp/sinit** | Bare-Metal Fork | A variation of the suckless init that shifts configurations natively into compiled C headers to fork hardcoded services directly. |
| **angt/slashinit** | Initramfs Bootstrapper | Designed to handle initial RAM filesystems, setting up minimal hardware mounts before forking into the primary system supervisor. |
| **arachsys/init** | Modular BSD-Style Init Toolkit | Uses a minimal `reap` utility to explicitly ignore `SIGCHLD` so the kernel automatically discards dead processes, alongside a specialized `daemon` utility to orchestrate parallel forking and dependency waiting. |
