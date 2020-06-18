# Curso de JavaScript Geek University

1. forEach()
2. map()
3. filter()
4. reduce()
5. Funções Anônimas
6. Arrow Functions
7. Funções Construtoras

### .forEach()
Realiza uma iteração em uma coleção, semelhante ao ```for``` tradicional. Retorna a mesmo coleção, podendo ter aplicado alguma transformação em seus elementos, ou não.

```
let nomes = ['Nathan', 'Batista', 'Assis', 'Bahia'];

nomes.forEach(function (nome, index) {
  console.log(nome);
});

>>> Nathan
>>> Batista
>>> Assis
>>> Bahia
```

### .map()
Realiza uma iteração em uma coleção de elementos e retorna uma nova coleção.
```
function dobrar(elemento) {
  return elemento * 2;
 }
 
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

let numeros_dobrados = numeros.map(dobrar);

>>> (10) [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

### .filter()
Assim como o .map(), retorna uma nova coleção de elementos, porém, apenas com aqueles que atendam a determinada condição:

```
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

function filtra_pares (numero) {
  if (numero % 2 === 0) {
    return true;
  }
}

let pares = numeros.filter(filtra_pares);

>>> (5) [2, 4, 6, 8, 10]*
```

### .reduce()
Reduz uma coleção de elementos:

```
let numeros = [1, 2, 3, 4, 5];
numeros.reduce(function(anterior, posterior) {
  return anterior + posterior;
});

>>> 15

```

### Funções anônimas
São funcões que não possuem nome definidos. Tem a desvantagem de serem dificilmente reaproveitadas em outras partes do código.

Exemplo 1:
```
btn.onclick = function () {
  alert("Botão clicado!");
}
```

Exemplo 2:
```
const calculaIdade = (anoAtual, anoNasc) => {
  return anoAtual - anoNasc;
}
minhaIdade = calculaIdade(2020, 1994);
console.log(minhaIdade);

>>> 26
```

No exemplo 2, apesar de ser uma função anônima, declaramos ela dentro de uma constante, que poderá chamar a função como feito acima.
