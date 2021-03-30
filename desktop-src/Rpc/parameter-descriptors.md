---
title: Descritores de parâmetro
description: Como mencionado anteriormente, existem os descritores de parâmetro de estilo \ 8211; Oi e \ 8211; OIF.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641627"
---
# <a name="parameter-descriptors"></a>Descritores de parâmetro

Como mencionado [**anteriormente, existem descritores de parâmetro**](/windows/desktop/Midl/-oi) de estilo **OIF** .

## <a name="the-oi-parameter-descriptors"></a>Os descritores de parâmetro – Oi

Stubs totalmente interpretados exigem informações adicionais para cada um dos parâmetros em uma chamada RPC. As descrições de parâmetro de um procedimento seguem imediatamente após a descrição do procedimento.

[**Simples – Oi**](/windows/desktop/Midl/-oi)

**Descritores de parâmetro**

O formato para a descrição de um \[  \] parâmetro de tipo simples in ou Return é:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–ou–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Em que o \_ tipo simples<1> é o token FC que indica o tipo simples. Os códigos são os seguintes:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Outros – Oi**

**Descritores de parâmetro**

O formato da descrição para todos os outros tipos de parâmetro é:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Onde a direção do param \_<1> campo para cada uma dessas descrições deve ser um daqueles mostrados na tabela a seguir.



| Hex | Sinalizador                          | Significado                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4D  | FC \_ no \_ param                 | Um parâmetro in.                                            |
| 50  | \_parâmetro FC em \_ saída \_            | Um parâmetro in/out.                                        |
| 51  | \_parâmetro de saída do FC \_                | Um parâmetro out.                                           |
| 52  | \_parâmetro de retorno de FC \_             | Um valor de retorno de procedimento.                                   |
| 4F  | FC \_ em \_ param \_ sem \_ Free \_ Inst | Um em transmissão/representante como um parâmetro para o qual não foi feita nenhuma liberação. |



 

O tamanho da pilha \_<1> é o tamanho do parâmetro na pilha, expresso como o número de inteiros que o parâmetro ocupa na pilha.

> [!Note]  
> Não há suporte para o modo [**– Oi**](/windows/desktop/Midl/-oi) em plataformas de 64 bits.

 

O \_ campo deslocamento de tipo<2> é o deslocamento na tabela de cadeia de caracteres de formato de tipo, indicando o descritor de tipo para o argumento.

## <a name="the-oif-parameter-descriptors"></a>Os descritores de parâmetro – OIF

Há dois formatos possíveis para uma descrição de parâmetro, um para tipos base, outro para todos os outros tipos.

Tipos de base:

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

No deslocamento de pilha \_<2> indica o deslocamento na pilha de argumentos virtuais, em bytes. Para tipos base, o tipo de argumento é fornecido diretamente pelo caractere de formato correspondente ao tipo. Para outros tipos, o \_ campo deslocamento de tipo<2> fornece o deslocamento na tabela de cadeia de caracteres de formato de tipo em que o descritor de tipo para o argumento está localizado.

O campo atributo de parâmetro é definido da seguinte maneira:

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

-   O bit **MustSize** será definido somente se o parâmetro precisar ser dimensionado.
-   O bit **MustFree** será definido se o servidor precisar chamar a rotina NdrFree do parâmetro \* .
-   O bit **IsSimpleRef** é definido para um parâmetro que é um ponteiro de referência para qualquer coisa diferente de outro ponteiro, e que não tem atributos Allocate. Para esse tipo, o deslocamento de tipo da descrição do parâmetro \_<> campo, com exceção de um ponteiro de referência para um tipo base, fornece o deslocamento para o tipo do Referent; o ponteiro de referência é simplesmente ignorado.
-   O bit **IsDontCallFreeInst** é definido para determinadas representações \_ como parâmetros cujas rotinas de instância gratuita não devem ser chamadas.
-   Os bits de **ServerAllocSize** são diferentes de zero se o parâmetro estiver \[ **fora** \] , \[ **no** \] ponteiro de \[ **saída ou dentro** dele \] para ponteiro, ou ponteiro para enum16, e será inicializado na pilha do intérprete do servidor, em vez de usar uma chamada para **I \_ RpcAllocate**. Se for diferente de zero, esse valor será multiplicado por 8 para obter o número de bytes para o parâmetro. Observe que isso significa que pelo menos 8 bytes sempre são alocados para um ponteiro.
-   O bit **Isbasetype** é definido para tipos simples que estão sendo empacotados pelo loop do intérprete principal [**– OIF**](/windows/desktop/Midl/-oi) . Em particular, um tipo simples com um atributo de intervalo não é sinalizado como um tipo base para forçar o marshaling da rotina de intervalo por meio de expedição usando um token de intervalo de FC \_ .
-   O bit **IsByValue** é definido para os tipos compostos que estão sendo enviados por valor, mas não é definido para tipos simples, independentemente de o argumento ser um ponteiro. Os tipos compostos para os quais ele está definido são estruturas, uniões, [**Transmit \_ como**](/windows/desktop/Midl/transmit-as), [**representam \_ como**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) e SafeArray. Em geral, o bit foi introduzido para o benefício do principal loop do interpretador no interpretador [**– Oicf**](/windows/desktop/Midl/-oi) , para garantir que os argumentos não simples (chamados de argumentos de tipo composto) sejam desreferenciados corretamente. Esse bit nunca foi usado em versões anteriores do intérprete.

 

 