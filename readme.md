## Compilation Lifecycle
- Preprocess: ```g++ -E```
  - Macro substitution
  - Stripping comments
  - File inclusion
- Compilation: ```g++ -S```
  - Input: C++; Output: assembly code
- Assembly: ```g++ -c```
  - Input: assembly code
  - Output: binary code (.o file)
- Linking: ```g++ -o```
  - Input: object file (.o)
  - Output: executable file (.exe)
  - Symbol resolution
  - Relocation

## Compiling Seperately
```
// compile main.cc and generate main.o
g++ -c -Wall main.cc -o main.o

// compile insert.cc and generate insert.o
g++ -c -Wall insert.cc -o insert.o

// compile search.cc and generate search.o
g++ -c -Wall search.cc -o search.o

// generate bs_tree.o from above .o files
g++ main.o insert.o search.o -o bs_tree.o

// clean
rm *.o bs_tree
```

## Shortcut
```
// Compiling Seperately is more useful when debugging
// but compliation can be done all at the same time
g++ -c main.cc insert.cc search.cc -o bs_tree.o
```

## Checking Version
```g++ --version```