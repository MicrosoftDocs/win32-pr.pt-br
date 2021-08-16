---
title: Descritores de parâmetro
description: Conforme mencionado anteriormente, existem descritores de parâmetro de estilo \ 8211;Oi e \ 8211;Oif.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a13b052d49629333bd9cb121b4d1b661722cb3a7a69ad2a17d3e2740a0cd8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927545"
---
# <a name="parameter-descriptors"></a>Descritores de parâmetro

Conforme mencionado anteriormente, existem descritores de parâmetro de estilo [**–Oi**](/windows/desktop/Midl/-oi) e **–Oif.**

## <a name="the-oi-parameter-descriptors"></a>Os descritores de parâmetro –Oi

Stubs totalmente interpretados exigem informações adicionais para cada um dos parâmetros em uma chamada RPC. As descrições de parâmetro de um procedimento são seguidas imediatamente após a descrição do procedimento.

[**Simples –Oi**](/windows/desktop/Midl/-oi)

**Descritores de parâmetro**

O formato para a descrição de um parâmetro de tipo simples \[ **in** \] ou return é:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–ou–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Em que \_ o tipo<1> é o token FC que indica o tipo simples. Os códigos são os seguinte:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Outros –Oi**

**Descritores de parâmetro**

O formato para a descrição de todos os outros tipos de parâmetro é:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Em que a direção do<1> campo para cada uma dessas descrições deve ser uma das \_ mostradas na tabela a seguir.



| Hex | Sinalizador                          | Significado                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ IN \_ PARAM                 | Um parâmetro in.                                            |
| 50  | FC \_ IN \_ OUT \_ PARAM            | Um parâmetro in/out.                                        |
| 51  | FC \_ OUT \_ PARAM                | Um parâmetro out.                                           |
| 52  | FC \_ RETURN \_ PARAM             | Um valor de retorno de procedimento.                                   |
| 4f  | FC \_ IN \_ PARAM \_ NO \_ FREE \_ INST | Um em xmit/rep como um parâmetro para o qual nenhuma liberação é feita. |



 

O tamanho da pilha<1> é o tamanho do parâmetro na pilha, expresso como o número de inteiros que o parâmetro ocupa \_ na pilha.

> [!Note]  
> Não há suporte para o modo [**–Oi**](/windows/desktop/Midl/-oi) em plataformas de 64 bits.

 

O deslocamento de tipo<campo 2> é o deslocamento na tabela de cadeia de caracteres de formato de tipo, indicando o descritor de tipo \_ para o argumento .

## <a name="the-oif-parameter-descriptors"></a>Os descritores de parâmetro –Oif

Há dois formatos possíveis para uma descrição de parâmetro, um para tipos base, outro para todos os outros tipos.

Tipos base:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

Outros:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

Em ambos os deslocamentos<2> indica o deslocamento na pilha \_ de argumentos virtuais, em bytes. Para tipos base, o tipo de argumento é dado diretamente pelo caractere de formato correspondente ao tipo. Para outros tipos, o deslocamento de tipo<2> campo fornece o deslocamento na tabela de cadeia de caracteres de formato de tipo em que o descritor de tipo para o argumento \_ está localizado.

O campo de atributo de parâmetro é definido da seguinte forma:

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   O **bit MustSize** será definido somente se o parâmetro tiver que ser dimensionado.
-   O **bit MustFree** será definido se o servidor deve chamar a rotina NdrFree do \* parâmetro.
-   O **bit IsSimpleRef** é definido para um parâmetro que é um ponteiro de referência para qualquer coisa diferente de outro ponteiro e que não tem atributos alocados. Para esse tipo, o campo<> deslocamento de tipo da descrição do parâmetro, exceto por um ponteiro de referência para um tipo base, fornece o deslocamento para o tipo do referenciado; o ponteiro de referência é simplesmente \_ ignorado.
-   O **bit IsDontCallFreeInst** é definido para determinados representar como parâmetros cujas rotinas de instância \_ livre não devem ser chamadas.
-   Os bits **ServerAllocSize** não serão zero se o parâmetro estiver fora de , em ou em, ponteiro de saída para ponteiro ou ponteiro para enum16 e serão inicializados na pilha do interpretador do servidor, em vez de usar uma chamada para \[  \] \[  \] \[  \] I **\_ RpcAllocate**. Se não for zero, esse valor será multiplicado por 8 para obter o número de bytes para o parâmetro . Observe que fazer isso significa que pelo menos 8 bytes são sempre alocados para um ponteiro.
-   O **bit IsBasetype** é definido para tipos simples que estão sendo empacotados pelo loop principal do interpretador [**–Oif.**](/windows/desktop/Midl/-oi) Em particular, um tipo simples com um atributo de intervalo não é sinalizado como um tipo base para forçar o marshaling de rotina do intervalo por meio da expedição usando um token FC \_ RANGE.
-   O bit **IsByValue** é definido para tipos compostos enviados por valor, mas não é definido para tipos simples, independentemente de o argumento ser um ponteiro. Os tipos compostos para os quais ele é definido são estruturas, uniões, transmitir como , [**representar \_ como**](/windows/desktop/Midl/represent-as), [**marshal de \_ transmissão**](/windows/desktop/Midl/wire-marshal) e SAFEARRAY. [**\_**](/windows/desktop/Midl/transmit-as) Em geral, o bit foi introduzido para o benefício do loop do interpretador principal no interpretador [**–Oicf,**](/windows/desktop/Midl/-oi) para garantir que os argumentos não simples (chamados de argumentos de tipo composto) sejam desreferenciados corretamente. Esse bit nunca foi usado em versões anteriores do interpretador.

 

 