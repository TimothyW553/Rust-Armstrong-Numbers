# Rust-Armstrong-Numbers
CCEXTRACTOR DEVELOPMENT - Rust: Armstrong Numbers

Try it out here!
https://repl.it/@TimothyW553/Armstrong-Numbers

```Rust
use std::io;

pub fn is_armstrong_number(num: u32) -> bool {
    let len = ((num + 1) as f32).log10().ceil() as u32;
    let number_as_string = num.to_string();
    let armstrong: u32 = number_as_string.chars().map(|digit| digit.to_digit(10).unwrap()).map(|digit| digit.pow(len)).sum();
    armstrong == num
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let n: u32 = input.trim().parse().unwrap();
    println!("{}", is_armstrong_number(n));
}
```
