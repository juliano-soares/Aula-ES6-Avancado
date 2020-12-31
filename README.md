# Aula ES6 avançado

### Funções avançadas do ES6

Quando podemos omitir os parênteses de uma arrow function?

> Quando existir apenas um argumento e nada mais.

Qual a forma tradicional de escrever funções, antes de existirem arrow functions?

> A palavra function, o seu nome de maneira opcional, os parênteses e as chaves para o corpo.

Qual a forma de criar uma função construtora com arrow functions?

> Não podemos criar funções construtoras usando arrow functions.

As arrow functions são sempre:

> Funções anônimas.

Quando podemos omitir o valor de uma propriedade ou método ao definir um objeto literal?

> Quando o valor vier de uma variável com o mesmo nome da propriedade ou método.

O que será exibido no console após a execução do código abaixo:
var obj = {
sleep: function() {
setTimeout(() => {
console.log(this);
}, 1000);
}
}
obj.sleep();

> O objeto 'obj'.

Podemos realizar expressões para definir nomes de atributos?

> Sim, utilizando colchetes.

O que é 'lazy evaluation'?

> A característica que permite podermos utilizar funções para definir valores de um argumento e a mesma só será invocada quando o argumento for indefinido.

Podemos referenciar outro argumento como valor padrão para um argumento?

> Sim, mas apenas se o argumento vier anteriormente ao que está sendo atribuído.

Qual a forma de atribuir um valor padrão ao argumento de uma função que surgiu com o ES6:

> Usando o caractere '=' seguido do valor que queremos atribuir ao argumento.

### Aplicando conceitos Rest, Spread Operator e Destructuring

Ao realizar o seguinte destructuring assignment, qual será o valor da variável 'four'?
let [one, two, three, four] = ['Digital', 'Innovation', 'One'];

> undefined

O destructuring pode ser usado em nested objects (objetos aninhados)?

> Sim.

Ao construir um objeto literal a partir de outro, utilizando o spread operator, a ordem é importante pois:

> A ordem define quais valores das chaves com o mesmo nome irão prevalecer.

Qual a forma de aplicar o destructuring assignement em um array (arr), atribuindo o valor do seu primeiro índice para uma constante teste?

> const [ teste ] = arr;

Quando o rest operator é utilizado nos argumentos de uma função, além da lista de argumentos, ele também traz:

> Os métodos e propriedades de array por ser uma instância de um array.

Antes da existência do spread operator, qual era uma das formas utilizadas para enviar os items de lista como argumentos para uma função?

> Utilizando o método de função apply.

É possível combinar default function arguments com destructuring?

> Sim, sempre que necessário podemos utilizar os dois, respeitando as regras de ambos.

Ao utilizar o spread operator em uma string o seu retorno será:

> Uma lista contendo cada um dos caracteres da string.

Spread operators podem ser utilizados onde?

> Em arrays, strings, na definição de objetos literais e objetos iteráveis.

Qual a forma de combinar dois arrays utilizando spread operator?

> [...arr1, ...arr2];

### Introdução a Generators

Symbols podem ser usados para gerar:

> Identificadores únicos.

Tipos e objetos iteráveis possuem:

> Um método responsável por gerar o seu iterador, sendo acessível pela chave Symbol.iterator.

O "for of" é utilizado para:

> Obter os valores gerados através do iterador em um objeto ou tipo iterável.

Podemos utilizar generators para construir objetos iteráveis?

> Sim, pois generators utilizam a mesma interface e podem ser utilizados para construir o iterador de um objeto iterável.

Generators podem "pausar" sua execução através de qual palavra reservada:

> yield.

Generators podem receber valores em cada pausa para continuar sua execução?

> Sim, podemos enviar valores de volta ao iterador passando o valor como parâmetro ao método next.

Qual a forma de retornar um valor em cada iteração de uma função generator?

> Incluindo o valor após a palavra yield.

Ao consumir um iterador, como sabemos se a iteração finalizou?

> Através da propriedade done no objeto retornado na iteração.

Ao invocar o método next de um iterador, o seu retorno deve ser:

> Um objeto contendo um método next e uma propriedade done.

Propriedades de objetos criadas usando identificadores únicos podem ser descobertas usando:

> Utilizando o symbol utilizado como identificador ou o método Object.getOwnPropertySymbols.

### Aplicando conceitos Promises e Fetch

A palavra reservada await pode ser usada quando?

