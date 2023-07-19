# 1.3. Finding Duplicate Lines
#### How to create a new empty key/value pairs
```go
counts := make(map[string]int)
```
A map holds a set of key/value pairs and provides constant-time operations to store, retrieve, or test for an item in the set. 

The key may be of any type whose values can compared with ==,strings being the most common example; the value may be of any type at all. 

In this example,the keys are strings and the values are ints. The built-in function make creates a new empty map; it has other uses too.

#### The statement counts[input.Text()]++ is equivalent to?
```go
line := input.Text()
counts[line] = counts[line] + 1
```



#### Write a snippet that reads from the program’s standard input line by line.

The scanner reads from the program’s standard input. Each call to input.Scan() reads the
next line and removes the newline character from the end;

```go
input := bufio.NewScanner(os.Stdin)
```

#### use printf to write series of outputs in lines one integer output and after a tab sring 
```go
fmt.Printf("%d\t%s\n", n, line)
```

#### reads the entire contents of a named file
```go
data, err := ioutil.ReadFile(filename)
```



```