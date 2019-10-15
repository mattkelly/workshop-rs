# Storing Multiple Types

`Vec`s can only store items of the same type.

Rust must know the size of `T` at compile time such that it knows how much heap
memory to allocate for each elements.

An intermediate enum can be used to wrap an exhaustive set of types:

```rust
# #[derive(Debug)]
enum SpreadsheetCell {
    Int(i32),
    Float(f64),
    Text(String),
}

let row = vec![
    SpreadsheetCell::Int(3),
    SpreadsheetCell::Text(String::from("blue")),
    SpreadsheetCell::Float(10.12),
];

println!("{:?}", row);
```

If you don't know all the types the vector will hold at runtime, a _trait
object_ can be used instead.
