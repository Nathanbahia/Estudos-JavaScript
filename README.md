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
}
```

### .map()
Realiza uma iteração em uma coleção de elementos e retorna uma nova coleção.
```
function dobrar(elemento) {
  return elemento * 2;
 }
 
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

let numeros_dobrados = numeros.map(dobrar);
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
```
