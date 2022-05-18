## Estruturas condicionais

Veremos aqui:
- operador ternário
- if...else
- switch case 

# Operador ternário

Estrutura do operador ternário: 

condição ? caso seja verdadeiro : caso seja falso

1- Você irá passar o que quer verificar e a condição 
2- Vai passar, depois do '?', o que você quer que aconteça caso a condição seja verdadeira
3- Vai passar, depois do ':', o que você quer que aconteça caso a condição seja falsa

### Exemplo:
```jsx 
let valor = 5
valor > 10 ? console.log('o valor é maior do que 10') : console.log('o valor não é maior do que 10')
```
1- Verificou a variável valor e a condição que botou é se ela é maior que 10
2- O que acontece caso a var seja maior que 10 (verdadeiro)
3- O que acontece caso a var seja menor do que 10 (falso)

#### Também é possível armazenar o operador ternário em uma variável e deixá-lo mais complexo

- Exemplo:

```jsx
let hora = 3

let resultado = hora >= 0 && hora <=5 ? 'madrugada ' :
hora >=6 && hora <=11 ? 'manhã' :
hora >=12 && hora <= 18 ? 'tarde' :
hora >=18 && hora <= 23 ? 'noite' :
'horario invalido'

console.log(resultado)

```

Nesse exemplo, armazenamos a estrutura na variável chamada resultado. Nesse caso, não botamos um console.log em cada condição, porque quando chamarmos a variável dentro do console.log, já irá aparecer normalmente o resultado.

Verificamos a variável hora e passamos condições para ela. 
É como se tivéssemos falado:
hora é maior ou igual a 0 e menor ou igual a 5? se for, aparece madrugada. se não for, verifica se ela é maior ou igual a 6, e menor ou igual a 11? se for, aparece manhã. se não for, verifica se ela é maior ou igual a 12, e menor ou igual 18? se for, aparece tarde. se não for, verifica se ela é maior ou igual a 18 e menor ou igual a 23? se for, aparece noite. se não for, aparece horário inválido. 

### Mais um exemplo:

```jsx

let nome = 'Maria', idade = 22;

let verifica = idade > 18 ?
`Pode entrar na festa! ${nome} entrou na festa.` :
`Desculpe, ${nome}, você não pode entrar na festa.`

console.log(verifica)

```

# If...else

Estrutura:

if(o que será verificado e sua condição){
escopo do if. se a condição for verdadeira, tudo que está aqui dentro acontece 
}else {
escopo do else. se a condição for falsa, acontece o que está aqui dentro
}

### Exemplos:

```jsx

/* 2. Escreva	 um	 programa	 para	 ler o	ano de	 nascimento	 de	 uma	 pessoa	 e	
escrever	 uma	 mensagem	 que	 diga	 se	
 ela	 poderá	 ou	 não	 votar	 este	 ano	
(não	é	necessário	considerar	o	mês	em	que	ela	nasceu).*/

let anoDeNascimento = 2004

if(anoDeNascimento <= 2006){

console.log('Você pode votar esse ano.')

} else {console.log('Você não pode votar esse ano.')}

```

1- Verificamos a variável anoDeNascimento e se ela era menor ou igual a 2006.
2- Se isso fosse verdadeiro, aconteceria tudo o que está dentro do escopo do if, ou seja: apareceria a mensagem dizendo que a pessoa pode votar esse ano.
3- Se fosse falso, aconteceria o que está dentro do escopo do else, ou seja: a mensagem dizendo que não pode votar esse ano.

```jsx

/*Escreva	 um	 programa	 que	 verifique	 a	 validade	 de	 uma	 senha	 fornecida	
pelo	 usuário.	 A	 senha	 válida	 é	 o	 número	 1234.	Devem	 ser	impressas	 as	
seguintes	mensagens:	
ACESSO	PERMITIDO	caso	a	senha	seja	válida.	
ACESSO	NEGADO	caso	a	senha	seja	inválida.*/

let senhaDeAcesso = '1234'

if (senhaDeAcesso === '1234'){

    console.log('ACESSO PERMITIDO')
}else {console.log('ACESSO NEGADO')}

```
Perceba que no else, não é preciso colocar nenhuma condição falsa, como se estivéssemos dizendo:
"Se for isso, isso e isso, é falso, e deve aparecer essa mensagem no console", porque o else é basicamente: tudo que for falso. Então, verificou a condição, não é verdadeira? Ela já cai no else.

