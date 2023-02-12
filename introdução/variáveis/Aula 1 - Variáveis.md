# Aulinha de cria - Python
------------------
Professor: Rafael Monteiro Zancanaro (aka Rafão).

[Github](https://github.com/Rafael-monte/Aulinhas-de-cria)

### Nesta aula veremos os seguintes conceitos:

- Variáveis

--------------------

## Variáveis
### O que são variáveis?
Variáveis são valores que são armazenados na memória do computador enquanto seu programa está executando, isto é, elas armazenam temporariamente alguma **informação** até que o programa acabe.

Variáveis possuem **tipos**, que representam qual é o valor que vai ser armazenado nela. Esse *tipo de dado* pode ser inteiro, decimal, texto ou até coisas mais complexas, como *listas* e *estruturas compostas* (que serão vistas mais adiante).

Os tipos básicos ou *primitivos* de váriaveis em Python são:

| **Tipo** | **Valor que é armazenado** | **tamanho em *disco*** |
| -------- | -------------------------- | ---------------------- |
| int      | valores inteiros ( + e - ) | 28 *bytes*              |
| float    | valores decimais ( + e - ) | 24 *bytes*              |
| str      | valores de texto           | mínimo de 49 *bytes*    |

> <span style="color:dodgerblue; font-weight: bolder"> 	&#x2139;&#xFE0F; Nota: </span> Também é possivel ver o quão grande é o tamanho desses tipos [neste site.](https://code.tutsplus.com/tutorials/understand-how-much-memory-your-python-objects-use--cms-25609)

O *tamanho em disco* representa quantas células o sistema operacional (Windows, Linux, Mac, etc.) vai separar para armazenar o dado.


## Dinâmica: Verificando o tamanho dos tipos!
Vamos acessar um [interpretador de python online](https://www.onlinegdb.com/online_python_compiler) e colar o seguinte trecho de código:
```python
from sys import getsizeof;

integer_variable: int = 1
float_variable: float = 1.5
string_variable: str = ''
string_variable_with_content = 'a'

print("Tamanho do inteiro: ", getsizeof(integer_variable))
print("Tamanho do float (ponto flutuante)", getsizeof(float_variable))
print("Tamanho da string vazia (texto vazio)", getsizeof(string_variable))
print("Tamanho da string com conteúdo (texto com conteúdo)", getsizeof(string_variable_with_content));
```
Por enquanto vamos ignorar a linha 1 com o `from ... import` e focar no resto do conteúdo.

Neste código são criadas várias variaveis, cada uma com um **tipo de dado** diferente e com um valor distinto. Vamos destrinchar ele.

> `integer_variable: int = 1`

Nesta linha declaramos um tipo *inteiro* chamado "integer variable" que recebe o valor 1.


> `float_variable: float = 1.5`

Já nesta outra linha, declaramos um tipo *decimal* ou *ponto flutuante* chamado "float_variable", que recebe o valor 1,5

 > <span style="color:yellow; font-weight: bolder"> &#9888; Importante: </span> Como grande parte das linguagens de programação são em inglês, o separador de casas decimais é o ponto ( . ), portanto devemos sempre usar ele para escrever numeros de ponto flutuante.


> `string_variable: str = ''`

Nessa linha declaramos um *texto* ou *string* vazio, sem nenhum conteúdo.

> `string_variable_with_content = 'a'`

E por fim, nesta linha declaramos uma outra *string* com um valor dentro, no caso o caractére "a"

> ```python
print("Tamanho do inteiro: ", getsizeof(integer_variable))
print("Tamanho do float (ponto flutuante)", getsizeof(float_variable))
print("Tamanho da string vazia (texto vazio)", getsizeof(string_variable))
print("Tamanho da string com conteúdo (texto com conteúdo)", getsizeof(string_variable_with_content));
```

Nestas linhas nós mostramos o tamanho dessas variáveis com o `getsizeof`.

### Considerações importantes
- Em Python as variáveis não precisam ter seu tipo informado, já que o interpretador *infere* os seus tipos automaticamente. Porém é uma **boa prática** inserir os tipos.

