# CommandLine Arguments

#### Where are Command-line arguments?

Command-line arguments are available to a program in a variable named Args that is part of the os package. thus its name anywhere outside the os package is os.Args.

os.Args is a slice of strings

#### What is Os Package?

The os package provides functions and other values for dealing with the operating system in a platform-independent fashion.

#### How is indexing in Golnag?

As in most other programming languages, all indexing in Go uses **half-open** intervals that include the first index but exclude the last, because it simplifies logic.&#x20;

#### How is slicing in os.Args?

The first element of os.Args, os.Args\[0], is the name of the command its elf; the other elements are the arguments that were presented to the program when it started execution. A slice expression of the form s\[m:n] yields a slice that refers to elements m through n1, so the elements we need for our next example are those in the slice os.Args\[1:len(os.Args)]. If m or n is omitted, it defau lts to 0 or len(s) respectively, so we can abbreviate the desired slice as os.Args\[1:].

#### What is the equivalent for the "assignment statement" `s = s + sep + os.Args[i]`?

&#x20;`s += sep + os.Args[i]`

#### `Write a loop that prints 1 to 10`

The for loop is the only loop statement in Go.

`for initialization; condition; post {`&#x20;

`// zero or more statements`&#x20;

}

so the answer code will be

`for i =0; i < 10; i++ {`&#x20;

`echo i`&#x20;

`}`

#### Which parts in a loop statement can be ignored?

All of them.

#### Write a for loop that iterates over a range of values from a `os.Args`

`for _, arg := range os.Args[1:] {`&#x20;

`echo arg`&#x20;

`}`

range, produces two values: index and value.&#x20;

#### blank identifier

the blank identifier, whose name is \_ (that is, an underscore). The blank identifier may be used whenever syntax requires a variable name but prog ram logic does not, for instance, to discard an unwanted loop index when we require only the element value.&#x20;

Most Go programmers would likely use range and \_ to write the echo program as above, since the indexing over os.Args, is implicit, not explicit, and thus easier to get right.

#### Write 4 methods to declare an empty s string

`s := ""`&#x20;

`var s string`&#x20;

`var s = "" // rarely used`

`var s string = "" // It has redundant parts`

In practice, you should generally use one of the first two forms, with explicit initialization to say that the initial value is important and implicit initialization to say that the initial value doesn’t matter

####