```jsx

/*As	maçãs	 custam	 R$	 0,30	 cada	 se	 forem	 compradas	menos	 do	 que	 uma	
dúzia,	 e	 R$	 0,25	 se	 forem	 compradas	 pelo	 menos	 doze.	 Escreva	 um	
programa	 que	 leia	 o	 número	 de	 maçãs	 compradas,	 calcule	 e	 escreva	 o	
valor	total	da	compra.*/

let quantidadeMaças = 50
let valorTotalDaCompra

if(quantidadeMaças < 12){
  valorTotalDaCompra =  quantidadeMaças*0.30
  console.log(`O valor total da sua compra é ${valorTotalDaCompra}`)
}else{ 

valorTotalDaCompra = quantidadeMaças * 0.25
console.log(`O valor total da sua compra é ${valorTotalDaCompra}`)
}
// Se a primeira condição for falsa, ou seja, for maior que 11 (porque ali na condição que botamos não inclui o 12, só incluiria se fosse <=12), já cai no escopo do else.
```

```jsx

/* 1. Faça um script que verifique se uma letra digitada
 num campo de input é vogal ou consoante.*/

 let letra = 'j'

 if(letra === 'a' || letra === 'e' || letra === 'i' || letra === 'o' || letra === 'u'){
     console.log('vogal')
 }else {console.log('consoante ')}

 // Não precisamos botar "se for b, c, d... é consoante" porque se verificar a condição, e ver que ela é falsa, ou seja, não é "a, e, i o ou u", só pode ser consoante, então já cai no escopo do else.

 ```

 # Switch case

 Estrutura:
switch (aqui você passa o que irá verificar){
case "seja isso": acontece isso
break; pra parar de rodar porque já aconteceu o que era preciso.

default: caso não seja nada, cai aqui
}

O switch não recebe condição e sim o que vai avaliar, uma variavel pode-se dizer. E aí tem os cases, e cada um é uma condição.

### Exemplos:
```jsx
let usuario = "comum"

switch(usuario){

case "comum": console.log('comum')
break
case "empresa": console.log('empresa')
break
case "gerente": console.log("gerente")
break

default: console.log("usuario não reconhecido") 
}
```
1- verificamos a variável usuario
2- dentro do escopo do switch, dissemos: CASO seja "comum": aparece isso e para de rodar o código (break); caso seja "empresa": aparece isso e para de rodar o código (break); caso seja "gerente": aparece isso e para de rodar o código. Se não for nem comum, nem empresa, nem gerente, cai no dafault, e aparece isso.

Ele vai verificando em sequência, se já atender o que queremos no primeiro case, o break faz o código parar de rodar ali. Se não atender, ele passa pra próxima linha, verifica e se atender, o break faz parar de rolar o código ali.

### O problema de não usar o break:

Ele lê e mostra no console tudo em sequência:
```jsx
let usuario = "comum"

switch(usuario){

case "comum": console.log('comum')

case "empresa": console.log('empresa')

case "gerente": console.log("gerente")


default: console.log("usuario não reconhecido") 
}
```
Nesse caso, sem o break:
Ele passou na linha 1, fez a conta. Depois foi na linha 2, fez a conta de novo e juntou ao resultado anterior...até a ultima linha ele fez isso. E não é o que queremos. Queremos que verifique o cargo e faça a multiplicação referente somente a aquele cargo. Nesse caso do exemplo, ele multiplicou o 2000 por 1.15, 1.10, 1.05. 
```jsx 
var cargo = "gerente";
var salario = 2000;

switch (cargo) {
    case "gerente":
        salario *= 1.15;
    case "supervisor":
        salario *= 1.10;
    default:
        salario *= 1.05;
} 

console.log(salario);

```



```jsx
 /* Crie uma variável chamada “fruta”. 
Esta variável deve receber uma string com o nome de uma fruta. 
Após, crie uma estrutura condicional switch que receba esta variável e que possua três casos: 
caso maçã, retorne no console: “Não vendemos esta fruta aqui”. 
Caso kiwi, retorne: “Estamos com escassez de kiwis” 
e caso melancia, retorne: “Aqui está, são 3 reais o quilo”. 
Teste com estas três opções e verifique o console do seu navegador.
 Crie também um default, que retornará uma mensagem de erro no console.

 */

 let fruta = 'uva'

 switch (fruta){

case 'maçã':
    console.log('não vendemos essa fruta aqui')
    break
    case 'kiwi':
        console.log('Estamos com escassez de kiwis')
        break
        case 'melancia':
            console.log('Aqui está, são 3 reais o quilo')
            break
default: console.log('ERRO')

 }
```

