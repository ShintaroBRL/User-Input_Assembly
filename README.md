# User-Input_Assembly
Entrada de usuário em assembly

# Variaveis
```
section .bss
   num resb 5
```

# Função start
```
section .text
   global _start
```

# Variaveis Fixas
```
section .data                          
   userMsg db 'Please enter a number: '
   lenUserMsg equ $-userMsg
   dispMsg db 'You have entered: '
   lenDispMsg equ $-dispMsg  
```

# Exibe a mensagem: userMsg quem tem lenUserMsg de tamanho
```
  mov eax, 4
  mov ebx, 1
  mov ecx, userMsg
  mov edx, lenUserMsg
  int 80h
```

# Le e armazena a entrada do usuario
```
  mov eax, 3
  mov ebx, 2
  mov ecx, num  
  mov edx, 5
  int 80h
```

# Finaliza o programa
```
   mov eax, 1
   mov ebx, 0
   int 80h
```
