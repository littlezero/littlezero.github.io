# Register in Vim

## What is the register?
Register is a memory space which stores text when you copy something. In OS, we
often use Ctrl+C to copy text. The text is stored in somewhere in memory and
when we Ctrl+V, the OS takes it and pastes. Register does the same thing in
Vim, but it allows you to have multiples spaces to store different texts. Is
that cool?! 

## Now, you don't need to reselect after `d`, `x`, `shift+V`

List of registers
```shell
:reg
```

Copy text to register
```shell
"<any-chracter>y
```

Paste text
```shell
"<any-chracter>p
```

## Special registers

`"%`: has the current path, starting from the directory `vim` was first opened
`":`: has the most recently executed command
`".`: has the last inserted text
`"=`: allows you to execute a expression, then value will be placeed in insert
point. Ex. 2+2=(now, you type Ctrl-r =, then write the expression, then enter)4

## References
- [Vim registers: The basics and beyond](https://www.brianstorti.com/vim-registers/)

- Vim tutor
```
:h registers
```
