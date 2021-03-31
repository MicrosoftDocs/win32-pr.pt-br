---
title: Usando identificadores de associação e fazendo chamadas RPC
description: Um erro comum entre os programadores de RPC é A manipulação de todas as exceções.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641487"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="e6008-103">Usando identificadores de associação e fazendo chamadas RPC</span><span class="sxs-lookup"><span data-stu-id="e6008-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="e6008-104">Um erro comum entre os programadores de RPC é A manipulação de todas as exceções.</span><span class="sxs-lookup"><span data-stu-id="e6008-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="e6008-105">Muitos programadores estruturam seus identificadores de exceção como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6008-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="e6008-106">O problema com esse manipulador é que ele captura todos os erros, incluindo erros no programa cliente.</span><span class="sxs-lookup"><span data-stu-id="e6008-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="e6008-107">A captura de erros no programa cliente torna a depuração mais difícil.</span><span class="sxs-lookup"><span data-stu-id="e6008-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="e6008-108">A maneira apropriada de estruturar um manipulador de exceção é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6008-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="e6008-109">Esse manipulador de exceção tem a vantagem de permitir um determinado intervalo de erros por meio do.</span><span class="sxs-lookup"><span data-stu-id="e6008-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="e6008-110">Esses erros nunca serão retornados pelo servidor, pois eles indicam um problema no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e6008-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="e6008-111">Além disso, o uso do **\[** [ \_ \_ identificador de contexto estrito](/windows/desktop/Midl/strict-context-handle) **\]** e o tipo de atributos de **\[** [ \_ \_ \_ identificador de contexto estrito](/windows/desktop/Midl/type-strict-context-handle) **\]** são recomendados para garantir que o tempo de execução de RPC crie um identificador de contexto em uma interface que possa ser passada como um argumento somente para métodos dessa interface.</span><span class="sxs-lookup"><span data-stu-id="e6008-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="e6008-112">Isso impedirá falhas de servidor que ocorrem quando os identificadores de contexto são abertos e passados entre diferentes interfaces que existem dentro do mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="e6008-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6008-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6008-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6008-114">\_identificador de contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="e6008-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="e6008-115">tipo \_ de \_ identificador de contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="e6008-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 