---
title: Descritores de correlação
description: Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão com base em um argumento relacionado a outro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbbeb682a7c558cd8c45050d27ea9bf64c39016a056a88566aef7048f3c0d610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022347"
---
# <a name="correlation-descriptors"></a>Descritores de correlação

Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão com base em um argumento relacionado a outro argumento. Um descritor de correlação é necessário para lidar com a semântica relacionada a atributos como \[ **\_ size is()** \] , length \[ **\_ is()** \] , switch \[ **\_ is()** \] e \[ **iid \_ is()** \] . Descritores de correlação são usados com matrizes, ponteiros dimensionado, uniões e ponteiros de interface. O valor da expressão eventual pode ser um tamanho, um comprimento, um discriminante de união ou um ponteiro para um IID, respectivamente. Em termos de cadeias de caracteres de formato, os descritores de correlação são usados com matrizes, uniões e ponteiros de interface. Um ponteiro dimensionado é descrito em cadeias de caracteres de formato como um ponteiro para uma matriz.

Há duas rotinas que executam cálculos básicos de expressão: NdrpComputeConformance é usado para tamanhos, opções e IID, enquanto \* NdrpComputeVariance é usado para comprimentos. Também há uma única rotina para executar uma validação de valor de correlação para a funcionalidade de negação de ataque.

Descritores de correlação foram projetados para dar suporte apenas a expressões muito limitadas. Para situações complicadas, o compilador gera uma rotina de avaliação de expressão a ser chamada pelo mecanismo quando necessário.

Um descritor de correlação tem o seguinte formato:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

O tipo de correlação do descritor de correlação<1> consiste em duas nibbles: os 4 bits superiores descrevem onde a expressão pode ser encontrada e os 4 bits inferiores descrevem o tipo do valor da \_ expressão.

A nibble superior pode ter um destes cinco valores:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>CONFORMIDADE \_ NORMAL \_ DO FC
</dt> <dd>

Um caso normal de conformidade, como descrito em um campo de uma estrutura.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>CONFORMIDADE \_ COM O PONTEIRO DO \_ FC
</dt> <dd>

Para ponteiros atribuídos **(size \_ is()**, **length \_ is()**) que são campos em uma estrutura. Isso afeta a maneira como o ponteiro de memória base é definido.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>CONFORMIDADE \_ DE NÍVEL SUPERIOR DO \_ \_ FC
</dt> <dd>

Para conformidade de nível superior descrita por outro parâmetro.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>CONFORMIDADE \_ COM A EQUIPE DE NÍVEL SUPERIOR DO \_ \_ \_ FC
</dt> <dd>

Para conformidade de nível superior de uma matriz multidimensional descrita por outro parâmetro.

> [!Note]  
> Ponteiros e matrizes de tamanho multidimensional disparam uma opção para [**–Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMIDADE \_ CONSTANTE \_ DO FC
</dt> <dd>

Para um valor constante. O compilador pré-compila o valor de uma expressão constante fornecida pelo usuário. Quando esse é o caso, os 3 bytes subsequentes na descrição de conformidade contêm os 3 bytes inferiores de um longo que descrevem o tamanho da conformidade. Não é necessário nenhum cálculo posterior.

</dd> </dl>

A nibble inferior fornece o tipo do valor que precisa ser extraído da memória:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> Não há suporte para expressões de 64 bits. FC \_ HYPER é usado somente para **iid \_ is()** em plataformas de 64 bits para extrair o valor do ponteiro para IID. \*
>
> O compilador define o tipo nibble como zero para os seguintes casos: expressão constante mencionada acima e quando a rotina de expressão de avaliação precisa ser chamada, por exemplo, quando FC CONSTANT CONFORMANCE e FC CALLBACK são \_ \_ \_ usados.

 

O tamanho é op<um campo> permite que uma das seguintes operações seja aplicada à \_ \_ variável de conformidade:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

A constante FC DEREFERENCE é usada para correlação sendo um pointee, como para \_ **\[ \_ size is( \* pL). \]** Os operadores aritméticos usam apenas a constante indicada. A constante \_ FC CALLBACK indica que uma rotina de avaliação de expressão precisa ser chamada.

O deslocamento<campo 2> normalmente é um deslocamento de memória relativo para a variável de argumento de expressão. Ele também pode ser um índice de avaliação de expressão– rotina. Conforme mencionado anteriormente neste documento, para expressões constantes, ele faz parte do valor real da expressão final.

A interpretação do campo de deslocamento<2> como deslocamento de memória depende da complexidade da expressão, do local da variável de expressão e, no caso de uma matriz, se a matriz é, na verdade, um ponteiro atribuído.

Se a matriz for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do início da estrutura para o campo que descreve a conformidade. Se a matriz não for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do final da parte não compatível da estrutura para o campo que descreve a conformidade. Normalmente, a matriz compatível está no final da estrutura.

Para conformidade de nível superior, o campo de deslocamento contém o deslocamento do local do primeiro parâmetro do stub na pilha para o parâmetro que descreve a conformidade. Isso não é usado no **modo –Os.** Há outras exceções à interpretação do campo de deslocamento; essas exceções são descritas na descrição desses tipos.

Quando o deslocamento<2> é usado com FC CALLBACK, ele contém um índice na tabela de rotina de avaliação de expressão \_ gerada pelo compilador. A mensagem stub é passada para a rotina de avaliação, que calcula o valor de conformidade e o atribui ao campo MaxCount da mensagem de stub.

Os sinalizadores robustos<campo> 2 foram adicionados para o Windows 2000 para dar suporte a /robust , como o recurso de negação de \_ ataques. [](/windows/desktop/Midl/-robust) Os seguintes sinalizadores são definidos no primeiro byte:

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

O sinalizador Early indica correlação antecipada versus tardia. Uma correlação antecipada é quando o argumento de expressão precede o argumento descrito, por exemplo, um argumento de tamanho é antes de um argumento de ponteiro dimensionado. Uma correlação tardia é quando o argumento de expressão vem após o argumento relacionado. O mecanismo executa a validação de valores de correlação antecipados imediatamente, os valores de correlação tardia são armazenados para verificação depois que o desmarque é feito.

O sinalizador Split indica uma divisão assíncrona entre \[ \] argumentos in e \[ \] out. Por exemplo, um argumento de tamanho pode \[ estar em enquanto o ponteiro \] dimensionado pode estar fora \[ \] . No contexto assíncrono do DCOM, esses argumentos estão em pilhas diferentes, portanto, o mecanismo deve estar ciente disso.

O sinalizador IsIidIs indica uma correlação **iid \_ is().** A rotina NdrComputeConformance é complicada para obter um ponteiro para IID como um valor de expressão, mas a rotina de validação não pode comparar esses valores (eles seriam ponteiros) e, portanto, o sinalizador indica que os IIDs reais precisam ser comparados.

### <a name="variance-description-and-other-array-attributes"></a>Descrição de variação e outros atributos de matriz

O formato do campo de descrição de variância é idêntico ao campo de descrição de conformidade. A diferença é que um campo de mensagem de stub diferente é usado pelo mecanismo NDR como uma variável temporária. No caso da descrição da variância, é o comprimento avaliado e o campo correspondente é chamado ActualLength.

Com a variação, o deslocamento inicial normalmente é zero e o mecanismo é ajustado de acordo. Se o **primeiro \_ atributo is()** for aplicado a uma matriz variável compatível, um retorno de chamada para uma rotina de avaliação de expressão será forçado.

 

 