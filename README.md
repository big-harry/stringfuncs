# StringFuncs
String tools that I often use
# Installation
```sh
go get github.com/big-harry/stringfuncs@latest
```
# Purpose
I usually use different versions so it's nice to have a library with minimal dependencies

# Usage
## Searching functions
* `In()`            -   Gets the location of a rune in a string, returns -1 if not found
```go
In("Foo", 'F')
// Returns 0
```
* `In_string()`     -   Gets the location of a string in a string array, returns -1 if not found
```go
LookingIn := []string{"Foo", "bar"} // Create an array with 2 items
In_string(LookingIn, "bar")
// Returns 1
```
* `In_int()`        -   Gets the location of an int in an int array, returns -1 if not found
```go
LookingIn := []int{0, 1, 2, 3}  // Create an array with 4 items
In_int(LookingIn, 2)
// Returns 2
```

## Usage functions
* `Usage()`         -   Gets the count of runes in a string
```go
Usage("Foobar", 'o')
// Returns 2
```
* `Usage_string()`  -   Gets the count of strings in a string array
```go
LookingIn := []string{"Foo", "bar"} // Create an array with 2 items
Usage_string(LookingIn, "Foo")
// Returns 1
```

## Finding functions
* `Find()`          -   Gets the index of a rune in a string, returns -1 if not found
```go
Find("Foobar", 'o', 2)  // Gets the second occurence of 'o'
// Returns 2
```
* `Contains()`      -   Sees if a string is in another string
```go
Contains("Foobar", "Foo")
// Returns true
```

## Outlier functions
* `Outlier()`       -   Gets count of characters not in a source array
```go
Outliers("Fooba", "Foobar")
// Returns 1
Outliers("Foba", "Foobar")
// Returns 1
Outliers("Foobar", "Foo")
// Returns 0
```

## String changing functions
* `RemoveSpace()`   -   Removes all spaces in a string
```go
RemoveSpace("Foo  bar")
// Returns "Foobar"
```
* `StripSpace()`    -   Removes all whitespace in a string
```go
StripSpace("Foobar\n\n\n")
// Returns "Foobar"
```
* `Split()`         -   Splits a string by another string, returns string array
```go
Split("Foobar", "oo")
// Returns []string{"F", "bar"}
```

## Number checking functions
* `IsInt()`         -   Checks if a string is also an int
```go
IsInt("0123")
// Returns true
```
* `IsFloat()`       -   Checks if a string is also a float
```go
IsFloat("0123.45")
// Returns true
```

## Misc.
* `Flatten()`       -   Coverts a string array into a string
```go
Source := []string{"A", "B", "C"}
Flatten(Source)
// Returns "ABC"
```
