---
title: Rotina de execução de contexto de servidor
description: Se a comunicação for interrompida enquanto o servidor estiver mantendo o contexto em nome do cliente, uma rotina de limpeza poderá ser necessária para limpar o estado mantido pelo servidor em nome de um determinado cliente.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005963"
---
# <a name="server-context-run-down-routine"></a>Rotina de execução de contexto de servidor

Se a comunicação for interrompida enquanto o servidor estiver mantendo o contexto em nome do cliente, uma rotina de limpeza poderá ser necessária para limpar o estado mantido pelo servidor em nome de um determinado cliente. Essa rotina de limpeza é chamada de *rotina de execução de contexto*. Quando uma conexão for interrompida, o stub do servidor e a biblioteca de tempo de execução chamarão essa rotina em cada identificador de contexto aberto pelo cliente.

A rotina de execução de contexto é necessária e é implicitamente declarada e nomeada quando você aplica o \[ atributo de **\_ identificador de contexto** \] a uma definição de tipo. O servidor não chamará a rotina de execução de contexto se o \[ atributo de **\_ identificador de contexto** \] tiver sido aplicado diretamente a um parâmetro.

A sintaxe de rotina de execução de contexto é:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Observe que o nome do tipo determina o nome da rotina de execução do contexto.

O fragmento de código a seguir apresenta uma rotina de execução de contexto de exemplo. Isso chama o procedimento RemoteClose usado no exemplo de [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md), desenvolvimento de [servidor usando identificadores de contexto](server-development-using-context-handles.md)e desenvolvimento de [cliente usando identificadores de contexto](client-development-using-context-handles.md). Este procedimento fecha o identificador de arquivo, libera a memória associada ao arquivo e atribui **NULL** ao identificador de contexto. A atribuição de **NULL** é um resultado da chamada da função RemoteClose e não é necessária em um cenário de execução. O tempo de execução de RPC limpa seu estado, independentemente de o identificador de contexto ser definido como **nulo**.

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




