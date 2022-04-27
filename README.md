# ex5_os


## Authors

- [@Dolev Dublon, ID: 207867342](https://www.github.com/dolev146)
- [@Yakov Khodorkovsky, ID: 207045063 ](https://www.github.com/yakov103)

 
# Multi-proccess server in c mmap() memeory for shared memory stack allocation and fcntl() for blocking

* The server can handle multiple connections at once.

* we also had to implement a stack that support: 
1) PUSH <txt>
2) POP
3) TOP

* locking mechanisim with fcntl()

* we also had to use understand and use shared memroy with mmap() 


## Run Locally

Clone the project

```bash
  git clone https://github.com/dolev146/ex5_os.git
```

Go to the project directory

```bash
  cd ex5_os
```

Install dependencies

```bash
  sudo apt install ruby
  sudo apt install make
  sudo apt install g++ 
```

Start the server

```bash
  make; ./server
```

and in a diffrent terminal

```bash
  ./client
```



## Running Tests

The first test will test handling multiple clients

first  run the server

```bash
  make clean;make; ./server
```

and in a diffrent terminal run

```bash
  ./clienttest
```

this is testing makeing 150! connections that sending messages and reciving mesesges from the server


press ctrl+c to terminate the server terminal


The second test will be testing the stack implementation for blocking


```bash
  make clean;make; ./server
```

and in a diffrent terminal run

```bash
  ./clienttest2
```

you will see that the size of the stack will be 400 
if you comment out the lines that use fcntl() you may get a smaller number as an affect of not handling correncty about multi-proccessing




  