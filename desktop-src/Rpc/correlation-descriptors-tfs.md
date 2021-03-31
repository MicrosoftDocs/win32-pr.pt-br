---
title: Descritores de correlação
description: Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão baseada em um argumento relacionado a outro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823954"
---
# <a name="correlation-descriptors"></a>Descritores de correlação

Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão baseada em um argumento relacionado a outro argumento. Um descritor de correlação é necessário para lidar com semânticas relacionadas a atributos como o \[ **tamanho \_ é ()** \] , \[ **length \_ is ()** \] , \[ **switch \_ is ()** \] e \[ **IID \_ is ()** \] . Os descritores de correlação são usados com matrizes, ponteiros de tamanho, uniões e ponteiros de interface. O valor da expressão eventual pode ser um tamanho, um comprimento, um discriminante de União ou um ponteiro para um IID, respectivamente. Em termos de cadeias de caracteres de formato, os descritores de correlação são usados com matrizes, uniões e ponteiros de interface. Um ponteiro de tamanho é descrito em Formatar cadeias de caracteres como um ponteiro para uma matriz.

Há duas rotinas executando cálculos de expressão básicos: NdrpComputeConformance é usado para tamanhos, switches e IID \* enquanto NdrpComputeVariance é usado para comprimentos. Também há uma única rotina para executar uma validação de valor de correlação para a funcionalidade de negação de ataque.

Os descritores de correlação foram projetados para dar suporte apenas a expressões muito limitadas. Para situações complicadas, o compilador gera uma rotina de avaliação de expressão a ser chamada pelo mecanismo quando necessário.

Um descritor de correlação tem o seguinte formato:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

O tipo de correlação do descritor de correlação \_<1> consiste em dois Nibbles: os quatro bits superiores descrevem onde a expressão pode ser encontrada e os quatro bits inferiores descrevem o tipo do valor da expressão.

O Nibble superior pode ter um destes cinco valores:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformidade normal com FC \_
</dt> <dd>

Um caso de conformidade normal, como o descrito em um campo de uma estrutura.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformidade do ponteiro FC \_
</dt> <dd>

Para ponteiros atribuídos (o **tamanho \_ é ()**, **length \_ is ()**), que são campos em uma estrutura. Isso afeta a maneira como o ponteiro de memória base é definido.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformidade de \_ nível \_ superior de FC
</dt> <dd>

Para conformidade de nível superior descrita por outro parâmetro.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformidade múltipla de nível superior \_ de FC \_
</dt> <dd>

Para conformidade de nível superior de uma matriz multidimensional descrita por outro parâmetro.

> [!Note]  
> Os ponteiros e as matrizes com dimensionamento multidimensional disparam um comutador para [**– Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>\_conformidade da constante de FC \_
</dt> <dd>

Para um valor constante. O compilador precalcula o valor de uma expressão constante fornecida pelo usuário. Quando esse for o caso, os 3 bytes subsequentes na descrição de conformidade conterão os 3 bytes inferiores de um longo que descreve o tamanho de conformidade. Nenhuma computação adicional é necessária.

</dd> </dl>

O Nibble inferior fornece o tipo do valor que precisa ser extraído da memória:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> Não há suporte para expressões de 64 bits. O FC \_ Hyper é usado apenas para **IID \_ é ()** em plataformas de 64 bits para extrair o valor do ponteiro para IID \* .
>
> O compilador define o tipo Nibble como zero para os seguintes casos: expressão constante mencionada acima e quando a rotina de expressão de avaliação precisa ser chamada, por exemplo, quando a conformidade com a \_ constante FC \_ e o \_ retorno de chamada FC são usados.

 

O tamanho \_ é \_ op<1> campo permite que uma das seguintes operações seja aplicada à variável de conformidade:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

A \_ constante de desreferência de FC é usada para que a correlação seja um ponto, como para o **\[ tamanho \_ é ( \* pl) \]**. Os operadores aritméticos usam apenas a constante indicada. A \_ constante de retorno de chamada FC indica que uma rotina de avaliação de expressão precisa ser chamada.

O campo deslocamento<2> normalmente é um deslocamento de memória relativo para a variável de argumento de expressão. Ele também pode ser uma avaliação de expressão – índice de rotina. Conforme mencionado anteriormente neste documento, para expressões constantes ele faz parte do valor real e final da expressão.

A interpretação do deslocamento<2> campo como deslocamento de memória depende da complexidade da expressão, do local da variável de expressão e, no caso de uma matriz, se a matriz é, na verdade, um ponteiro atribuído.

Se a matriz for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do início da estrutura até o campo conformidade-descrição. Se a matriz não for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do final da parte não compatível da estrutura para o campo conformidade-descrever. Normalmente, a matriz em conformidade está no final da estrutura.

Para conformidade de nível superior, o campo de deslocamento contém o deslocamento do local do primeiro parâmetro do stub na pilha para o parâmetro que descreve a conformidade. Isso não é usado no modo **– os** . Há outras exceções à interpretação do campo de deslocamento; essas exceções são descritas na descrição desses tipos.

Quando o deslocamento<2> é usado com \_ o retorno de chamada FC, ele contém um índice na tabela de rotina de avaliação de expressão gerada pelo compilador. A mensagem de stub é passada para a rotina de avaliação, que computa o valor de conformidade e o atribui ao campo MaxCount da mensagem de stub.

O campo de sinalizadores robustos \_<2> foi adicionado ao Windows 2000 para dar suporte a [**/robust**](/windows/desktop/Midl/-robust), como o recurso de negação de ataques. Os seguintes sinalizadores são definidos no primeiro byte:

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

O sinalizador inicial indica a correlação antecipada versus tardia. Uma correlação inicial é quando o argumento da expressão precede o argumento descrito, por exemplo, um argumento de tamanho é anterior a um argumento de ponteiro de tamanho. Uma correlação tardia é quando o argumento da expressão vem após o argumento relacionado. O mecanismo executa a validação dos valores de correlação iniciais imediatamente, os valores de correlação tardias são armazenados para verificação após a conclusão do desempacotamento.

O sinalizador Split indica uma divisão assíncrona entre os \[ \] argumentos in e \[ out \] . Por exemplo, um argumento de tamanho pode estar \[ no \] enquanto o ponteiro de tamanho pode estar \[ fora \] . No contexto assíncrono do DCOM, esses argumentos ocorrem em pilhas diferentes, portanto, o mecanismo deve estar ciente disso.

O sinalizador IsIidIs indica uma correlação de **IID \_ ()** . A rotina NdrComputeConformance é induzida a obter um ponteiro para o IID como um valor de expressão, mas a rotina de validação não pode comparar esses valores (eles seriam ponteiros) e, portanto, o sinalizador indica que o IIDs real precisa ser comparado.

### <a name="variance-description-and-other-array-attributes"></a>Descrição da variância e outros atributos de matriz

O formato do campo de descrição da variação é idêntico ao campo de descrição de conformidade. A diferença é que um campo de mensagem de stub diferente é usado pelo mecanismo de NDR como uma variável temporária. No caso da descrição da variação, é o comprimento que é avaliado e o campo correspondente é chamado de ActualLength.

Com a variação, o deslocamento inicial geralmente é zero e o mecanismo é ajustado de acordo. Se o **primeiro atributo \_ is ()** for aplicado a uma matriz de variação em conformidade, um retorno de chamada para uma rotina de avaliação de expressão será forçado.

 

 