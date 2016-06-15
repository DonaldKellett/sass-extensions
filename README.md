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

There are currently no string functions in this repo.

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

There are currently no list functions in this repo.

### Map Functions

There are currently no map functions in this repo.

### Selector Functions

There are currently no selector functions in this repo.

### Introspection Functions

There are currently no introspection functions in this repo.

### Miscellaneous Functions

There are currently no miscellaneous functions in this repo.
