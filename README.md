# Bake
A Make alternative written entirely in bash

Original idea by [Herberto Graça](https://github.com/hgraca).

## How to use

Copy the `bake` file into your project and make it executable, and run it
```sh
$ chmod a+x bake
$ ./bake
```

This will create a `.recipes` folder where you can add your own `.sh` files if it does not already exist.  
Here you can create (bash) functions, like so
```sh
#!/usr/bin/env bash

bake::recipe::hello-world() ( ## Greet the world
    echo "Hello world!"
)
```

You can add descriptions to your commands by adding them with `## Description` on the same line as the function.

Example output
```sh
Usage: './bake <target> [arg1] [arg2] [...]'
    Available targets:
        hello-world      Greet the world
```

Run your commands like so
```sh
$ ./bake hello-world
Hello world!

real    0m0.001s
user    0m0.000s
sys     0m0.001s
```
