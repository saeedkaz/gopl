# 2. Program Structure

## 2.1. Names

>**What is the rules for namning in go?**

The names in go begin with a letter or underscore and can have many letters, digits & underscores
***
>**What's difference when in entity is declared within a function? What'd visibility boundries?**

When an entity is defined inside a function it't local but when it's definid in a program it can be seen by all function belong to that package.
If the first letter is upper case, it is exporterd and it can be seen by other packages as well.

## 2.2. Declarations

>**How many declations are in go?**

4

var, const, type, func

## 2.3. Variables

>**What is the general form of var decleration?**

```go
var name type = expression
```

### 2.3.1. Short Variable Declarations

>**How to defien a varialbe in Short Variable Declarations mode?**

```go
i  := 0
i, j := 0, 1
```

### 2.3.2. Pointers

>**What is pointer? How can define it? How to update it**
Pointer value is the adress of a variable.

```go
    x := 1
    p := &x // p, of type *int, points to x
    fmt.Println(*p) // "1"
    *p = 2 // equivalent to x = 2
    fmt.Println(x) // "2"
```

>**What is result of this snippet?**

```go
    var x, y int
    fmt.Println(&x == &x, &x == &y, &x == nil)
```

> *Answer*

The zero value for a pointer of any typ e is nil.

The test p != nil is true if p points to a variable.

Pointers are comparable; two pointers are equal if and only if they point to the same
var iable or both are nil.

```go
// "true false false"
```

>**Define a function that return the address of a local variable?**

```go
    var p = f()
    func f() *int {
    v := 1
    return &v
    }
```

>**Define a function that takes the address of a local variable?**

```go
    func incr(p *int) int {
    *p++ // increments what p points to; does not change p
    return *p
    }
    v := 1
    incr(&v) // side effect: v is now 2
    fmt.Println(incr(&v)) // "3" (and v is 3)
```

### 2.3.3. The new Function

>**How can we create a variable by using new function?**
by using new(T), an unnamed variable type T will be created

```go
p := new(int) // p, of type *int, points to an unnamed int variable
fmt.Println(*p) // "0"
*p = 2 // sets the unnamed int to 2
fmt.Println(*p) // "2"
```

>**Why the new function is relatively rarely used?**

Because the most common unnamed variables are of struct types, for which the struct literal syntax is more flexible

### 2.3.4. Lifetime of Variables

>**ٌWhat is the lifetime of package-level and local variables?**
The lifetime of package-level variables is the entire execution of the program.
The lifetime of local variables is dynamic, until it becomes unreachalbe.

## 2.4. Assignments

>**What is assignment? give some examples.**
A value hold by a variable is updated by an assignment.
In the simplest form the variable is on the left of = and an experssion on the right.

```go
x = 1 // named variable
*p = true // indirect variable
person.name = "bob" // struct field
count[x] = count[x] * scale // array or slice or map element
```

>**Write corresponding assignment operator for following assignments?**

```go
        v = v + 1
        v = v - 1
        count[x] = count[x] * scale
```

```go
v++ // v = v + 1 
v-- // v = v - 1
count[x]*=scale // count[x] = count[x] * scale
```

### 2.4.1. Tuple Assignment

>**What is tuple assignment?**

By using tuple assignment we can assigend several varialbe at once.

```go
// computing the n-t h Fibonacci number iteratively
func fib(n int) int {
x, y := 0, 1
for i := 0; i < n; i++ {
x, y = y, x+y
}
return x
}
```

>**How can we use tuple function when call to a function with multiple results, produce several values?**
we use as many variable as function has result.

```go
f, err = os.Open("foo.txt") // function call returns two values
v, ok = m[key] // map lookup
v, ok = x.(T) // type assertion
v, ok = <-ch// channel receive
_, err = io.Copy(dst, src) // discard byte count
_, ok = x.(T) // check type but discard result
```

### 2.4.2. Assignability

>**Is this explicit or implicit?**
> > > `medals := []string{"gold", "silver", "bronze"}?`

This is implicit, because it uses the := operator to infer the type and value of medals from the slice literal.

## 2.5. Type Declarations

**What is type decleration?**  
A type declaration defines a new named ty pe that has the same underlying type as an existing type.  
The named typ e provides a way to sep arate dif ferent and perhaps incompatible uses of the underlying typ e so that they can’t be mixed unintentionally.  
>`type name underlying-type`

## 2.6. Packages and Files

**The source code for a package resides in?**
One or more .go files, usually in a directory whose name ends with the import path;

### 2.6.1. Imports

**Within a Go program, every package is identified by a unique string called waht?**  
 import path.

### 2.6.2. Package Initialization

**What is the used case fo inti function?**  
Each variable declared at package level starts life with the value of its initializer expression, if any, but for some variables, like tables of data, an initializer expression may not be the simplest
way to set its initial value.  
In that case, the init function mechanism may be simpler.

## 2.7. Scope


**Question?**  
**Question?**  
**Question?**  
**Question?**  
**Question?**  
**Question?**  
**Question?**  
**Question?**  
**Question?**  



```go
// Some code
```

```go
package main
fund main() {
    for i=1; i<10{{{{{}}}}

    }
}
```

```go
// Some code
```

>**Question?**

| Question    | Answer |
| -------- | ------- |
| February | $80     |
| |
