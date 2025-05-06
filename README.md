# Funçõesjs

## Declaration
Funções do tipo declaration são aquelas criadas a partir da palavra-chave function seguida do nome da função, seguido de parenteses que entre eles podem conter parâmetros para inserir valores diretamente ao chamar a função. Este tipo de função não é executada de imediato apenas quando ela é invocada.

### Vantagens
Este tipo de função pode realizar hoisting, tambem facilita a leitura e organização do codigo pos possui uma sintaxe clara.

### Desvantagens
Ela não é flexivel assim como as outras funções por possuir uma natureza estatica e não pode ser ultilizada como argumento em outra função.

### Exemplos
1- Forma de declaração padrão:

function soma() { return 1 + 1; } <br> soma();

2- Declaração com parametros:

function soma(a,b) { <br>
let resultado = a + b; <br>
return resultado; <br>
} <br> soma(3,3);

## Expression
Estas funções são declaradas diretamente em uma variavel sem a necessidade de dar um nome a função pois ela sera invocada ultilizando o nome da variavel logo esta variavel passa a ser ultilizada como uma função. Após a declaração da função é necessario terminar a linha com ponto e virgula pois passa a ser considerada como uma linha execultavel. 

## Arrow
