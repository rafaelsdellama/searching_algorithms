# searching_algorithms

## Arvore Binaria
* Suponho que x é um nó da arvore de busca binária, para qualquer nó y,
* Se y está na sub-arvore esquerda do x, então key[y] £ key[x].
* Se y está na sub-arvore direita do x, então key[x] £ key[y].

```
int ArvoreBusca(int v [], int x, int k){
	if (x == null || k == v[x])
		return x
	if (k < v[x])
		return ArvoreBusca(v[x-1], k)
	else 
		return ArvoreBusca(v[x+1], k)
}
```

## Busca Binaria
* Se os dados estiverem ordenados em um arranjo, pode-se
tirar vantagens dessa ordenação - Busca binária
* O elemento buscado é comparado ao elemento do meio
do arranjo
• Se igual, busca bem-sucedida
• Se menor, busca-se na metade inferior do arranjo
• Se maior, busca-se na metade superior do arranjo
* Complexidade: O(log(n))

```
int Bin-Search(int c[], int primeiro, int ultimo, int k){
	int meio;
	if primeiro > ultimo
		return null;
	meio = (primeiro + ultimo) / 2;
	if (k == c[meio])
		return meio;
	else 
		if k < c[meio]
			return Bin_search(c, primeiro, meio - 1, k);
		else 
			return Bin_search(c, meio + 1, ultimo, k);
}
```

## Algoritmo de busca seqüencial em um vetor A, com
N posições (0 até N-1), sendo x a chave procurada
* Compara a chave com cada item na array ou lista, até encontrar
um item de dado cujo valor é igual o valor da chave.
* Melhor caso: O(1)
* Pior caso: O(n)

```
int BuscaSequencial (int A[], int x, int n){
	int i;
	for (i=0; i<n; i++)
		if (A[i]==x)
			return(i); /*chave encontrada*/
	return(-1); /*chave não encontrada*/
}
```

## Busca Sequencial com Sentinela
* Sentinela: consiste em adicionar um elemento de valor x
no final da tabela
* O sentinela garante que o elemento procurado será
encontrado, o que elimina uma expressão condicional,
melhorando a performance do algoritmoA[N]=x;
* Melhor caso: O(1)
* Pior caso: O(n)

```
int BuscaSequencialSentinela ( int A[], int x, int n){
	int i;
	for(i=0; x!=A[i]; i++){
	}
	if (i<n) 
		return(i); /*chave encontrada*/
	else 
		return(-1); /*sentinela encontrado*/
}
```
