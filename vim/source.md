Sourcing a file is 'executing' it. Essentially, each line of the file is considered a command. Sourcing it is the same as typing each command in order. You source with the command **:source**(usually shortened to **:so**)

So if you source myStuff.vim

```:so myStuff.vim```
and if myStuff.vim contained these lines

```
set xx iI just intersted this<C-]>
set yy bbbb4dw
```
Its the same as if you typed those commands into vim

```
:set xx iI just intersted this<C-]>
:set yy bbbb4dw
```
The only file sourced by default is the .vimrc(_vimrc on windows) so that's a place you can keep all the commands you use to set up vim every time.

Where it gets interesting is the fact that since a sourced file is just a series of commands, and sourcing is a command, you can source files from your source files. So pluggins you use every time could be sourced when you start up vim by adding a line to your .vimrc like this

 ```so myPluggin.vim```
