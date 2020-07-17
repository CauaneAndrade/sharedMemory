# Shared Memory no Linux
memória compartilhada - produtor/consumidor <br>
A memória compartilhada fornece uma maneira de permitir que dois ou mais processos compartilhem um segmento de memória.

Em **SHMServer.c** define-se um identificado *key* exclusivo, que os outros processos que compartilham a memória conhecem.

Em seguida é verificado o retorno de *shmget*, que retorna um identificador do segmento de memória compartilhada shmid, ou -1 em caso de erro. <br>
Após adicionar as letras de 'a' a 'z' verifica se o processo consumidor adicionou '*' para finalizar a comunicação.

Em **SHMClient.c** define-se um identificado *key* exclusivo definido também no processo produtor. <br>
Em seguida lê o que o servidor colocou na memória, por fim adiciona o caracter '*' que o servidor entende como o comando para confirmar o recebimento da mensagem e encerrar o compartilhamento