## 100 days of Chapel
We have created this repository to learn chapel. Each day, we will be posting code snippets of whatever progress we have made on that particular day.

### Day 1

#### Declaring Variables
In chapel, like other programming languages(Javascript,C++), variable declaration is explicit. The type of variable declared however, is not specified. We can directly create the type of variable we want.
Also, the type of variable is static and is inferred in compile time which means we cannot change the type of variable at any other state.

```chapel
var name = "Alice";
var age = "12";
var height = "136.66"
```

#### Comments

```chapel
/* multiline
line 1
*/
// single line
```

#### Input/Output from the console
The type of variable being input needs to be specified.

```chapel
write("Hello World!!!")
writeln("Hello World!!!") //writes to new line
var name = read(string);
var age = read(int);
```

#### Boolean Variables

```chapel 
var boolvar = true;
var boolvar = false;
```

#### If/Else conditional statements

```chapel
var num = read(int);

if num%2==0 {
writeln("This is an even number");
} else {
writeln("This is an odd number");
}
```

#### Switch Case

```chapel
writeln(Colours and symbols);
var colour = read(string);
 
select(colour){
when "Saffron" {
writeln("Symbol for courage and strength");
}
when "White"{
writeln("Peace");
}

when "Green"{
writeln("Fertility");
}

when "Purple"{
writeln("Royalty");
}

when "Yellow"{
writeln("Happiness");
}

}
```

#### Ranges

```chapel
var ran1 = 199..599; //outputs numbers to 199-599
var ran2 = 1000..400; //outputs numbers 1000-400
```

#### Loops

```chapel
for i in 1000..1{
  writeln(i);
}

//while
var num = 1;  // while loop
while num<100 {
    num += 5;
    if num>50{
    writeln('Num greater than 50');
    }
    writeln(num);
}

num = 0;      // do-while loop
do {
    num += 25;
    writeln(num);
} while(i<10000);

````

#### Lists / Arrays
In chapel , we dont have lists like python, instead we have arrays. Another interesting concept is that of domains. A domain defines a set of indices. With this we can define whether we want 
a 1-based or 0-based indexing. We can see the use of arrays and domains in the example below. Here we have used 0-9, hence this is 0 based indexing.

``` chapel
var newlist: [0..9, 0..9] real;

//Element wise iteration
for item in newlist {          
    writeln(item);
}
// Iteration using indexes
for (i, j) in newlist.domain {
    writeln("(",i,",",j,") = ",newlist[i,j]);
}
```

#### Classes and Objects
```chapel
class Rainbow {
    var color1: string;
    var color2: string;
    var color3: string;
    var color4: string;
    var color5: string;
    var color6: string;
    var color7: string;
    
    proc Rainbow(color1: string,color2: string,color3: string,color4: string,color5: string,color6: string,color7: string) {
        this.color1 = color;
        this.color2 = color;
        this.color3 = color;
        this.color4 = color;
        this.color5 = color;
        this.color6 = color;
        this.color7 = color;
    }
}
var rainBow = new Rainbow("Violet","Indigo","Blue","Green","Yellow","Orange","Red");
writeln(rainBow.color1,rainBow.color2,rainBow.color3,rainBow.color4,rainBow.color5,rainBow.color6,rainBow.color7);
```






