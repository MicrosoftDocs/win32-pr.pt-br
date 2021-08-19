---
title: Alças
description: Até duas partes na descrição da cadeia de caracteres de formato de um endereço de procedimento são lidas.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb31dcf075b7b07b65d2a976a37386e164d8cadc11903a33c22172c433a3a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929533"
---
# <a name="handles"></a>Alças

Até duas partes na descrição da cadeia de caracteres de formato de um endereço de procedimento são lidas. A primeira parte é o tipo de identificador<1> campo da descrição de um \_ procedimento, usado para indicar identificador implícito. Essa parte está sempre presente. A segunda parte é uma descrição de parâmetro de qualquer alça explícita no procedimento. Ambos são explicados nas seções a seguir, juntamente com uma discussão sobre o suporte adicional do compilador MIDL da estrutura do descritor stub para problemas de alça de associação.

## <a name="implicit-handles"></a>Alças implícitas

Se um procedimento usar um identificador implícito para associação, o tipo de identificador<1> campo da descrição do procedimento conterá um dos três valores diferentes \_ de zero válidos. O suporte do compilador MIDL para alças implícitas é encontrado no campo IMPLICIT \_ HANDLE INFO da estrutura do \_ Descritor de Stub:

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

Se o procedimento usar um handle automático, o membro **pAutoHandle** conterá o endereço da variável de alça automática definida pelo stub.

Se o procedimento usar um manipulador primitivo implícito, o membro **pPrimitiveHandle** conterá o endereço da variável de alça stub defined-primitive.

Por fim, se o procedimento usar um handle genérico implícito, o membro **pGenericBindingInfo** manterá o endereço do ponteiro para a estrutura **GENERIC BINDING \_ \_ INFO** correspondente. A ESTRUTURA de **dados MIDL \_ STUB \_ DESC** contém um ponteiro para uma coleção de **estruturas GENERIC \_ BINDING \_ PAIR.** A entrada na posição zero desta coleção é  reservada para as rotinas **de** associação e desa associação correspondentes ao handle de associação genérico referenciado por **pGenericBindingInfo** em **IMPLICIT \_ HANDLE \_ INFO**. O tipo de identificador de associação implícita é indicado na cadeia de caracteres de formato.

## <a name="explicit-handles"></a>Alças explícitas

Há três tipos de alça explícitos possíveis: contexto, genérico e primitivo. No caso de um alça explícito (ou um alça de contexto somente de saída, que é tratado da mesma maneira), as informações de manipulação de associação aparecem como um dos \[  \] parâmetros do procedimento. As três descrições possíveis são as a seguir.

Primitivo

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

O sinalizador<1> indica se o ponteiro é passado por um ponteiro.

O deslocamento<2> fornece o deslocamento do início da pilha para o alça primitivo.

> [!Note]  
> Uma descrição de identificador primitivo na cadeia de caracteres de formato de tipo é reduzida a um único FC \_ IGNORE.

 

Genérico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

O sinalizador e o tamanho<1> tem a nibble de sinalizador superior e a \_ \_ nibble de tamanho inferior. O sinalizador indica se o alça é passado por um ponteiro. O campo tamanho fornece o tamanho do tipo de identificador genérico definido pelo usuário. Esse tamanho é limitado a ser de 1, 2 ou 4 bytes em sistemas de 32 bits e 1, 2, 4 ou 8 bytes em sistemas de 64 bits.

O deslocamento<2> campo fornece o deslocamento do início da pilha do ponteiro para os dados do tamanho determinado.

O campo> índice de par de rotina de associação<1 fornece o índice no campo \_ \_ \_ aGenericBindingRoutinePairs   do Descritor de Stub para os ponteiros de função de rotina de associação e desa associação para o indicador genérico.

> [!Note]  
> Uma descrição de identificador genérico no formato de tipo é a descrição apenas do tipo de dados relacionado.

 

