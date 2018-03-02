### Counting Sort in Chapel  


#### Algorithm
-> Create N buckets where N is 1 greater than the range of elements in the array. <br/>
-> Traverse the input list and increment the counter in the bucket each time we come across a value. <br/>
-> In the end, each bucket's index is the number from the input array, and its count indicates, how many times it has appeared. <br/>
-> Again traverse from left to right, output the index of the element, output it the number of times same as its count,decrease its count, and
repeat for other elements until counter for all is 0.

```chapel
writeln("Input range of numbers:");
var range = read(int);
writeln("Input array size");
var size = read(int);
var arraylist:[0..size-1]; //0 based indexing
writeln("EInput array elements");

var i = 0;
while i<size {
    arraylist[i] = read(int);
    i = i+1;
}

//print input array 
i=0;
while i<size {
    writeln(arraylist[i]);
    i = i + 1;
}

i=0;
var tempArr:[0..range];
while i<size {
    tempArr[arraylist[i]]=tempArr[Arr[i]]+1;
    i = i + 1;
}
//print sorted array
i=0;
while i<range{
    while(tempArr[i]!=0){
        writeln(i);
        tempArr[i]=tempArr[i]-1;
    }
    i = i + 1;
}
```
