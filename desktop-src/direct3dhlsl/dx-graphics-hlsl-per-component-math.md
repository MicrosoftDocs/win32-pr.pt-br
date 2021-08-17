---
title: Per-Component operações matemáticas
description: Com o HLSL, você pode programar sombreadores em um nível de algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96181604b04e888159352e06cc15305ea5b047fda4f2e4e161b81822e64e6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513693"
---
# <a name="per-component-math-operations"></a>Per-Component operações matemáticas

Com o HLSL, você pode programar sombreadores em um nível de algoritmo. Para entender a linguagem, você precisará saber como declarar variáveis e funções, usar funções intrínsecas, definir tipos de dados personalizados e usar a semântica para conectar argumentos de sombreador a outros sombreadores e ao pipeline.

Depois de aprender a criar sombreadores no HLSL, você precisará aprender sobre chamadas de API para poder: compilar um sombreador para determinado hardware, inicializar constantes de sombreador e inicializar outro Estado de pipeline, se necessário.

-   [O tipo de vetor](#the-vector-type)
-   [O tipo de matriz](#the-matrix-type)
    -   [Ordenação de matriz](#matrix-ordering)
-   [Exemplos](#examples)
-   [Tópicos relacionados](#related-topics)

## <a name="the-vector-type"></a>O tipo de vetor

Um vetor é uma estrutura de dados que contém entre um e quatro componentes.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



O inteiro imediatamente após o tipo de dados é o número de componentes no vetor.

Inicializadores também podem ser incluídos nas declarações.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Como alternativa, o tipo de vetor pode ser usado para fazer as mesmas declarações:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



O tipo de vetor usa colchetes angulares para especificar o tipo e o número de componentes.

Os vetores contêm até quatro componentes, cada um deles pode ser acessado usando um dos dois conjuntos de nomes:

-   O conjunto de posições: x, y, z, w
-   O conjunto de cores: r, g, b, a

Essas instruções retornam o valor no terceiro componente.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



Os conjuntos de nomenclatura podem usar um ou mais componentes, mas não podem ser misturados.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



A especificação de um ou mais componentes de vetor ao ler os componentes é chamada de swizzling. Por exemplo:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



O mascaramento controla quantos componentes são gravados.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



As atribuições não podem ser gravadas no mesmo componente mais de uma vez. Portanto, o lado esquerdo desta instrução é inválido:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Além disso, os espaços de nome de componente não podem ser misturados. Esta é uma gravação de componente inválida:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



Acessar um vetor como um escalar acessará o primeiro componente do vetor. As duas instruções a seguir são equivalentes.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>O tipo de matriz

Uma matriz é uma estrutura de dados que contém linhas e colunas de dados. Os dados podem ser qualquer um dos tipos de dados escalares, no entanto, cada elemento de uma matriz é do mesmo tipo de dados. O número de linhas e colunas é especificado com a cadeia de caracteres de linha por coluna que é anexada ao tipo de dados.


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



O número máximo de linhas ou colunas é 4; o número mínimo é 1.

Uma matriz pode ser inicializada quando ela é declarada:


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Ou, o tipo de matriz pode ser usado para fazer as mesmas declarações:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



O tipo de matriz usa os colchetes angulares para especificar o tipo, o número de linhas e o número de colunas. Este exemplo cria uma matriz de ponto flutuante, com duas linhas e duas colunas. Qualquer um dos tipos de dados escalares pode ser usado.

Essa declaração define uma matriz de valores float (números de ponto flutuante de 32 bits) com duas linhas e três colunas:


```
matrix <float, 2, 3> fFloatMatrix;
```



Uma matriz contém valores organizados em linhas e colunas, que podem ser acessadas usando o operador de estrutura "." seguido por um dos dois conjuntos de nomes:

-   A posição da coluna de linha com base em zero:
    -   \_M00, \_ M01, \_ M02, \_ M03
    -   \_M10, \_ M11, \_ M12, \_ M13
    -   \_M20, \_ M21, \_ M22, \_ M23
    -   \_M30, \_ M31, \_ M32, \_ M33
-   A posição da coluna de linha baseada em um:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Cada conjunto de nomenclatura começa com um sublinhado seguido pelo número da linha e o número da coluna. A convenção baseada em zero também inclui a letra "m" antes do número da linha e da coluna. Aqui está um exemplo que usa os dois conjuntos de nomes para acessar uma matriz:


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



Assim como os vetores, os conjuntos de nomes podem usar um ou mais componentes de um conjunto de nomes.


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



Uma matriz também pode ser acessada usando a notação de acesso de matriz, que é um conjunto de índices baseado em zero. Cada índice está dentro de colchetes. Uma matriz 4x4 é acessada com os seguintes índices:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]
-   \[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]
-   \[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]

Aqui está um exemplo de acesso a uma matriz:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Observe que o operador de estrutura "." não é usado para acessar uma matriz. A notação de acesso à matriz não pode usar swizzling para ler mais de um componente.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



No entanto, o acesso à matriz pode ler um vetor de vários componentes.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Assim como acontece com os vetores, a leitura de mais de um componente de matriz é chamada de swizzling. Mais de um componente pode ser atribuído, pressupondo que apenas um espaço de nome seja usado. Estas são todas as atribuições válidas:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



O mascaramento controla quantos componentes são gravados.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



As atribuições não podem ser gravadas no mesmo componente mais de uma vez. Portanto, o lado esquerdo desta instrução é inválido:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Além disso, os espaços de nome de componente não podem ser misturados. Esta é uma gravação de componente inválida:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Ordenação de matriz

Ordem de embalagem de matriz para parâmetros uniformes é definido como coluna-principal por padrão. Isso significa que cada coluna da matriz é armazenada em um único registro constante. Por outro lado, uma matriz de linha principal empacota cada linha da matriz em um único registro constante. A embalagem de matriz pode ser alterada com a diretiva de **\# \_ matriz pragmapack** ou com a **linha \_ principal** ou a palavra-chave **\_ Major da coluna** .

Os dados em uma matriz são carregados em registros de constante de sombreador antes de um sombreador ser executado. Há duas opções de como os dados da matriz são lidos: na ordem principal da linha ou na ordem principal da coluna. Coluna-a ordem principal significa que cada coluna de matriz será armazenada em um único registro de constante e a ordem de principal de linha significa que cada linha da matriz será armazenada em um único registro constante. Essa é uma consideração importante para quantos registros constantes são usados para uma matriz.

Uma matriz de linha principal é disposta da seguinte maneira:

:::row:::
    :::column:::
        11<br/>
        21<br/>
        31<br/>
        41<br/>
    :::column-end:::
    :::column:::
        12<br/>
        22<br/>
        32<br/>
        42<br/>
    :::column-end:::
    :::column:::
        13<br/>
        23<br/>
        33<br/>
        43<br/>
    :::column-end:::
    :::column:::
        14<br/>
        24<br/>
        34<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Uma matriz de coluna principal é disposta da seguinte maneira:


:::row:::
    :::column:::
        11<br/>
        12<br/>
        13<br/>
        14<br/>
    :::column-end:::
    :::column:::
        21<br/>
        22<br/>
        23<br/>
        24<br/>
    :::column-end:::
    :::column:::
        31<br/>
        32<br/>
        33<br/>
        34<br/>
    :::column-end:::
    :::column:::
        41<br/>
        42<br/>
        43<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Classificação de matriz de linha principal e coluna-principal determine a ordem em que os componentes de matriz são lidos de entradas de sombreador. Depois que os dados são gravados em registros constantes, a ordem de matriz não tem nenhum efeito sobre como os dados são usados ou acessados no código do sombreador. Além disso, as matrizes declaradas em um corpo de sombreador não são incluídas em registros constantes. A ordem de embalagem de linha principal e coluna-principal não tem influência sobre a ordem de embalagem dos construtores (que sempre segue a ordenação da linha principal).

A ordem dos dados em uma matriz pode ser declarada no momento da compilação ou o compilador solicitará os dados em tempo de execução para o uso mais eficiente.

## <a name="examples"></a>Exemplos

O HLSL usa dois tipos especiais, um tipo de vetor e um tipo de matriz para facilitar a programação de gráficos 2D e 3D. Cada um desses tipos contém mais de um componente; um vetor contém até quatro componentes, e uma matriz contém até 16 componentes. Quando vetores e matrizes são usados em equações HLSLs padrão, a matemática realizada é projetada para funcionar por componente. Por exemplo, HLSL implementa essa multiplicação:


```
float4 v = a*b;
```



como uma multiplicação de quatro componentes. O resultado é quatro escalares:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



São quatro multiplicações em que cada resultado é armazenado em um componente separado do v. Isso é chamado de multiplicação de quatro componentes. O HLSL usa a matemática do componente, o que torna os sombreadores de escrita muito eficientes.

Isso é muito diferente de uma multiplicação, que normalmente é implementada como um produto de ponto que gera um único escalar:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Uma matriz também usa operações por componente em HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



O resultado é uma multiplicação por componente das duas matrizes (em oposição a uma multiplicação padrão de matriz 3x3). Uma multiplicação por matriz de componente produz esse primeiro termo:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Isso é diferente de uma multiplicação de matriz 3x3 que produziria esse primeiro termo:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Versões sobrecarregadas da função intrínseca de multiplicação tratam casos em que um operando é um vetor e o outro operando é uma matriz. Como: \* vetor de vetor, \* matriz de vetor, \* vetor de matriz e \* matriz de matriz. Por exemplo:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



produz o mesmo resultado que:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



Este exemplo converte o vetor de pos em um vetor de coluna usando a conversão (float1x4). A alteração de um vetor por meio da conversão ou troca da ordem dos argumentos fornecidos para multiplicar é equivalente a transposição da matriz.

Conversão de conversão automática faz com que as funções de multiplicação e de ponto intrínsecos retornem os mesmos resultados usados aqui:


```
{
  float4 val;
  return mul(val,val);
}
```



Esse resultado da multiplicação é um \* 4x = 1x1 vector. Isso é equivalente a um produto de ponto:


```
{
  float4 val;
  return dot(val,val);
}
```



que retorna um único valor escalar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




