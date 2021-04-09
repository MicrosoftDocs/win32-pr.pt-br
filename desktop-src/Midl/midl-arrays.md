---
title: Matrizes de MIDL
description: Matrizes MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipos de dados MIDL, matrizes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007493"
---
# <a name="midl-arrays"></a>Matrizes de MIDL

Os declaradores de matriz aparecem no corpo da interface do arquivo IDL como um dos seguintes:

-   Parte de uma declaração geral
-   Um membro de um Declarador de estrutura ou União
-   Um parâmetro para uma chamada de procedimento remoto

Os limites de cada dimensão da matriz são expressos dentro de um par separado de colchetes. Uma expressão que é avaliada como *n* significa um limite inferior de zero e um limite superior de *n-1*. Se os colchetes estiverem vazios ou contiverem um único asterisco ( \* ), o limite inferior será zero e o limite superior será determinado em tempo de execução.

A matriz também pode conter dois valores separados por uma elipse que representa os limites inferior e superior da matriz, como em \[ *minúsculas*... *superior* \] . O Microsoft RPC requer um limite inferior de zero. O compilador MIDL não reconhece construções que especificam limites inferiores diferentes de zero.

As matrizes podem ser associadas com o [**tamanho \_**](size-is.md)dos atributos de campo is, [**Max \_ is**](max-is.md), [**length \_**](length-is.md)is, [**First \_ is**](first-is.md)e [**Last \_ é**](last-is.md) especificar o tamanho da matriz ou a parte da matriz que contém dados válidos. Esses atributos de campo identificam o parâmetro, o campo de estrutura ou a constante que especifica a dimensão ou o índice da matriz.

A matriz deve ser associada ao identificador especificado pelo atributo Field da seguinte maneira: quando a matriz é um parâmetro, o identificador também deve ser um parâmetro para a mesma função; Quando a matriz é um campo de estrutura, o identificador deve ser outro campo de estrutura da mesma estrutura.

Uma matriz é chamada de "compatível" se o limite superior de qualquer dimensão for determinado em tempo de execução. (Somente os limites superiores podem ser determinados em tempo de execução.) Para determinar o limite superior, a declaração de matriz deve incluir um atributo [**Size \_ is**](size-is.md) ou [**Max \_ is**](max-is.md) .

Uma matriz é chamada de "variação" quando seus limites são determinados em tempo de compilação, mas o intervalo de elementos transmitidos é determinado em tempo de execução. Para determinar o intervalo de elementos transmitidos, a declaração de matriz deve incluir um comprimento, o [**primeiro \_ é**](first-is.md), ou o [**último \_ é**](last-is.md) o atributo. [**\_**](length-is.md)

Uma matriz de variação em conformidade (também chamada de "aberta") é uma matriz cujo limite superior e o intervalo de elementos transmitidos são determinados em tempo de execução. No máximo, uma matriz de variável compatível ou compatível pode ser aninhada em uma estrutura C e deve ser o último elemento da estrutura. Por outro lado, matrizes de variação não compatíveis podem ocorrer em qualquer lugar em uma estrutura.

## <a name="examples"></a>Exemplos

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

Para obter mais informações, consulte [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Matrizes multidimensionais

O usuário pode declarar tipos que são matrizes e, em seguida, declarar matrizes de objetos desses tipos. A semântica de matrizes *m* bidimensionais de tipos de matriz *n*-dimensional é igual à *semântica de* + matrizes *n*-dimensional.

Por exemplo, o tipo RECT tipo \_ pode ser definido como uma matriz bidimensional e a variável *Rect* pode ser definida como uma matriz do \_ tipo Rect. Isso é equivalente à matriz tridimensional de *\_ retângulo equivalente*:

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

O Microsoft RPC é orientado a C. Seguindo as convenções de linguagem C, somente a primeira dimensão de uma matriz multidimensional pode ser determinada em tempo de execução. A interoperação com matrizes de IDL do DCE que dão suporte a outras linguagens é limitada a:

-   Matrizes multidimensionais com limites constantes (de tempo de compilação).
-   Matrizes multidimensionais com todos os limites de constante, exceto a primeira dimensão. O limite superior e o intervalo de elementos transmitidos da primeira dimensão dependem do tempo de execução.
-   Qualquer matriz unidimensional com um limite inferior de zero.

Quando o **\[** atributo de [**cadeia de caracteres**](string.md) **\]** é usado em matrizes multidimensionais, o atributo se aplica à matriz mais à direita.

## <a name="arrays-of-pointers"></a>Matrizes de ponteiros

Os ponteiros de referência devem apontar para dados válidos. O aplicativo cliente deve alocar toda a memória para uma **\[** matriz [**in**](in.md) **\]** ou **\[** **in,**[**fora**](out-idl.md) **\]** de ponteiros de referência, especialmente quando a matriz está associada aos valores **\[ in \]**, **\[** **in, out \]**, **\[** [**length \_**](length-is.md) **\]** ou **\[** [**Last \_ is**](last-is.md) **\]** . O aplicativo cliente também deve inicializar todos os elementos da matriz antes da chamada. Antes de retornar ao cliente, o aplicativo de servidor deve verificar se todos os elementos de matriz no intervalo transmitido apontam para um armazenamento válido.

No lado do servidor, o stub aloca armazenamento para todos os elementos da matriz, independentemente do **\[** [**comprimento \_**](length-is.md) **\]** ou do **\[** [**último \_**](last-is.md) **\]** valor no momento da chamada. Esse recurso pode afetar o desempenho do seu aplicativo.

Nenhuma restrição é colocada em matrizes de ponteiros exclusivos. No cliente e no servidor, o armazenamento é alocado para ponteiros nulos. Quando os ponteiros são não nulos, os dados são colocados no armazenamento pré-alocado.

Um Declarador de ponteiro opcional pode preceder o Declarador de matriz.

Quando ponteiros de referência inseridos são **\[** [](out-idl.md) **\]** parâmetros somente out, o código do Gerenciador de servidores deve atribuir valores válidos à matriz de ponteiros de referência. Por exemplo:

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

Os stubs gerados alocam a matriz e atribuem valores nulos a todos os ponteiros inseridos na matriz.

 

 