> Apenas dentro de uma função criada utilizando a palavra async e para aguardar a resolução de uma promise.

Qual o objetivo do método Promise.race?

> Criar uma Promise contendo diversas Promise e trazer o retorno da primeira que resolver entre elas.

Uma requisição feita utilizando fetch só irá disparar um erro caso:

> Aconteça um erro de rede e não seja possível realizar a requisição.

Qual a forma de processar múltiplas Promise de maneira paralela e tratar o retorno de todas posteriormente?

> Utilizando o método Promise.all.

Qual o retorno da invocação da função fetch?

> Uma Promise.

Qual a diferença entre o método on e once de uma instância EventEmitter?

> Um subscreve uma função a todas as ocorrências de um evento, o outro apenas para a primeira ocorrência.

Quais os três estados possíveis de uma Promise?

> Pending, fulfilled e rejected.

Qual é uma das formas de construir uma Promise no JavaScript?

> Invocando o seu construtor e passando uma função ao mesmo. Ex: new Promise((resolve, reject) => {}).

Utilizar callbacks ao desenvolver JavaScript assíncrono pode trazer quais tipos de problemas quando não utilizado com cautela?

> Problemas com a legibilidade e manutenção do código, pois podemos cair no chamado "callback hell".

Qual o método de uma Promise utilizado para tratar seus erros?

> O método .catch que irá receber uma função para o tratamento.

### Conceitos aplicados a qualidade de código e automação de testes em JS

Quais são as etapas que compõem o TDD?

> Escrita do teste descrevendo o comportamento esperado, escrita do código com o comportamento esperado e refatoração.

Qual é um dos principais objetivos do BDD (desenvolvimento orientado a comportamento)?

> Integrar regras de negócio com linguagens de programação.

Como aguardamos um código assíncrono finalizar em um teste no mocha?

> Utilizando a função done que vem como parâmetro ao it posteriormente à execução do código assíncrono.

Os testes unitários são responsáveis por testar o quê?

> A menor unidade do seu código como funções, métodos e afins.

Qual a função do método spy do sinon?

> Criar uma função ou interceptar a execução de uma outra função a fim de obter dados sobre como a mesma foi invocada.

A responsabilidade dos testes de integração é:

> Garantir o funcionamento de unidades menores trabalhando em conjunto com outras.

Caso não seja passada nenhuma configuração de diretórios ao mocha, qual será o diretório na raiz do projeto onde serão buscados os testes?

> test.

Ao utilizar o módulo assert do Node.js, quando utilizamos seu método equal para validar dois valores, caso os dois não sejam iguais, qual será o seu comportamento?

> Será disparado um erro contendo informações sobre a asserção incorreta.

Os testes funcionais visam:

> Garantir o correto funcionamento de uma funcionalidade de ponta a ponta.

Qual a maior vantagem de utilizar o chai como ferramenta de asserção?

> Ao escrever asserções utilizando chai, uma das maiores vantagens é a sua escrita muito mais expressiva do comportamento esperado.

### Tratamentos e exceções

Qual o objetivo do método console.assert?

> Exibir uma mensagem de erro no console caso a asserção não passe.

Qual o objetivo da aba styles dentro das ferramentas para desenvolvedor do navegador Chrome?

> Tem o objetivo de mostrar as regras de CSS aplicadas nos elementos, permitindo o debugging dos estilos.

Qual o objetivo da aba network dentro das ferramentas para desenvolvedor do Chrome?

> Trazer informações sobre as requisições executadas no navegador.

Qual a objetivo da declaração finally após os blocos de try e catch?

> Garantir e deixar explícito que um bloco de código será executado em caso de erro ou não.

Qual o objetivo do método console.time e console.timeEnd?

> Registrar um intervalo de tempo no console do navegador.

Qual o objetivo do método console.error?

> Mostrar logs de erro no console do navegador.

O que acontece no Chrome ao incluirmos a declaração debugger dentro de um código JavaScript?

> O código irá parar sua execução ao encontrar a declaração, permitindo o debugging.

Quais as vantagens de estender a classe de erro padrão do JavaScript?

> A possibilidade de adicionar métodos, propriedades e comportamentos ao erro.

Qual a maneira mais comum para capturar uma exceção no JavaScript?

> Através das declarações try e catch.

Qual o objetivo da função pretty print do navegador Chrome?

> Remover a minificação de um arquivo para possibilitar um debugging melhor.
