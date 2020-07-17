# Compilando o código fonte

```bash
gcc -o produtor SHMServer.c
gcc -o consumidor SHMClient.c
```
Agora em um terminal execute o programa produtor
```bash
./produtor
```

Em outro terminal execute o programa consumidor
```bash
./consumidor
```