Contexto

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Os sinalizadores<1> indicam como o identificador é passado e qual é o tipo. Sinalizadores válidos são mostrados na tabela a seguir.



| Hex | Sinalizador                                   |
|-----|----------------------------------------|
| 80  | HANDLE \_ PARAM \_ É VIA \_ \_ PTR            |
| 40  | HANDLE \_ PARAM \_ ESTÁ \_ EM                  |
| 20  | HANDLE \_ PARAM \_ IS \_ OUT                 |
| 21  | HANDLE \_ PARAM \_ IS \_ RETURN              |
| 08  | NDR \_ STRICT \_ CONTEXT \_ HANDLE           |
| 04  | NDR \_ CONTEXT \_ HANDLE \_ NO \_ SERIALIZE    |
| 02  | SERIALIZAR \_ O ALÇA DE \_ CONTEXTO \_ NDR        |
| 01  | O HANDLE \_ DE CONTEXTO \_ NDR NÃO PODE SER \_ \_ \_ NULO |



 

Os quatro primeiros sinalizadores sempre estavam presentes, os quatro últimos foram adicionados Windows 2000.

O deslocamento<2> campo fornece o deslocamento do início da pilha para o alça de contexto.

O índice de rotina de resumo de contexto<1> fornece um índice no campo \_ \_ \_ **apfnNdrRundownRoutines** do Descritor de Stub para a rotina de rundown usada para esse indicador de contexto. O compilador sempre gera um índice. Para rotinas que não têm uma rotina de rundown, esse é um índice para uma posição de tabela que contém nulo.

Para stubs integrados em **–Oi2**, o param num<1> fornece a contagem ordinal, começando em zero, especificando qual alça de contexto ele está no procedimento \_ especificado.

Para versões anteriores do interpretador, o parâmetro num<1> fornece o número de parâmetro do alça de contexto, começando em zero, em \_ seu procedimento.

> [!Note]  
> Uma descrição do identificador de contexto na cadeia de caracteres de formato de tipo não terá o deslocamento<2> na descrição.

 

## <a name="the-new-oif-header"></a>O novo -Oif header

Conforme mencionado anteriormente, o header [**–Oif**](/windows/desktop/Midl/-oi) se expande no **header –Oi.** Para sua conveniência, todos os campos são mostrados aqui:

(O antigo header)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(As [**extensões –Oif)**](/windows/desktop/Midl/-oi)

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

O tamanho constante do buffer do cliente<2> fornece o tamanho do buffer de marshaling que poderia ter sido \_ \_ \_ pré-computado pelo compilador. Isso pode ser apenas um tamanho parcial, pois o sinalizador ClientMustSize dispara o tamanho.

O tamanho constante do buffer do servidor<2> fornece o tamanho do buffer de marshaling conforme pré-compilado \_ \_ pelo \_ compilador. Isso pode ser apenas um tamanho parcial, pois o sinalizador ServerMustSize dispara o tamanho.

Os \_ SINALIZADORES DE OPT \_ DO INTERPRETADOR são definidos em Ndrtypes.h:

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

-   O bit ServerMustSize será definido se o servidor precisar executar uma passagem de tamanho de buffer.
-   O bit ClientMustSize será definido se o cliente precisar executar uma passagem de tamanho de buffer.
-   O bit HasReturn será definido se o procedimento tiver um valor de retorno.
-   O bit HasPipes será definido se o pacote de pipe precisar ser usado para dar suporte a um argumento de pipe.
-   O bit HasAsyncUuid será definido se o procedimento for um procedimento DCOM assíncrono.
-   O bit HasExtensions indica que Windows 2000 e extensões posteriores são usadas.
-   O bit HasAsyncHandle indica um procedimento RPC assíncrono.

O bit HasAsyncHandle foi inicialmente usado para uma implementação de DCOM diferente de suporte assíncrono e, portanto, não pôde ser usado para o suporte assíncrono de estilo atual no DCOM. O bit HasAsyncUuid atualmente indica isso.

 

 