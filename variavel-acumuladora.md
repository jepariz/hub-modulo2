# Exercício 1

## Enunciado: 
Faça uma função chamada convertAndSum(lst), essa função recebe uma lista que contém strings numéricas, e deve retornar o valor relativo a soma dos números nessas strings.

## Resolução:

``` 
function convertAndSum(lst){
  
  let soma = 0
  
  for(let i = 0; i < lst.length; i++){
    let number = Number(lst[i])
    soma += number
  }
  
  return soma
}
```

## Explicação:

Primeiro, eu criei uma **variável acumuladora** para receber a soma dos números do array a cada iteração.

Depois, eu criei um loop for para percorrer a lista. A cada nova iteração, a string é tranformada em número usando o método Number() e, depois, esse número é somado aos valores que já estão aramazenados na variável soma.  

Por fim, o return que está fora do loop for tem como função retornar a soma total. 

# Exercício 2

## Enunciado: 
Faça uma função chamada acumulaVogais(lst), que recebe uma lista contendo strings de um único caracter cada, e acumule em uma string todas as vogais dessa lista. Retorne a string das variáveis acumuladas.

## Resolução:

``` 
function acumulaVogais(lst){
  let string = "";
  
  for(let i = 0; i < lst.length; i++){
    let ehVogal = (lst[i] == 'a' || lst[i] == 'e' ||
     lst[i] == 'i' || lst[i] == 'o' || lst[i] == 'u') 
   
    if(ehVogal) {
    	string += lst[i];
    }
  }
  return string;
}
```
## Explicação:

Primeiro, eu criei uma variável "string" incializada como vazia, mas que vai receber as vogais da lista. 

Depois, eu criei um loop for para percorrer a lista. A cada iteração a variável "ehVogal" recebe um booleano (true se a string for vogal e false se for consoante). O if está verificando apenas os casos em que a variável "ehVogal" está como true, então, ele soma a vogal às outras que já estão aramazenadas na variável "string". 

Por fim, fora do loop, é feito o retorno da string. 