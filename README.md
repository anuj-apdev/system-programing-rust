# Learning Linux processes termination in Rust 
 - Cloned/forked Initially from Ivan Vanichuk's [Repo](https://github.com/iximiuz/reapme)

The project covers the following scenarios:

- awaiting a child process termination;
- awaiting a grandchild process termination;
- catching the parent process termination.
- using pipes to communicate between 2 different childs
- using prctl() to make parent or grandparent sub-reaper of (grand)child, if first child process (Parent of grand parent) dies.

Read more about it in Ivan Vanichuk's <a href="https://iximiuz.com/en/posts/dealing-with-processes-termination-in-Linux/">blog</a>.

## Usage
```bash
cargo build

# wait for the child termination
cargo run --bin wait_block

# wait for the child termination while busy looping
cargo run --bin wait_busy

# wait for the child termination signaled to you
cargo run --bin wait_signal

# test Linux CHILD_SUBREAPER feature
cargo run --bin subreaper

# put all things together
cargo run --bin combined
```
