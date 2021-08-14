---
title: O header
description: O seguinte header representa um dos estilos de header que podem ser gerados pela versão atual do MIDL. Para sua conveniência, a lista completa de campos de header é fornecida aqui.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ee00425f3611234b0cd001f254b1499a0d4873d05846c65a2828c3eeffe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924535"
---
# <a name="the-header"></a>O header

O seguinte header representa um dos estilos de header que podem ser gerados pela versão atual do MIDL. Para sua conveniência, a lista completa de campos de header é fornecida aqui.

([**–Oif**](/windows/desktop/Midl/-oi) header)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Extensões do Windows 2000: <8> para 32 bits, <12> para 64 bits)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

A versão \_ de<1> fornece o tamanho da seção de extensão, em bytes. Isso possibilita que o mecanismo de NDR atual vá sobre a seção de extensão corretamente, mesmo que a seção venha de uma versão posterior do compilador com mais campos do que o mecanismo atual entende.

Os \_ SINALIZADORES DE \_ ACEITAÇÃO DO INTERPRETADOR2 são definidos da seguinte forma:

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

O **membro HasNewCorrDesc** indica se novos descritores de correlação são usados nas cadeias de caracteres de formato geradas pelo compilador. O novo descritor de correlação está relacionado à funcionalidade de negação de ataque. Os **membros ClientCorrCheck** e **ServerCorrCheck** são definidos quando a rotina precisa da verificação de correlação no lado indicado.

Os **sinalizadores HasNotify** e **\[ \]** **HasNotify2** indicam que a rotina usa o recurso de notificação conforme definido pelos atributos de notificação e notificação **\[ \_ do \]** sinalizador, respectivamente.

O **membro ClientCorrCheck** é uma dica de tamanho de cache no lado do cliente e **ServerCorrCheck** é uma dica no lado do servidor. Quando o tamanho sai como zero, um tamanho padrão deve ser usado.

O **elemento NotifyIndex** é um índice para uma rotina de notificação, se um for usado.

O **elemento FloatDoubleMask** aborda o problema de um argumento de ponto flutuante para 64 bits Windows. Esse campo é gerado somente para stubs de 64 bits. A máscara é necessária para as rotinas de assembly que baixam/carregam registros de/para a pilha virtual para lidar com argumentos de ponto flutuante e se registra corretamente. A máscara consiste em 2 bits por argumento ou, em vez disso, por registro de ponto flutuante. A codificação é a seguinte: os bits menos significativos correspondem ao primeiro registro de FP, os próximos 2 bits correspondem ao segundo registro e assim por diante.

> [!Note]  
> Para rotinas de objeto, o primeiro argumento termina no segundo registro devido a esse ponteiro ser o primeiro. Para cada registro, o significado de bits é conforme mostrado na tabela a seguir.

 



| Bits | Significado                                          |
|------|--------------------------------------------------|
| 01   | Um valor float deve ser carregado no registro.  |
| 10   | Um valor duplo deve ser carregado no registro. |



 

00 e 11 são valores inválidos para os bits.

Atualmente, há oito registros FP em um processador intel Architecture de 64 bits, portanto, a máscara pode ter apenas 16b bits mais baixos definidos. O tamanho da máscara foi definido como um total de 16 bits com base na máscara do compilador C permanece inalterada.

## <a name="header-streamlining-for-performance"></a>Fluxo de header para desempenho

Para simplificar o código e melhorar o desempenho, o compilador tenta gerar um header de tamanho fixo sempre que possível. Em particular, o seguinte header é usado para DCOM assíncrono:

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 