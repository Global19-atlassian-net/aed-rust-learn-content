In this unit your challenge is to fix the missing parts of each exercise's code to make them
compile.

You can use your local development environment or use the Rust Playground to edit the code.

# Exercise 3: Hashmaps

In this exercise you will need to define a basket of fruits in the form of a hash map, where the key
represents the name of the fruit and the value represents how many of that particular fruit is in
the basket.

You have to put at least three different types of fruits (e.g apple, banana, mango) in the basket
and the total count of all the fruits should be at least five.

Keep in mind that you only need to edit the `fruit_basket` function in this exercise.

```rust
use std::collections::HashMap;

fn fruit_basket() -> HashMap<String, u32> {
    let mut basket = ??? ; // TODO: declare your hash map here.

    // Two bananas are already given for you :)
    basket.insert(String::from("banana"), 2);

    // TODO: Put more fruits in your basket here.

    basket
}

fn main() {
    let basket = fruit_basket();
    assert!(
	basket.len() >= 3,
	"basket must have at least three types of fruits"
    );
    assert!(
	basket.values().sum::<u32>() >= 5,
	"basket must have at least five fruits"
    );
}
```

You can run this code in your local computer or use this [Rust Playground link](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=8351e5ee4fc27335e54cdc027383f238).
