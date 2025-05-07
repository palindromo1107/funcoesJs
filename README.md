# FunçõesJs

## Declaration
Funções do tipo declaration são aquelas criadas a partir da palavra-chave function seguida do nome da função, seguido de parenteses que entre eles podem conter parâmetros para inserir valores diretamente ao chamar a função. Este tipo de função não é executada de imediato apenas quando ela é invocada.

### Vantagens
Este tipo de função pode realizar hoisting, tambem facilita a leitura e organização do codigo pos possui uma sintaxe clara.

### Desvantagens
Ela não é flexivel assim como as outras funções por possuir uma natureza estatica e não pode ser ultilizada como argumento em outra função.

### Exemplos
1- Forma de declaração padrão sem parâmetros:

function soma() { return 1 + 1; } <br> soma();

2- Declaração com parametros:

function soma(a,b) { <br>
let resultado = a + b; <br>
return resultado; <br>
} <br> soma(3,3);

3- Hoisting:

soma(9,1); <br>
function soma(a,b){ <br>
let resultado = a + b; <br>
return resultado; <br>
}

## Expression
Estas funções são declaradas diretamente em uma variavel geralmente são funções de uso único, este tipo de função pode ser considerado uma função anonima pois nao há necessidade de dar um nome a função pois ela sera invocada ultilizando o nome da variavel logo esta variavel passa a ser ultilizada como uma função. Após a declaração da função é necessario terminar a linha com ponto e virgula pois passa a ser considerada como uma linha execultavel.

### Vantagens
Funções do tipo expression tendem a serem mais flexiveis que as do tipo declaration, servem como argumento para outras funções e evita a poluição do escopo global.

### Desvantagens
Este tipo não pode realizar o hoisting como as do tipo declaration e são mais difíceis de ler quando a lógica por trás delas é complexa.

### Exemplos
1- Forma de declaração padrão sem parâmetros:

const subtracao = function(){ <br> return 1 + 1; <br>
}; <br>
subtracao();

2- Declaração com parametros:

const subtracao = function(a,b){ <br>
let resultado = a - b; <br>
return resultado; <br>
}; <br>
subtracao(8,6);

3- Função resultante em erro já que este tipo de função não realiza hoisting:

erro(); <br>
const erro = function(){<br>
return 1+1;<br>
};

## Arrow
Funções arrow são uma forma concisa de declarar funções e são ótimas para funções de callback, nela não é necessário a utilização da palavra-chave function, para retornar um valor não é necessário também a palavra-chave return se a função tiver apenas uma instrução que retorne um valor, é ultilizado "=>" para separar os paramteros do corpo da função.

### Vantagens
Estas funções possuem um código mais limpo e legível, possuem uma abordagem mais clara em questão do conceito this e são mais simples de ler se ultilizadadas em funções callback.

### Desvantagens
Não são adequadas para um conceito dinâmico do this, não são boas para escopo próprio por herdarem o escopo do contexto definido.

### Exemplos
1- Declaração sem parâmetros:

const soma = () => 1 + 9; <br>
soma()

2- Declaração com parametros:

const soma = (a,b) => a + b; <br>
soma(1,9);

3- Função em bloco:

const soma = (a,b) => { <br>
let resultado = a + b; <br>
return resultado; <br>
}; <br>
soma(7,3);
