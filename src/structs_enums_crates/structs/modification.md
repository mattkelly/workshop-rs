# Modification

Both C and Rust have very similar ways of modifying struct members:

```c
sContext context = {
    .name = "Context",
    .path = "/home/context",
    .entries = 0,
    .is_busy = false,
};

context.path = "/var/context";
```

```rust,ignore
let mut context = Context {
    name: String::from("Context"),
    path: String::from("/home/context"),
    entries: 0,
    is_busy: false,
};

context.path = String::from("/var/context");
```
