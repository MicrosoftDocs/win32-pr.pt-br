---
title: Operadores
description: As expressões são sequências de variáveis e literais pontuados por operadores.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119601"
---
# <a name="operators"></a>Operadores

As expressões são sequências de [variáveis](dx-graphics-hlsl-variable-syntax.md) e literais pontuados por [operadores](dx-graphics-hlsl-statement-blocks.md). Os operadores determinam como as variáveis e os literais são combinados, comparados, selecionados e assim por diante. Os operadores incluem:



| Nome do operador                                                                                | Operadores                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Operadores aditivos e multiplicativas](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Operador de matriz](#array-operator)                                               | \[i\]                                                              |
| [Operadores de atribuição](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Conversões binárias](#binary-casts)                                                   | Regras c para as regras float e int, C ou intrínsecos HLSL para bool     |
| [Operadores bit a bit](#bitwise-operators)                                         | ~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ = |
| [Operadores matemáticos boolianos](#boolean-math-operators)                               | & &, \| \| ,?:                                                      |
| [Operador cast](#cast-operator)                                                 | Escreva                                                             |
| [Operador de vírgula](#comma-operator)                                               | ,                                                                  |
| [Operadores de comparação](#comparison-operators)                                   | <, >, = =,! =, <=, >=                                   |
| [Operadores de prefixo ou sufixo](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Operador de estrutura](#structure-operator)                                       | .                                                                  |
| [Operadores unários](#unary-operators)                                             | !, -, +                                                            |



 

Muitos dos operadores são por componente, o que significa que a operação é executada de forma independente para cada componente de cada variável. Por exemplo, uma única variável de componente tem uma operação executada. Por outro lado, uma variável de quatro componentes tem quatro operações executadas, uma para cada componente.

Todos os operadores que fazem algo com o valor, como + e \* , funcionam por componente.

Os operadores de comparação exigem que um único componente funcione, a menos que você use a função [**All**](dx-graphics-hlsl-all.md) [**ou intrínseca**](dx-graphics-hlsl-any.md) com uma variável de vários componentes. A operação a seguir falha porque a instrução If requer um bool único, mas recebe um bool4:


```
if (A4 < B4)
```



As seguintes operações foram realizadas com sucesso:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Os operadores de conversão binária [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asent**](dx-graphics-hlsl-asint.md)e assim por diante funcionam por componente, com exceção de [**duas vezes**](asdouble.md) cujas regras especiais são documentadas.

Operadores de seleção como ponto, vírgula e colchetes de matriz não funcionam por componente.

Os operadores de conversão alteram o número de componentes. As operações de conversão a seguir mostram sua equivalência:


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Operadores aditivos e multiplicativas

Os operadores aditivo e multiplicativa são: +,-, \* ,/,%


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



O operador de módulo retorna o restante de uma divisão. Isso produz resultados diferentes ao usar inteiros e números de ponto flutuante. Os pendências inteiros que são fracionários serão truncados.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



O operador de módulo Trunca um resto fracionário ao usar números inteiros.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



O operador% é definido somente em casos em que ambos os lados são positivos ou ambos os lados são negativos. Ao contrário de C, ele também opera em tipos de dados de ponto flutuante, bem como inteiros.

## <a name="array-operator"></a>Operador de matriz

O operador de seleção de membro da matriz " \[ i \] " seleciona um ou mais componentes em uma matriz. É um conjunto de colchetes que contêm um índice baseado em zero.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



O operador de matriz também pode ser usado para acessar um vetor.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



Ao adicionar um índice adicional, o operador de matriz também pode acessar uma matriz.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



O primeiro índice é o índice de linha com base em zero. O segundo índice é o índice de coluna com base em zero.

## <a name="assignment-operators"></a>Operadores de atribuição

Os operadores de atribuição são: =, + =,-=, \* =,/=

Variáveis podem receber valores literais:


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



As variáveis também podem ser atribuídas ao resultado de uma operação matemática:


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Uma variável pode ser usada em qualquer um dos lados do sinal de igual:


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



A divisão para variáveis de ponto flutuante é como esperado porque as pendências decimais não são um problema.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Tenha cuidado se você estiver usando inteiros que podem ser divididos, especialmente quando o truncamento afetar o resultado. Este exemplo é idêntico ao exemplo anterior, exceto para o tipo de dados. O truncamento causa um resultado muito diferente.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Conversões binárias

A operação de conversão entre int e float converterá o valor numérico em representações apropriadas, seguindo as regras de C para truncar um tipo int. Converter um valor de um float para um int e voltar para um float resultará em uma conversão com perdas com base na precisão do destino.

As conversões binárias também podem ser executadas usando [**funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), que reinterpreta a representação de bits de um número no tipo de dados de destino.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Operadores bit a bit

O HLSL dá suporte aos operadores bit a seguir, que seguem a mesma precedência de C com relação a outros operadores. A tabela a seguir descreve os operadores.

> [!Note]  
> Os operadores de bit a bit exigem o [modelo de sombreador 4 \_ 0](dx-graphics-hlsl-sm4.md) com hardware Direct3D 10 e superior.

 



| Operador          |  Função                 |
|-----------|-------------------|
| ~         | Não lógico       |
| <<  | Deslocamento à esquerda        |
| >>  | Deslocamento à direita       |
| &         | AND lógico       |
| \|        | Ou lógico        |
| ^         | XOR lógico       |
| <<= | Deslocamento à esquerda igual  |
| >>= | Deslocamento à direita igual |
| &=        | E igual a         |
| \|=       | Ou igual a          |
| ^=        | XOR igual         |



 

Os operadores bit a bit são definidos para operar somente em tipos de dados int e uint. A tentativa de usar operadores bit-a-ponto nos tipos de dados float ou struct resultará em um erro.

## <a name="boolean-math-operators"></a>Operadores matemáticos boolianos

Os operadores matemáticos boolianos são:  &&, \| \| ,?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



Diferentemente da avaliação de curto-circuito de &&, \| \| e?: em C, as expressões HLSL nunca fazem um circuito curto de uma avaliação porque são operações de vetor. Todos os lados da expressão são sempre avaliados.

Operadores boolianos funcionam em uma base por componente. Isso significa que, se você comparar dois vetores, o resultado será um vetor que contém o resultado booliano da comparação para cada componente.

Para expressões que usam operadores boolianos, o tamanho e o tipo de componente de cada variável são promovidos para serem os mesmos antes que a operação ocorra. O tipo promovido determina a resolução na qual a operação ocorre, bem como o tipo de resultado da expressão. Por exemplo, uma expressão Int3 + float seria promovida para float3 + float3 para avaliação, e seu resultado seria do tipo float3.

## <a name="cast-operator"></a>Operador cast

Uma expressão precedida por um nome de tipo entre parênteses é uma conversão de tipo explícita. Uma conversão de tipo converte a expressão original para o tipo de dados da conversão. Em geral, os tipos de dados simples podem ser lançados para os tipos de dados mais complexos (com uma cast de promoção), mas apenas alguns tipos de dados complexos podem ser lançados em tipos de dados simples (com uma cast de rebaixamento).

Somente a seleção de tipo do lado direito é legal. Por exemplo, expressões como são `(int)myFloat = myInt;` ilícitas. Use `myFloat = (float)myInt;` em vez disso.

O compilador também executa conversão de tipo implícita. Por exemplo, as duas expressões a seguir são equivalentes:


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Operador de vírgula

O operador de vírgula (,) separa uma ou mais expressões que devem ser avaliadas na ordem. O valor da última expressão na sequência é usado como o valor da sequência.

Aqui está um caso para o qual vale a pena chamar a atenção. Se o tipo de construtor for acidentalmente deixado do lado direito do sinal de igual, o lado direito agora conterá quatro expressões, separadas por três vírgulas.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



O operador vírgula avalia uma expressão da esquerda para a direita. Isso reduz o lado direito para:


```
float4 x = 1; 
```



O HLSL usa promoção escalar nesse caso, portanto, o resultado é como se isso tivesse sido escrito da seguinte forma:


```
float4 x = float4(1,1,1,1);
```



Nesse caso, deixar o tipo float4 do lado direito provavelmente é um erro que o compilador não consegue detectar porque essa é uma instrução válida.

## <a name="comparison-operators"></a>Operadores de comparação

Os operadores de comparação são: <, >, ==, !=, <=, >=.

Compare valores que são maiores que (ou menores que) qualquer valor escalar:


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



Ou compare valores iguais a (ou não igual a) qualquer valor escalar:


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



Ou combine e compare valores maiores ou iguais a (ou menor ou igual a) qualquer valor escalar:


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Cada uma dessas comparações pode ser feita com qualquer tipo de dados escalar.

Para usar operadores de comparação com tipos de vetor e matriz, use a função intrínseca [**all**](dx-graphics-hlsl-all.md) ou any. [](dx-graphics-hlsl-any.md)

Essa operação falha porque a instrução if requer um único bool, mas recebe um bool4:


```
if (A4 < B4)
```



Essas operações são bem-sucedidas:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Operadores de prefixo ou pós-sufixo

Os operadores de prefixo e pós-sufixo são: ++, --. Os operadores de prefixo alteram o conteúdo da variável antes que a expressão seja avaliada. Operadores de pós-correção alteram o conteúdo da variável depois que a expressão é avaliada.

Nesse caso, um loop usa o conteúdo de i para controlar a contagem de loops.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Como o operador de incremento de pós-sufixo (++) é usado, arrayOfFloats i é multiplicado por \[ \] 2 antes de eu ser incrementado. Isso pode ser ligeiramente reorganizar para usar o operador de incremento de prefixo. Esse é mais difícil de ler, embora ambos os exemplos sejam equivalentes.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Como o operador de prefixo (++) é usado, arrayOfFloats i+1 - 1 é multiplicado por 2 depois \[ que i é \] incrementado.

O operador de decremento de decremento de prefixo e pós-sufixo (--) é aplicado na mesma sequência que o operador de incremento. A diferença é que o decremento subtrai 1 em vez de adicionar 1.

## <a name="structure-operator"></a>Operador structure

O operador de seleção de membro da estrutura (.) é um ponto. Dada esta estrutura:


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



Ela pode ser lida da seguinte maneira:


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



Cada membro pode ser lido ou gravado com o operador de estrutura:


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Operadores unários

Os operadores unários são: !, -, +

Operadores unários operam em um único operando.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Precedência de operador

Quando uma expressão contém mais de um operador, a precedência do operador determina a ordem de avaliação. A precedência do operador para HLSL segue a mesma precedência que C.

## <a name="remarks"></a>Comentários

Chaves ( ) iniciam e {,} terminam um bloco de instrução. Quando um bloco de instrução usa uma única instrução, as chaves são opcionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




