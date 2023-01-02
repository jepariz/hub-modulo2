# Exercício 1

## Enunciado: 
Crie uma função chamada string3(lst), que recebe uma lista de strings e retorna a primeira string de 3 letras encontrada. Caso não exista strings de tamanho 3, retorne uma string vazia.

## Resolução:

``` 
function string3(lst){
  for(let i=0; i < lst.length; i++){ 
    if(lst[i].length === 3){
      return lst[i]
    }
  }
  return ""
} 
```

## Explicação:

Primeiro, eu criei um loop for para percorrer a lista. 

Depois, criei a condção de parada do loop: 
```  
    if(lst[i].length === 3){
      return lst[i]
    } 
```
Essa técnica se chama **retorno antecipado** justamente porque o return dentro do if vai encerrar o loop assim que a condição do if for válida, ou seja, assim que um item que tenha 3 caracteres for encontrado. Dessa forma, nós não percorremos todo o array, pois vamos retornar um resultado assim que a condição for verdadeira. 

Por fim, o return que está fora do loop for tem como função retornar uma string vazia caso depois de percorrer todo o array não seja encontrada nenhuma ocorrência de string com 3 caracteres. 


# Exercício 2

## Enunciado:
Cria uma função chamada valorDobraIndice(lst), que recebe uma lista de inteiros e que analisa essa lista em procura de um caso onde o valor do elemento seja o dobro do índice que aquele elemento ocupa. Retorne o valor do índice caso exista esse caso, e false caso contrário.

## Resolução:
``` 
function valorDobraIndice(lst){
  for(let i =0; i < lst.length; i++){
    if(lst[i] === i * 2){
      return i
    }
  }
  return false
}

```

## Explicação:

Primeiro, criei um loop for para percorrer o array.

Depois, o if está buscando por um item na lista (lst[i]) que seja igual ao índice dele mesmo (i) multiplicado por 2. Caso encontre um item que atenda a essa condição, ocorrerá o **retorno antecipado** que retornará o índice em que esse item se encontrava (i).

Por fim, o return fora do loop for retorna false caso não haja nenhum item atenda à condição do if. 

# Exercício 3

## Enunciado:
Crie uma função chamada ultimoNegativo(lst) que recebe uma array, e precisa retornar o valor do elemento com o maior índice dessa array que é negativo. Ou seja, se houver vários números negativos, a função deve retornar aquele que aparece por último (maior índice). Caso a função não encontre valores negativos deve retornar false.

## Resolução:
``` 
function ultimoNegativo(lst) {
  for (let i = lst.length - 1; i >= 0; i--) {
    if (lst[i] < 0) {
      return lst[i];
    }
  }
  return false;
}

```

## Explicação:

Primeiro, criei um loop for para percorrer o array de forma reversa, ou seja, do fim para o início. Por isso, o "i" inicializa na última posição do array (lst.length - 1), a condição é que ele percorra todo o array, então como estamos indo do maior índice para o menor, ele verifica se o i é maior ou igual a 0 (já que 0 é a primeira posição de um array) e ao invés de incremetar o valor de "i", nós diminuímos porque ele deve ir do maior para o menor índice. 

Depois, o if está buscando por um item na lista (lst[i]) que seja igual negativo, ou seja, menor que 0. Como nós queremos o valor negativo que está no maior índice, assim que ele encontrar um item que atenda a condição vai retornar esse item, pois estamos percorrendo o array dos maiores índices para o menor. 

Por fim, o return fora do loop for retorna false caso não haja nenhum item atenda à condição do if. 
