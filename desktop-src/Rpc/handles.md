---
title: Alças
description: Até duas partes na descrição da cadeia de caracteres de formato de identificadores de endereço de procedimento.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294370"
---
# <a name="handles"></a>Alças

Até duas partes na descrição da cadeia de caracteres de formato de identificadores de endereço de procedimento. A primeira parte é o tipo de identificador \_<1> campo da descrição de um procedimento, usado para indicar identificadores implícitos. Esta parte está sempre presente. A segunda parte é uma descrição de parâmetro de qualquer identificador explícito no procedimento. Ambos são explicados nas seções a seguir, juntamente com uma discussão sobre o suporte adicional do compilador MIDL da estrutura do descritor de stub para problemas de identificador de associação.

## <a name="implicit-handles"></a>Identificadores implícitos

Se um procedimento usar um identificador implícito para associação, o tipo de identificador \_<1> campo da descrição do procedimento conterá um dos três valores válidos de zero. O suporte do compilador MIDL para identificadores implícitos é encontrado no \_ \_ campo informações do identificador implícito da estrutura do descritor de stub:

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

Se o procedimento usar um identificador automático, o membro **pAutoHandle** conterá o endereço do stub definido – variável de identificador auto.

Se o procedimento usar um identificador primitivo implícito, o membro **pPrimitiveHandle** conterá o endereço do stub definido – variável de identificador primitivo.

Por fim, se o procedimento usar um identificador genérico implícito, o membro **pGenericBindingInfo** manterá o endereço do ponteiro para a estrutura de **\_ \_ informações de associação genérica** correspondente. A estrutura de dados do **stub de MIDL \_ \_** contém um ponteiro para uma coleção de estruturas de **\_ \_ par de ligação genérica** . A entrada na posição zero dessa coleção é reservada para as rotinas **de associação e** **desvinculação** correspondentes ao identificador de associação genérico referenciado por **PGenericBindingInfo** nas **\_ \_ informações do identificador implícito**. O tipo de identificador de ligação implícita é indicado na cadeia de caracteres de formato.

## <a name="explicit-handles"></a>Identificadores explícitos

Há três tipos de identificador explícitos possíveis: contexto, genérico e primitivo. No caso de um identificador explícito (ou um \[  \] identificador de contexto somente out, que é manipulado da mesma maneira), as informações do identificador de associação são exibidas como um dos parâmetros do procedimento. As três descrições possíveis são as seguintes.

Primitiva

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

O sinalizador<1> indica se o identificador é passado por um ponteiro.

O deslocamento<2> fornece o deslocamento desde o início da pilha até o identificador primitivo.

> [!Note]  
> Uma descrição do identificador primitivo na cadeia de caracteres de formato de tipo é reduzida para uma única \_ ignorar FC.

 

Genérico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

O sinalizador \_ e \_ o tamanho<1> tem o sinal superior Nibble e o tamanho inferior Nibble. O sinalizador indica se o identificador é passado por um ponteiro. O campo tamanho fornece o tamanho do tipo de identificador genérico definido pelo usuário. Esse tamanho é limitado a 1, 2 ou 4 bytes em sistemas de 32 bits e 1, 2, 4 ou 8 bytes em sistemas de 64 bits.

O campo deslocamento<2> fornece o deslocamento do início da pilha do ponteiro até os dados do tamanho fornecido.

O índice de par de rotina de associação \_ \_ \_<campo 1> fornece ao índice o campo aGenericBindingRoutinePairs do descritor de stub para os ponteiros de função de rotina de **Associação** e **desassociação** para o identificador genérico.

> [!Note]  
> Uma descrição de identificador genérico no formato de tipo é a descrição somente do tipo de dados relacionado.

 

Contexto

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Os sinalizadores<1> indicam como o identificador é passado e qual é o tipo. Os sinalizadores válidos são mostrados na tabela a seguir.



| Hex | Sinalizador                                   |
|-----|----------------------------------------|
| 80  | o identificador de \_ parâmetro \_ é \_ via \_ PTR            |
| 40  | o \_ parâmetro Handle \_ está \_ em                  |
| 20  | o \_ parâmetro Handle \_ está \_ fora                 |
| 21  | o \_ parâmetro Handle \_ é \_ retornado              |
| 08  | \_identificador de \_ contexto \_ estrito NDR           |
| 04  | \_manipulador de contexto NDR \_ \_ sem \_ serialização    |
| 02  | \_serialização de \_ identificador de contexto NDR \_        |
| 01  | o \_ identificador de contexto NDR \_ \_ não pode \_ ser \_ nulo |



 

Os quatro primeiros sinalizadores sempre estão presentes, os últimos quatro foram adicionados ao Windows 2000.

O campo deslocamento<2> fornece o deslocamento desde o início da pilha até o identificador de contexto.

O índice de rotina de encerramento de contexto \_ \_ \_<1> fornece um índice para o campo **apfnNdrRundownRoutines** do descritor de stub para a rotina de encerramento usada para esse identificador de contexto. O compilador sempre gera um índice. Para rotinas que não têm uma rotina de encerramento, esse é um índice para uma posição de tabela que contém NULL.

Para stubs internos **– Oi2**, o param \_ num<1> fornece a contagem ordinal, começando em zero, especificando qual identificador de contexto está no procedimento fornecido.

Para versões anteriores do interpretador, o param \_ num<1> fornece o número do parâmetro do identificador de contexto, começando em zero, em seu procedimento.

> [!Note]  
> Uma descrição de identificador de contexto na cadeia de caracteres de formato de tipo não terá o deslocamento<2> na descrição.

 

## <a name="the-new-oif-header"></a>O cabeçalho New – OIF

Conforme mencionado anteriormente, o cabeçalho [**– OIF**](/windows/desktop/Midl/-oi) se expande no cabeçalho **– Oi** . Para sua conveniência, todos os campos são mostrados aqui:

(O cabeçalho antigo)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(As extensões [**– OIF**](/windows/desktop/Midl/-oi) )

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

O \_ \_ tamanho de buffer de cliente constante \_<2> fornece o tamanho do buffer de marshaling que poderia ter sido previamente computado pelo compilador. Isso pode ser apenas um tamanho parcial, pois o sinalizador ClientMustSize aciona o dimensionamento.

O \_ tamanho do buffer do servidor constante \_ \_<2> fornece o tamanho do buffer de marshaling como pré-compilado pelo compilador. Isso pode ser apenas um tamanho parcial, pois o sinalizador ServerMustSize aciona o dimensionamento.

Os sinalizadores de \_ consentimento do intérprete \_ são definidos em Ndrtypes. h:

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   O bit ServerMustSize será definido se o servidor precisar executar uma passagem de dimensionamento de buffer.
-   O bit ClientMustSize será definido se o cliente precisar executar uma passagem de dimensionamento de buffer.
-   O bit HasReturn será definido se o procedimento tiver um valor de retorno.
-   O bit HasPipes será definido se o pacote de pipe precisar ser usado para dar suporte a um argumento de pipe.
-   O bit HasAsyncUuid será definido se o procedimento for um procedimento DCOM assíncrono.
-   O bit HasExtensions indica que o Windows 2000 e extensões posteriores são usados.
-   O bit HasAsyncHandle indica um procedimento RPC assíncrono.

O HasAsyncHandle bit foi usado inicialmente para uma implementação de DCOM diferente do suporte assíncrono e, portanto, não pôde ser usado para o suporte assíncrono de estilo atual no DCOM. O bit HasAsyncUuid atualmente indica isso.

 

 