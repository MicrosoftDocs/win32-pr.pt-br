---
Description: Veja a seguir uma breve comparação dos vários métodos de alocação de memória.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparando métodos de alocação de memória
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103930527"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="26dbc-103">Comparando métodos de alocação de memória</span><span class="sxs-lookup"><span data-stu-id="26dbc-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="26dbc-104">Veja a seguir uma breve comparação dos vários métodos de alocação de memória:</span><span class="sxs-lookup"><span data-stu-id="26dbc-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="26dbc-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="26dbc-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="26dbc-107">**HeapAlloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="26dbc-108">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="26dbc-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-109">**malloc**</span></span>
-   <span data-ttu-id="26dbc-110">**Novo**</span><span class="sxs-lookup"><span data-stu-id="26dbc-110">**new**</span></span>
-   [<span data-ttu-id="26dbc-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="26dbc-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="26dbc-112">Embora as funções [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) alocam, por fim, a memória do mesmo heap, cada uma delas fornece um conjunto de funcionalidades um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="26dbc-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="26dbc-113">Por exemplo, **HeapAlloc** pode ser instruído a gerar uma exceção se a memória não puder ser alocada, um recurso não disponível com **LocalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="26dbc-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="26dbc-114">O **LocalAlloc** dá suporte à alocação de identificadores que permitem que a memória subjacente seja movida por uma realocação sem alterar o valor do identificador, um recurso não disponível com **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="26dbc-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="26dbc-115">Começando com o Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) são implementados como funções de wrapper que chamam [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando um identificador para o heap padrão do processo.</span><span class="sxs-lookup"><span data-stu-id="26dbc-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="26dbc-116">Portanto, **GlobalAlloc** e **LocalAlloc** têm maior sobrecarga do que o **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="26dbc-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="26dbc-117">Como os alocadores de heap diferentes fornecem funcionalidade distinta usando mecanismos diferentes, você deve liberar memória com a função correta.</span><span class="sxs-lookup"><span data-stu-id="26dbc-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="26dbc-118">Por exemplo, a memória alocada com [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve ser liberada com [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e não [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ou [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span><span class="sxs-lookup"><span data-stu-id="26dbc-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="26dbc-119">A memória alocada com [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve ser consultada, validada e liberada com a função global ou local correspondente.</span><span class="sxs-lookup"><span data-stu-id="26dbc-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="26dbc-120">A função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) permite que você especifique opções adicionais para a alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="26dbc-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="26dbc-121">No entanto, suas alocações usam uma granularidade de página, portanto, usar o **VirtualAlloc** pode resultar em maior uso de memória.</span><span class="sxs-lookup"><span data-stu-id="26dbc-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="26dbc-122">A função **malloc** tem a desvantagem de ser dependente do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="26dbc-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="26dbc-123">O **novo** operador tem a desvantagem de ser dependente do compilador e dependente do idioma.</span><span class="sxs-lookup"><span data-stu-id="26dbc-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="26dbc-124">A função [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tem a vantagem de funcionar bem em C, C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="26dbc-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="26dbc-125">Também é a única maneira de compartilhar memória em um aplicativo baseado em COM, pois MIDL usa **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para empacotar a memória.</span><span class="sxs-lookup"><span data-stu-id="26dbc-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="26dbc-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26dbc-126">Examples</span></span>

* [<span data-ttu-id="26dbc-127">Reservando e confirmando memória</span><span class="sxs-lookup"><span data-stu-id="26dbc-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="26dbc-128">Exemplo de AWE</span><span class="sxs-lookup"><span data-stu-id="26dbc-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="26dbc-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26dbc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26dbc-130">Funções globais e locais</span><span class="sxs-lookup"><span data-stu-id="26dbc-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="26dbc-131">Funções de heap</span><span class="sxs-lookup"><span data-stu-id="26dbc-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="26dbc-132">Funções de memória virtual</span><span class="sxs-lookup"><span data-stu-id="26dbc-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 