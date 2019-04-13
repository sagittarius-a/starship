<h3 align="center">Starship ✨🚀</h3>
<p align="center">The cross-shell prompt for astronauts.</p>

---

> ⚠️ This is very much work in progress, so please don't try to use it just yet!

Starship is a Rust port of the minimalistic, powerful, and extremely customizable prompt [Spaceship ZSH](https://github.com/denysdovhan/spaceship-prompt).


## Development plans

The project is beginning as a port of Spaceship ZSH, but will be improved in areas where Spaceship ZSH was previously limited:
- Speed 
    - Concurrency of segment logic execution
    - Memoization of expensive operations
- Safety and error handling
- Testability of code
- Configuration
    - Cross-shell support with JSON or TOML config files

We will _not_ be aiming to achieve full pairity with Spaceship ZSH as a result, so I am very open to discussing and reevaluating new solutions and ideas for the prompt.

I'm very new to Rust, so any help is appreciated when it comes to improving development patterns, writing idiomatic Rust, performance, safety, etc. 😄

### Prompt segments

- [x] Prompt character turns red if the last command exits with non-zero code.
- [x] Current Node.js version(`⬢`).
- [ ] Current Rust version (`𝗥`).
- [ ] Current battery level and status
- [ ] Current Git branch and rich repo status.
- [ ] Indicator for jobs in the background (`✦`).
- [ ] Execution time of the last command if it exceeds the set threshold.

### Other features
- [ ] `.starshiprc` configuration (JSON or TOML)
- [ ] Custom sections given commands or binaries
- [ ] Self-updating

### Shell support

- [x] Fish shell
- [ ] Z Shell
- [ ] Bash

### Test strategy
- [ ] Per-segment benchmarking
- [ ] Per-segment unit + integration tests
- [ ] Shell + OS matrix acceptance tests

## Setup

### Prerequisites

- Rust v1.33 or higher
- Fisher v3

### Getting Started

1. `cd` to the root of the **starship** repo
1. Install the **starship** binary:

    ```bash
    cargo install --path .
    ```

1. Install the fish shell prompt with fisher:

    ```bash
    fisher $PWD
    ```