```jsx
/* Um homem decidiu ir à uma revenda comprar um carro. 
 Ele deseja comprar um carro hatch, e a revenda possui
  além de carros hatch, sedans, motocicletas e caminhonetes. 
  Utilizando uma estrutura switch/case, caso o comprador queira o hatch, 
  retorne: “Compra efetuada com sucesso”. Nas outras opções, 
  retorne: “Tem certeza que não prefere este modelo?”. 
  Caso seja especificado um modelo que não está disponível, 
  retorne no console: “Não trabalhamos com este tipo de automóvel aqui”.

  */

  let modeloDoCarro = 'logan'

  switch (modeloDoCarro){
case 'hatch':
    console.log('Compra efetuada com sucesso')
    break
    case 'sedans':
    console.log('Tem certeza que não prefere este modelo?')
    break
    case 'motocicletas':
    console.log('Tem certeza que não prefere este modelo?')
    break
    case 'caminhonetes':
    console.log('Tem certeza que não prefere este modelo?')
    break
    default: console.log('Não trabalhamos com este tipo de automóvel aqui')
  }
  ```

  ```jsx 
  


 

  /*
   Temos como dados de entrada a nota média de cada aluno. 
   Dentro do switch, teremos vários cases (casos). 
   Caso a nota for maior ou igual a sete, o aluno estará aprovado. 
   Caso seja entre cinco e sete, o aluno estará em recuperação 
   e se a nota for menor que cinco, o aluno está reprovado. 
   Utilizando este exemplo conceitual, conseguimos aplicar na prática o uso do switch/case.
   */

let notaMedia = 6

switch(notaMedia <5){
case true:
console.log('reprovado')
break
case false:
switch(notaMedia >=5 && notaMedia<7){
case true: 
console.log('recuperação')
break
case false:
switch(notaMedia >=7){
case true:
console.log('aprovado')
break
                }
        }
}
```

Quando estamos trabalhando com algo menos fixo no switch, fica mais complexo. 

### Exemplo:
```jsx
let valor = 158

switch (valor <= 150){ // o que vai verificar 
case true: console.log('dentro do orçamento') // caso seja verdade, aparece isso
break; // e para de rodar o código, pois ja atendeu a condição
case false: // caso seja falso, temos um outro switch case
switch(valor >150){
case true: console.log('fora do orçamento')
break;
        

    }}
```

### Lembra do exemplo das horas com o operador ternário?
Se colocássemos esse exemplo no switch, assim:

switch (horario) { 
case (horario >=0 && horario <=6): 
console.log('madrugada') 
break }

Não ia aparecer nada, o case é para casos mais específicos. Condições assim precisam vir no switch.


#### Outra forma de fazer o exercício de horários: 
```jsx
switch (horario) { 
    case 0: 
    case 1:
    case 2:
    case 3: 
    case 4:
    case 5:
        console.log("madrugada")
        break;
    case 6:
    case 7:
    case 8:
    case 9:
    case 10:
    case 11:
        console.log("manhã")
        break;
    case 12:
    case 13:
    case 14:
    case 15:
    case 16:
    case 17:
        console.log("tarde")
        break;
    case 18:
    case 19:
    case 20:
    case 21:
    case 22:
    case 23:
        console.log("noite")
        break;
    default:
        console.log("horário inválido");
}

```
```jsx

let hora = 19

switch(hora>=0 && hora <=5){
case true: console.log('madrugada')
break;
case false:
switch(hora>=6 && hora <=11){
case true: console.log('manhã')
break;
case false:
switch(hora>= 12 && hora <=17 ){
case true: console.log('tarde')
break;
case false:
switch(hora>=18 && hora <=23){
case true: console.log('noite')
break;
default: console.log('horario invalido')
}}
}}

```




## Materiais de reforço:
#### Operador ternário:
https://programadorviking.com.br/if-ternario-javascript/

#### if...else:
https://professor.luzerna.ifc.edu.br/marcelo-cendron/wp-content/uploads/sites/40/2017/02/lista-exercicios-if-else.pdf
https://www.javascriptprogressivo.net/2018/08/Exercicios-IF-ELSE-JavaScript.html
https://www.devmedia.com.br/javascript-if-else-criando-scripts-com-estruturas-condicionais/39686

#### Switch case:
https://www.devmedia.com.br/javascript-switch/39761

