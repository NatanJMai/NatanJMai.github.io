*O que é um sistema de tempo real?*
Uma rápida introdução sobre sistemas operacionais de tempo real (real-time operating systems) 

**1.** O que é.
**2.** Escalonamento
**3.** Comunicação entre processos (IPC)

-----------------

**O que é.**

Um modelo de sistema onde é necessário conhecer e controlar o tempo
de cada tarefa (task). Basicamente existem dois tipos de sistemas
tempo real, são eles: *Hard* e *Soft*.

A diferença entre eles é basicamente o nível da consequência
caso algum erro do sistema ocorra. Um erro do sistema de uma aeronave 
é muito mais crítico do que um erro de um sistema de multimídia por exemplo. Esse é
um exemplo clássico que descreve bem a diferença entre ambos. Veja que o erro pode ser
tanto uma escolha errada, um processamento errado, uma falha de escalonamento ou qualquer
outra coisa.

-----------------

**Escalonamento de processos**
	A tarefa do escalonador é justamente encontrar o próximo 	 processo apto a ser executado. Existem diversos métodos de 	implementação para essa tarefa, alguns com preempção, 		outros com prioridades, etc.

**Comunicação entre processos (IPC)**
	Existe a necessidade de comunicação e troca de informações entre processos durante a execução. Esse procedimento é também conhecido como Comunicação entre processos (inter process communication).
    Aqui estão alguns dos principais métodos de IPC:
    
* Message queue.
* Mailbox.
* Pipe.
* Memória compartilhada.

A partir dessas informações, estou estudando principalmente os métodos de comunicação e fazendo a comparação entre eles. 
    
Até mais :)