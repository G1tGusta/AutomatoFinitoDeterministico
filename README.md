**Autômato Finito para Cadeias de Comprimento Par sobre {a, b, c}**

Este projeto consiste em um script Python que simula um Autômato Finito Determinístico (AFD) responsável por verificar se uma cadeia formada pelos símbolos a, b e c possui comprimento par.

**Funcionamento**

O programa implementa uma máquina de estados finitos que alterna entre dois estados — par e ímpar — à medida que lê cada caractere da cadeia.
Cada símbolo lido (a, b ou c) faz o autômato alternar seu estado atual:

	Se estava em par, passa para ímpar.
	Se estava em ímpar, retorna para par.

Ao final da leitura, a cadeia é aceita se o autômato terminar em um estado par, indicando que o número total de caracteres é par.

**Alfabeto**

O autômato aceita apenas os símbolos do conjunto:

	Σ = {a, b, c}

Qualquer caractere fora desse alfabeto torna a cadeia inválida e a faz ser rejeitada imediatamente.

**Estados da Máquina**

O autômato utiliza dois estados para representar a paridade do comprimento da cadeia:

q_par (Estado Inicial e de Aceitação):
Representa que a quantidade de símbolos lidos até o momento é par.
Como nenhuma letra foi lida no início, o autômato começa neste estado.

q_impar:
Representa que a quantidade de símbolos lidos até o momento é ímpar.
Sempre que o autômato está neste estado e lê mais um símbolo, ele volta para q_par.

**Lógica de Transição**

As transições entre os estados seguem o seguinte padrão:

	Se o estado atual for q_par e o símbolo lido for a, b ou c, o próximo estado será q_impar.
	Se o estado atual for q_impar e o símbolo lido for a, b ou c, o próximo estado será q_par.

Assim, cada novo símbolo lido alterna o estado entre par e ímpar, sem depender do tipo de letra.

**Estado Inicial e Final**

	Estado Inicial: q_par
	Estado(s) de Aceitação: {q_par}

Isso significa que o autômato aceita qualquer cadeia com quantidade par de caracteres válidos.

**Exemplos de Execução**

	Entrada: ab → 2 letras → par → ACEITA
	Entrada: abc → 3 letras → ímpar → REJEITADA
	Entrada: aabbcc → 6 letras → par → ACEITA
	Entrada: c → 1 letra → ímpar → REJEITADA
	Entrada: abbcaa → 6 letras → par → ACEITA
	Entrada: abx → contém símbolo inválido x → REJEITADA

**Conclusão**

O autômato desenvolvido é uma representação simples e eficiente de um reconhecedor de paridade de comprimento, demonstrando os fundamentos de funcionamento de autômatos finitos determinísticos em Python.
Ele mostra como é possível utilizar estados e transições para analisar cadeias de forma lógica e sistemática.
