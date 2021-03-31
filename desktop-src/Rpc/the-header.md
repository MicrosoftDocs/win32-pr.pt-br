---
title: O cabeçalho
description: O cabeçalho a seguir representa um dos estilos de cabeçalho que podem ser gerados pela versão atual do MIDL. Para sua conveniência, a lista completa de campos de cabeçalho é fornecida aqui.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afcc9ad880278fdbcb8efc45fdabdc22ad06224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823950"
---
# <a name="the-header"></a>O cabeçalho

O cabeçalho a seguir representa um dos estilos de cabeçalho que podem ser gerados pela versão atual do MIDL. Para sua conveniência, a lista completa de campos de cabeçalho é fornecida aqui.

(Cabeçalho [**– OIF**](/windows/desktop/Midl/-oi) )

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

Extensões que começam com o Windows 2000: <8> para 32 bits, <12> para 64 bits)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

A versão de extensão \_<1> fornece o tamanho da seção de extensão, em bytes. Isso possibilita que o mecanismo de NDR atual percorra a seção de extensão corretamente, mesmo que a seção venha de uma versão do compilador posterior com mais campos do que o mecanismo atual compreende.

Os FLAGS2 de intérprete do interpretador \_ \_ são definidos como segue:

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

O membro **HasNewCorrDesc** indica se novos descritores de correlação são usados nas cadeias de caracteres de formato geradas pelo compilador. O novo descritor de correlação está relacionado à funcionalidade de negação de ataque. Os membros **ClientCorrCheck** e **ServerCorrCheck** são definidos quando a rotina precisa da verificação de correlação no lado indicado.

Os sinalizadores **HasNotify** e **HasNotify2** indicam que a rotina usa o recurso notificar, conforme definido pelos atributos **\[ \] notificar** e **\[ notificar \_ sinalizador \]** , respectivamente.

O membro **ClientCorrCheck** é uma dica de tamanho de cache no lado do cliente e **ServerCorrCheck** é uma dica no lado do servidor. Quando o tamanho sai como zero, um tamanho padrão deve ser usado.

O elemento **NotifyIndex** é um índice para uma rotina de notificação, se for usado um.

O elemento **FloatDoubleMask** aborda o problema de um argumento de ponto flutuante para o Windows de 64 bits. Esse campo é gerado somente para stubs de 64 bits. A máscara é necessária para as rotinas de assembly que o download/upload registra de/para a pilha virtual para manipular argumentos de ponto flutuante e são registradas corretamente. A máscara consiste em 2 bits por argumento ou, em vez de por registro de ponto flutuante. A codificação é a seguinte: os bits menos significativos correspondem ao primeiro registro de FP, os próximos dois bits correspondem ao segundo registro e assim por diante.

> [!Note]  
> Para rotinas de objeto, o primeiro argumento termina no segundo registro devido a esse ponteiro ser primeiro. Para cada registro, o significado dos bits é o mostrado na tabela a seguir.

 



| Bits | Significado                                          |
|------|--------------------------------------------------|
| 01   | Um valor float deve ser carregado para o registro.  |
| 10   | Um valor duplo deve ser carregado para o registro. |



 

00 e 11 são valores inválidos para os bits.

Atualmente, há oito registros de FP em um processador de arquitetura Intel de 64 bits, portanto, a máscara pode ter apenas o conjunto de bits mais baixo definido. O tamanho da máscara foi definido como um total de 16 bits com base na máscara do compilador C restante inalterado.

## <a name="header-streamlining-for-performance"></a>Cabeçalho simplificando o desempenho

Para simplificar o código e melhorar o desempenho, o compilador tenta gerar um cabeçalho de tamanho fixo sempre que possível. Em particular, o seguinte cabeçalho é usado para o DCOM assíncrono:

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

 

 