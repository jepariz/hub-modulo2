# Exercício 1

## Enunciado: 
Crie uma função chamada ultimoImpar(lst), que recebe uma array como entrada que deve ser atravessada em busca do último elemento ímpar. Deve retornar o último valor ímpar encontrado. Caso não seja encontrado nenhum valor ímpar, deve ser retornado null.

## Resolução:

``` 
function ultimoImpar(lst){

  let ultimo = null
  
  for(let i = 0; i < lst.length; i++){
    if(lst[i] % 2 !== 0){
      ultimo = lst[i]
    }
  }
 return ultimo
}
```
## Explicação:

Primeiro, eu criei uma variável "ultimo" incializada como null, mas que vai receber o último valor ímpar (se houver). 

Depois, eu criei um loop for para percorrer a lista. A cada iteração, o if está verificando se o resto da divisão do item no índice "i" por 2 não é 0, pois assim sabemos que um número é ímpar. Caso a condição seja verdadeira, o valor desse item é enviado para a variável "ultimo"

Por fim, fora do loop, é feito o retorno de ultimo que se tiver algum número ímpar vai retorná-lo, senão vai retornar null. 

# Exercício 2

## Enunciado: 
Crie uma função chamada maiorDecimal(lst), que recebe uma lista e retorne o maior número em formato decimal que e for encontrado na lista. Caso não existam números no formato decimal retorne null.

## Resolução:

``` 
function maiorDecimal(lst){
  
  let maiorDec = null

 for(let i = 0; i < lst.length; i++){
   
    let numDec = (lst[i] - Math.floor(lst[i])) !== 0
   
      if(numDec){
        if(lst[i] > maiorDec){
         maiorDec = lst[i]
        }
        }     
 }
  return maiorDec
}
```
## Explicação:

Primeiro, eu criei uma variável "maiorDec" incializada como null, mas que vai receber o maior valor decimal (se houver). 

Depois, eu criei um loop for para percorrer a lista. A cada iteração, verificacamos se o valor do item naquela posição (lst[i]) menos o seu inteiro (Math.floor(lst[i])) é diferente de 0. Caso isso seja verdadeiro significa que ele é um número decimal, portanto a variável "numDec" vai armazenar um booleano true.(Ex: let numDec = 3.5 - 3 é igual a 0.5, assim, lst[i] é decimal)

Em seguida, se o número é decimal, um if verifica se ele é o maior, comparando com o valor armazenado na variável "maiorDec". Caso seja maior, lst[i] é armazenado na váriavel "maiorDec". 

Por fim, fora do loop, é feito o retorno de "maiorDec" que se tiver algum número vai retorná-lo, senão vai retornar null. 