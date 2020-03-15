# Breadth-First-Search
 Análise e desenvolvimento do algoritmo BFS
 Por Pedro Sacramento Xavier Barreto Rosa
 Através do

 Grupo Turing

 Breadth-First-Search
 14 de Março de 2020
 ________________________________________
 Resumo: BFS é um algoritmo para atravessar um *gráfico*, uma estrutura de dados que conecta nódulos entre si e permite uma abordagem diferente daquela tradicional às listas. A característica definitiva desse algoritmo é que ele visita todos os nódulos vizinhos ao primeiro que são equidistantes, ou seja:


 nesse caso, o algoritmo deve, partindo do nódulo preto, visitar primeiro aqueles em amarelo, então os em vermelho, terminando com o verde seguido do azul.

 O algoritmo escrito abaixo na sua versão iterativa como pseudo-código, tradicionalmente funciona se valendo de uma "queue", que difere do "stack" - que é mais comum - pois o primeiro é varrido "por ordem de chegada", o chamado *"first in, first out"*. Outra particularidade é que os nódulos já visitados devem ser marcados e a eles deve ser atribuído um "pai", ou seja, o outro nódulo que serviu de caminho para chegar nele.


 Pseudo-código:
 1 função BFS(inicio, final):
 2 	nódulos_visitados ← começa com (inicio), seu pai é (NaN)
 3 	fila ← queue vazia
 4 	adiciona à fila(inicio)
 5 	enquanto ainda há elemento na fila:
 6     	atual ← remove e recebe elemento da fila()
 7     	se (atual) é igual ao (final), então:
 8         	retorno
 9     	se não:
 10        	para cada (nódulo) em (conexões do atual):
 11            	se (nódulo) não foi visitado:
 12                	adiciona a nódulos_visitados, com (atual) como pai
 13                	adiciona à fila(nódulo)

 Complexidade

 -	Complexidade de tempo

 O algoritmo, da forma construída, possui complexidade em notação 'BigOH' O(N + C), onde N é o número de Nódulos e C é o número de conexões, isso é facilmente visível se analisarmos o papel das linhas 6, 10 e 11 do pseudo-código. É observado que, por conta do queue e do fato de que mantemos na memória quais elementos foram visitados, então cada nódulo só será visitado uma vez, assim, para essa parte a complexidade do pior caso é O(N). Na linha 10, contudo, nós verificamos cada conexão de cada nódulo uma vez, e como a mesma conexão aparece em dois nódulos diferentes, toda conexão aparecerá duas vezes no pior caso, assim, a complexidade dessa parte do algoritmo no pior caso será O(2C) = O(C). Finalmente, para o algoritmo inteiro, podemos concluir que ele possui complexidade de tempo em notação "BigOH" O(N + C)

 -	Complexidade de memória

 Como devemos manter na memória cada nódulo já visitado, concluímos que a complexidade de memória em notação "BigOH" será O(N), onde N é o número de nódulos.






 links externos:

 ●	Detalhamento do algoritmo
 ○	https://pt.wikipedia.org/wiki/Busca_em_largura#Complexidade_de_Espa%C3%A7
 ○	https://www.hackerearth.com/pt-br/practice/algorithms/graphs/breadth-first-search/tutorial/

 ●	Análise
 ○	https://www.ime.usp.br/~pf/algoritmos_para_grafos/aulas/bfs.html
 ○	http://aris.me/contents/teaching/data-mining-ds-2016/resources/clrs-bfs.pdf

 ●	Vídeos
 ○	https://www.youtube.com/watch?v=piBq7VD0ZS


 ________________________________________
 Grupo Turing
 Grupo de Extensão da Universidade de São Paulo (USP)
 turing.usp@gmail.com
 grupoturing.netlify.com
 facebook.com/grupoturing.poliusp
 medium.com/turing-talks
 linkedin.com/company/grupo-turing
