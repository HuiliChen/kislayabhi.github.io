---
layout: post
title: "Writing a MakeFile"
published: true
comments: true
---

Understanding the concept of Libraries is important if you have to deal with C or C++ code on a daily basis. For me, since these days I am working with OpenVX specification and taking the Operating Systems class, it has become an absolute necessity. 

A good place to look at: <http://www.thegeekstuff.com/2010/08/ar-command-examples/>. 
It has good general things that you might want to look up. I will try to build up on his post.

We have two C files

``` addition.c ```

```C
int addition(int x, int y)
{
	return x+y;
}
```

``` multiplication.c ```

```C
int multiplication(int x, int y)
{
	return x*y;
}
```

You must remember that you cannot generate the executables using gcc for any of the two files. gcc complains that it could not find the main() function.

```sh
$ gcc addition.c
(.text+0x20): undefined reference to 'main'
collect2: error: ld returned 1 exit status
```

But what you can do is, just compile it and create the object files. 

```sh
$ gcc -c addition.c
$ gcc -c multiplication.c
$ ls
addition.c addition.o multiplication.c multiplication.o
```

Let's say we define our main() function in the file main.c somewhere else.

```C
#include<stdio.h>
int main()
{   
    int i,j;
    i=5;
    j=6;

    printf("%d \n", addition(i, j));
    printf("%d \n", multiplication(i, j));
}
```

We see that  ``main.c`` has dependency on the ```addition()``` and the ```multiplication()``` function. Since our program is small and 