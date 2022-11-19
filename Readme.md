# mkjit
People say C programs need to be compiled before they can be used.

Well, they do. But let's try to hide that fact.

```
$ echo "
    #include <stdio.h>

    void main() {
        printf("Hello, world");
    }
" > hello.c
$
$ mkjit hello
$
$ ./hello
Hello, world
$
$ sed 's/world/earth/g' hello.c > hello.c
$
$ ./hello
Hello, earth
```

Let's make 1970s great again!
