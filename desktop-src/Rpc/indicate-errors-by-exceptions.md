---
title: Indicar erros por exceções
description: Para programadores C tradicionais, os erros são normalmente retornados por meio de valores de retorno ou um parâmetro "out \" especial que retorna o código de erro.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823887"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="27233-103">Indicar erros por exceções</span><span class="sxs-lookup"><span data-stu-id="27233-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="27233-104">Para programadores C tradicionais, os erros são normalmente retornados por meio de valores de retorno ou um \[ parâmetro de saída especial \] que retorna o código de erro.</span><span class="sxs-lookup"><span data-stu-id="27233-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="27233-105">Isso leva a interfaces implementadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="27233-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="27233-106">O problema dessa abordagem é que os valores de retorno de RPC são simplesmente inteiros longos.</span><span class="sxs-lookup"><span data-stu-id="27233-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="27233-107">Eles não têm um significado especial como erros (Observe que o [**status de erro \_ \_ t**](/windows/desktop/Midl/error-status-t) não tem semântica especial no lado do servidor), o que transporta implicações importantes.</span><span class="sxs-lookup"><span data-stu-id="27233-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="27233-108">Primeiro, o RPC não é alertado de que a operação falhou; Ele tenta desempacotar todos os \[ argumentos de entrada, saída \] e \[ saída \] .</span><span class="sxs-lookup"><span data-stu-id="27233-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="27233-109">A semântica de falha dos identificadores de contexto também é diferente.</span><span class="sxs-lookup"><span data-stu-id="27233-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="27233-110">O pacote retornado para o cliente é essencialmente um pacote de êxito, com o código de erro enterrado em profundidade no pacote.</span><span class="sxs-lookup"><span data-stu-id="27233-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="27233-111">Isso também significa que o RPC não usa informações de erro estendidas, portanto, o software cliente geralmente não é capaz de distinguir onde a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="27233-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="27233-112">Indicar erros nas rotinas do servidor RPC lançando Exceções SEH (manipulação de exceção estruturada) (e não C++) é uma abordagem muito melhor.</span><span class="sxs-lookup"><span data-stu-id="27233-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="27233-113">Quando uma exceção SEH é gerada, o controle vai diretamente para o tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="27233-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="27233-114">Às vezes, um erro ocorre em uma rotina que não pode ser limpa corretamente e precisa indicar um erro para seu chamador.</span><span class="sxs-lookup"><span data-stu-id="27233-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="27233-115">A rotina deve retornar um erro para seu chamador, que, por sua vez, pode retornar um erro para seu chamador e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="27233-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="27233-116">No entanto, a última rotina de servidor na pilha deve lançar uma exceção antes que ela retorne ao RPC para indicar ao RPC que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="27233-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27233-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27233-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27233-118">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="27233-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 