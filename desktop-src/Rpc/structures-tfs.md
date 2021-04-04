---
title: Estruturas (RPC)
description: Descrição de vários tipos de estruturas na RPC (chamada de procedimento remoto).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007893"
---
# <a name="structures-rpc"></a>Estruturas (RPC)

Há várias categorias de estruturas, progressivamente mais complicadas em termos de ações necessárias para o marshaling. Eles começam com uma estrutura simples que pode ser copiada em bloco como um todo e continuam em uma estrutura complexa que deve ser atendida em campo por campo.

-   [Estrutura simples](#simple-structure)
-   [Estrutura simples com ponteiros](#simple-structure-with-pointers)
-   [Estrutura de conformidade](#conformant-structure)
-   [Estrutura compatível com ponteiros](#conformant-structure-with-pointers)
-   [Estrutura variável em conformidade (com ou sem ponteiros)](#conformant-varying-structure-with-or-without-pointers)
-   [Estrutura rígida](#hard-structure)
-   [Estrutura complexa](#complex-structure)
-   [Descrição do layout do membro da estrutura](#structure-member-layout-description)

> [!Note]  
> Quando comparada às categorias de matriz, fica claro que apenas estruturas de até 64K podem ser descritas (o tamanho é para a parte plana da estrutura), ou seja, não há equivalente a matrizes SM e LG.

 

**Membros comuns a estruturas**

-   **sintonia**

    O alinhamento necessário do buffer antes de desempacotar a estrutura. Os valores válidos são 0, 1, 3 e 7 (o alinhamento real menos 1).

-   **tamanho da memória \_**

    Tamanho da estrutura na memória em bytes; para estruturas em conformidade, esse tamanho não inclui o tamanho da matriz.

-   **deslocamento \_ da \_ Descrição da matriz \_**

    Deslocamento do ponteiro da cadeia de caracteres de formato atual para a descrição da matriz em conformidade contida em uma estrutura.

-   **layout do membro \_**

    Descrição de cada elemento da estrutura. As rotinas de NDR só precisam examinar essa parte da cadeia de caracteres de formato de um tipo se a transformação endian for necessária ou se o tipo for uma estrutura complexa.

-   **layout do ponteiro \_**

    Consulte a seção [layout do ponteiro](pointer-layout-tfs.md) .

## <a name="simple-structure"></a>Estrutura simples

Uma estrutura simples contém apenas tipos base, matrizes fixas e outras estruturas simples. O principal recurso da estrutura simples é que ele pode ser copiado em bloco como um todo.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Estrutura simples com ponteiros

Uma estrutura simples com ponteiros contém apenas tipos base, ponteiros, matrizes fixas, estruturas simples e outras estruturas simples com ponteiros. Como o layout<> só precisará ser visitado ao fazer uma conversão endianess, ele será colocado no final da descrição.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Estrutura de conformidade

Uma estrutura compatível contém apenas tipos base, matrizes fixas e estruturas simples e deve conter uma cadeia de caracteres de conformidade ou uma matriz compatível. Essa matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros que são inseridos nessa estrutura.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Estrutura compatível com ponteiros

Uma estrutura compatível com ponteiros contém apenas tipos base, ponteiros, matrizes fixas, estruturas simples e estruturas simples com ponteiros; uma estrutura compatível deve conter uma matriz compatível. Essa matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros inseridos nessa estrutura.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Estrutura variável em conformidade (com ou sem ponteiros)

Uma estrutura de variação em conformidade contém apenas tipos simples, ponteiros, matrizes fixas, estruturas simples e estruturas simples com ponteiros; uma estrutura de variação em conformidade deve conter uma cadeia de caracteres de conformidade ou uma matriz de variação variável. A cadeia de caracteres de conformidade ou a matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros inseridos nessa estrutura.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Estrutura rígida

A estrutura sólida era um conceito destinado à eliminação de penalidades acentuadas relacionadas ao processamento de estruturas complexas. Ele é derivado de uma observação de que uma estrutura complexa normalmente tem apenas uma ou duas condições que impedem a cópia de bloco e, portanto, estragam seu desempenho em comparação com uma estrutura simples. Os culpados geralmente são campos de União ou de enumeração.

Uma estrutura rígida é uma estrutura que tem um enum16, um preenchimento de extremidade na memória ou uma União como o último membro. Esses três elementos impedem que a estrutura caia em uma das categorias de estrutura anteriores, o que aproveita sobrecarga de interpretação pequena e potencial máximo de otimização, mas não a força na categoria de estrutura complexa muito dispendiosa.

O enum16 não deve fazer com que a memória e os tamanhos de conexão da estrutura sejam diferentes. A estrutura não pode ter nenhuma matriz compatível nem ponteiros (a menos que parte da União); os únicos outros membros permitidos são tipos base, matrizes fixas e estruturas simples.

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

O \_ campo deslocamento de enumeração<2> fornece o deslocamento do início da estrutura na memória para um enum16 se ele contiver um; caso contrário, o campo de deslocamento de enumeração \_<2> será – 1.

O \_ campo tamanho da cópia<2> fornece o número total de bytes na estrutura, que podem ser copiados em bloco em/do buffer. Esse total não inclui nenhuma União à direita nem qualquer preenchimento de extremidade na memória. Esse valor também é a quantidade que o ponteiro de buffer deve ser incrementado após a cópia.

O \_ campo incr de cópia do mem \_<2> é o número de bytes que o ponteiro de memória deve ser incrementado após a cópia de bloco antes de manipular qualquer União à direita. Incrementar por esse valor (não pelo tamanho da cópia \_<2> bytes) produz um ponteiro de memória adequado para qualquer União à direita.

## <a name="complex-structure"></a>Estrutura complexa

Uma estrutura complexa é qualquer estrutura que contenha um ou mais campos que impeçam que a estrutura seja copiada em bloco ou para a qual verificação adicional deve ser executada durante o marshaling ou o desempacotamento (por exemplo, verificações associadas em uma enumeração). Os seguintes tipos de NDR estão nesta categoria:

-   [tipos simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (somente em plataformas de 64 bits), um integral com \[ [ **intervalo**](/windows/desktop/Midl/range)\]
-   preenchimento de alinhamento no final da estrutura
-   ponteiros de interface (eles vão usar um complexo incorporado)
-   ponteiros ignorados (relacionados ao \[ atributo [**ignore**](/windows/desktop/Midl/ignore) \] e ao \_ token de ignorar FC)
-   matrizes complexas, matrizes variáveis, matrizes de cadeia de caracteres
-   matrizes de conformidade multidimensional com pelo menos uma dimensão não fixa
-   uniões
-   elementos definidos com \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**representar \_ como**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ empacotamento de conexão**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ Marshal do usuário**](/windows/desktop/Midl/user-marshal)\]
-   estruturas complexas inseridas
-   preenchimento no final da estrutura

Uma estrutura complexa tem a seguinte descrição de formato:

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

O tamanho da memória \_<2> campo é o tamanho da estrutura na memória, em bytes.

Se a estrutura contiver uma matriz em conformidade, a \_ Descrição da matriz de acordo com o \_ \_ \_<2> campo fornecerá o deslocamento para a descrição da matriz em conformidade, caso contrário, será zero.

Se a estrutura tiver ponteiros, o deslocamento \_ para o \_ \_ layout do ponteiro<2> campo fornecerá o deslocamento além do layout da estrutura para o layout do ponteiro, caso contrário, esse campo será zero.

O \_ layout do ponteiro<> campo de uma estrutura complexa é tratado de maneira um pouco diferente do que para outras estruturas. O layout do ponteiro \_<> campo de uma estrutura complexa só contém descrições dos campos de ponteiro reais na própria estrutura. Todos os ponteiros contidos em quaisquer matrizes, uniões ou estruturas incorporadas não são descritos no campo<> layout de ponteiro da estrutura complexa \_ .

> [!Note]  
> Isso é diferente de outras estruturas, que duplicam a descrição de quaisquer ponteiros contidos em matrizes ou estruturas inseridas em seu próprio layout de ponteiro \_<> campo também.

 

O formato de um layout de ponteiro de estrutura complexa também é radicalmente diferente. Como ele contém apenas descrições de membros reais de ponteiro e porque uma estrutura complexa é empacotada e não empacotada um campo por vez, o layout do ponteiro \_<> campo simplesmente contém a descrição do ponteiro de todos os membros do ponteiro. Não há um FC \_ PP inicial e nenhum dos layouts de ponteiro usuais \_<> informações.

## <a name="structure-member-layout-description"></a>Descrição do layout do membro da estrutura

A descrição do layout de uma estrutura contém um ou mais dos seguintes caracteres de formato:

-   Qualquer um dos caracteres de tipo base, como FC \_ Char e assim por diante
-   Diretivas de alinhamento. Há três caracteres de formato que especificam o alinhamento do ponteiro de memória: FC \_ ALIGNM2, FC \_ ALIGNM4 e FC \_ ALIGNM8.
    > [!Note]  
    > Também há tokens de alinhamento de buffer, FC \_ ALIGNB2 por meio de \_ ALIGNM8 FC; eles não são usados.

     

-   Enchimento da memória. Elas ocorrem apenas no final da descrição de uma estrutura e denotam o número de bytes de preenchimento na memória antes da matriz em conformidade na estrutura: FC \_ STRUCTPADn, em que n é o número de bytes de preenchimento.
-   Qualquer tipo não base inserido (Observe, no entanto, que uma matriz em conformidade nunca ocorre no layout da estrutura). Isso tem uma descrição de 4 bytes:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    em que não há garantia de que o deslocamento seja alinhado em 2 bytes.

    \_o controle de memória<1> é um preenchimento necessário na memória antes do campo complexo.

    \_o deslocamento para a \_ Descrição<2> é um deslocamento de tipo relativo para o tipo inserido.

Também pode haver um pad FC \_ antes do final do FC de terminação \_ , se necessário, para garantir que a cadeia de caracteres de formato seja alinhada a um limite de 2 bytes após a extremidade do FC \_ .

 

 