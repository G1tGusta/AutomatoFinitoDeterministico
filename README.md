NOMES: Gustavo Lucas Santos Silva e Kauã de Sousa Franco da Costa

ATIVIDADE 10:
Cadeias com uma quantidade par de símbolos. {ε, bb, ac, aabc, abac, abbc, abcc, acac, acbc, aaaacb, bababc, ... } Sigma = {a,b,c} S -> XXS X -> a X -> b X -> c S -> ε ((a|b|c)(a|b|c))*

O código implementa um Autômato Finito Determinístico (AFD) com o propósito exclusivo de verificar se a cadeia de entrada, composta pelos símbolos {a,b,c}, possui comprimento par. Esse autômato opera com dois estados, "q_par" e "q_impar". A lógica de transição é simples: a leitura de qualquer símbolo (a,b ou c) faz o autômato alterar entre "q_par" e "q_impar", que no final da cadeia a função "automato" retorna TRUE se o estado final "q_par", confirmando que a cadeia tem um número par de símbolos, e FALSE caso contrário.
