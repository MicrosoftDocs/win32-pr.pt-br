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
# <a name="server-context-run-down-routine"></a><span data-ttu-id="b5853-103">Rotina de execução de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="b5853-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="b5853-104">Se a comunicação for interrompida enquanto o servidor estiver mantendo o contexto em nome do cliente, uma rotina de limpeza poderá ser necessária para limpar o estado mantido pelo servidor em nome de um determinado cliente.</span><span class="sxs-lookup"><span data-stu-id="b5853-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="b5853-105">Essa rotina de limpeza é chamada de *rotina de execução de contexto*.</span><span class="sxs-lookup"><span data-stu-id="b5853-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="b5853-106">Quando uma conexão for interrompida, o stub do servidor e a biblioteca de tempo de execução chamarão essa rotina em cada identificador de contexto aberto pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="b5853-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="b5853-107">A rotina de execução de contexto é necessária e é implicitamente declarada e nomeada quando você aplica o \[ atributo de **\_ identificador de contexto** \] a uma definição de tipo.</span><span class="sxs-lookup"><span data-stu-id="b5853-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="b5853-108">O servidor não chamará a rotina de execução de contexto se o \[ atributo de **\_ identificador de contexto** \] tiver sido aplicado diretamente a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b5853-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="b5853-109">A sintaxe de rotina de execução de contexto é:</span><span class="sxs-lookup"><span data-stu-id="b5853-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="b5853-110">Observe que o nome do tipo determina o nome da rotina de execução do contexto.</span><span class="sxs-lookup"><span data-stu-id="b5853-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="b5853-111">O fragmento de código a seguir apresenta uma rotina de execução de contexto de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b5853-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="b5853-112">Isso chama o procedimento RemoteClose usado no exemplo de [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md), desenvolvimento de [servidor usando identificadores de contexto](server-development-using-context-handles.md)e desenvolvimento de [cliente usando identificadores de contexto](client-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="b5853-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="b5853-113">Este procedimento fecha o identificador de arquivo, libera a memória associada ao arquivo e atribui **NULL** ao identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="b5853-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="b5853-114">A atribuição de **NULL** é um resultado da chamada da função RemoteClose e não é necessária em um cenário de execução.</span><span class="sxs-lookup"><span data-stu-id="b5853-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="b5853-115">O tempo de execução de RPC limpa seu estado, independentemente de o identificador de contexto ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5853-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

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

 

 




