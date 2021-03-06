# sass-extensions

Adds core functionality that Sass painfully lacks.  Public Domain

## Repo Details

- Current Version: None
- Status: In Development but always ready for production
- License: **Public Domain** (feel free to do whatever with it :smile:)

## Initialization

Simply include the following line of code in your main Sass file(s) to get started:

```scss
@include "path/to/your/extensions";
```

## Contributing

[![Join the chat at https://gitter.im/DonaldKellett/sass-extensions](https://badges.gitter.im/DonaldKellett/sass-extensions.svg)](https://gitter.im/DonaldKellett/sass-extensions?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Contributions are more than welcome in this repo.  Feel free to contribute in the following ways:

 - Create an issue
 - Start a pull request
 - Leave a message on the Gitter Channel (click on the badge below)

If:

 - You would like a new core functionality to be implemented that is not currently supported (by either creating an issue (label as "Suggestion" please :smile:) or leaving a message on the Gitter Channel)
 - You have successfully implemented a new core functionality yourself (make sure to test it thoroughly :wink:) and would like it to be included in this repo (start a pull request and I will merge it if appropriate)

Regarding the Gitter channel, apart from contributions, questions are also always welcome.  Please note that severely off-topic, offensive or profane comments will be deleted (and the user(s) reported) but semi-off-topic comments (e.g. comments regarding Sass as a whole or other programming concepts not strictly related to Sass) are also welcome :smile:

### Help Needed!

[Donald Sebastian Leung](https://github.com/DonaldKellett) would like your help in implementing the following core functions:

#### Lexicographical Sort

Since [Donald Sebastian Leung](https://github.com/DonaldKellett) is unable to implement a lexicographical (alphabetical) sort (he does not know how to implement the correct algorithm for a lexicographical sort), he would like your help in implementing this core functionality.  If you have successfully implemented an algorithm for this function and **have tested it thoroughly against a set of test cases**, feel free to start a pull request.  I will then test the algorithm myself and if the algorithm works properly for a wide range of cases then I will merge the pull request and **your contribution will be officially recognised by GitHub** :smile:.

## Documentation

### Built-in Sass Functions (Reference Link)

To view the entire list of functions that are natively available in Sass, please refer to [this link](http://sass-lang.com/documentation/Sass/Script/Functions.html).

### Compass Helper Functions (Reference Link)

Additionally, [Compass](http://compass-style.org), which is quite frequently used as a Sass extension, also comes with a bunch of [handy helper functions](http://compass-style.org/reference/compass/helpers/) so I won't be implementing them here.

### RGB Functions

There are currently no RGB functions in this repo.

### HSL Functions

There are currently no HSL functions in this repo.

### Opacity Functions

There are currently no opacity functions in this repo.

### Other Color Functions

There are currently no color functions in this repo.

### String Functions

#### str-to-char-list

```scss
str-to-char-list($string);
```

Converts a string into a list of characters, separated by comma delimiters.  Works for all strings of all lengths; however, *please note that if the string is empty then an empty string is returned* because an empty list is not considered a valid CSS value.

#### repeat-str

```scss
repeat-str($string, $count);
```

Repeats a string over `$count` times and returns a new **string** (not a list!).  Similar to repeating strings in Ruby by the multiplication operator (`*`) but please note that *the order of the arguments matter - the string must be passed in first and the repeat count second*.  `$string` can be any valid string and `$count` any valid natural number (i.e. positive integer).

### Number Functions

#### round-to

```scss
round-to($number, $precision);
```

Rounds a given number to a specified number of decimal places.  Behaves properly for:

- Any `$number` that is a valid number *with no units*
- Any integer value of `$precision` (can be positive or negative)

Both arguments are required as otherwise, `round` alone can save you some typing :wink:

#### trunc

```scss
trunc($number);
```

Truncates a given number (i.e. removes all decimal places, showing only the integer part).  Works for all numbers *with no units*.

#### exp

```scss
exp($x);
```

Calculates e^x for all values of `$x`.  Works for all valid numbers *with no units*.

#### rand-int

```scss
rand-int([$min, $max]);
```

Returns a random integer in the range specified.  Works properly only when both `$min` and `$max` are integers **and** `$min < $max`.

`$min` and `$max` are optional; if not specified `$min` defaults to `0` and `$max` defaults to `100`.

### List Functions

#### list-join

```scss
list-join($list, $separator);
```

Joins all the elements in a list into a string with the provided `$separator` in between.  Similar to the built-in `implode` function in PHP except the arguments are in the opposite order (in `list-join`, `$list` goes first before the `$separator`).  `$list` may be any valid list and `$separator` any valid string.

#### list-map

```scss
list-map($list, $fn);
```

Expects a list `$list` to be mapped as its first argument and a function `$fn` as its second argument which is used to map the list.  Returns a new list with its elements mapped according to the function provided.  Similar to `Array.prototype.map` in Javascript, `Array#map` in Ruby and `array_map` in PHP.

#### list-reduce

```scss
list-reduce($list, $fn[, $init]);
```

Expects two arguments, a `$list` to iterate through and a `$fn` to be called.  The third argument `$init` (the initial value before reducing) is optional but best practice is to provide it.  `list-reduce` iterates through the list, reducing values and returning a value, list or map, depending on the function passed into `list-reduce`.  Behaves very similarly to `Array.prototype.reduce` in Javascript and `array_reduce` in PHP except **no** third argument (the current index) is passed into your function.

#### bubblesort

```scss
bubblesort($list);
```

Expects a **numerical list** `$list` as its only argument and returns a new list without altering the original list using the **Bubblesort Algorithm**.  Please note that all items in the list must be **valid numbers** *with no units*.

*N.B. The bubblesort function may work with numbers with units (e.g. `px`, `em`) provided that the units are consistent; however, this has NOT been tested yet so please do not expect it to work properly in such cases.*

#### list-reverse

```scss
list-reverse($list);
```

Accepts a list and returns a new list with the order of the elements reversed.

### Map Functions

There are currently no map functions in this repo.

### Selector Functions

There are currently no selector functions in this repo.

### Introspection Functions

There are currently no introspection functions in this repo.

### Miscellaneous Functions

There are currently no miscellaneous functions in this repo.
