---
title: Pilha
description: Um heap rastreia um grupo de alocações que são liberadas como uma unidade.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Serviços Web de heap para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368959"
---
# <a name="heap"></a><span data-ttu-id="d0df5-106">Pilha</span><span class="sxs-lookup"><span data-stu-id="d0df5-106">Heap</span></span>

<span data-ttu-id="d0df5-107">Um heap rastreia um grupo de alocações que são liberadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="d0df5-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="d0df5-108">Isso permite que você evite padrões complexos de alocar e desalocar memória ao usar o WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="d0df5-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="d0df5-109">Há um heap associado a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0df5-109">There is a heap associated with every message.</span></span> <span data-ttu-id="d0df5-110">Como uma mensagem está sendo enviada, ou quando uma mensagem está sendo recebida, o heap da mensagem é usado para qualquer alocação relacionada a essa mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="d0df5-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="d0df5-111">Depois que uma mensagem é enviada ou recebida, o heap é redefinido (o que limpa todas as alocações relacionadas à mensagem específica).</span><span class="sxs-lookup"><span data-stu-id="d0df5-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="d0df5-112">Os heaps também podem ser usados para armazenar dados de mensagens separadamente do tempo de vida de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0df5-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="d0df5-113">Muitas das especificações de permissão de API do heap a serem usadas na leitura de dados fornecem controle explícito durante o tempo de vida de qualquer leitura de dados.</span><span class="sxs-lookup"><span data-stu-id="d0df5-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="d0df5-114">As alocações de um heap têm a garantia de serem alinhadas em pelo menos um limite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="d0df5-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="d0df5-115">As alocações de zero byte retornarão um ponteiro não nulo.</span><span class="sxs-lookup"><span data-stu-id="d0df5-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="d0df5-116">No Windows 7, se PageHeap estiver habilitado, um heap retornado de HeapCreate será usado para gerenciar a memória.</span><span class="sxs-lookup"><span data-stu-id="d0df5-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="d0df5-117">Nesse caso, o [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) mapeia diretamente para HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) é mapeado para HeapDestroy.</span><span class="sxs-lookup"><span data-stu-id="d0df5-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="d0df5-118">A seguinte enumeração é usada com o heap:</span><span class="sxs-lookup"><span data-stu-id="d0df5-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="d0df5-119">**\_ID da \_ propriedade da heap do WS \_**</span><span class="sxs-lookup"><span data-stu-id="d0df5-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="d0df5-120">As funções a seguir são usadas com o heap:</span><span class="sxs-lookup"><span data-stu-id="d0df5-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="d0df5-121">**WsAlloc**</span><span class="sxs-lookup"><span data-stu-id="d0df5-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="d0df5-122">**WsCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="d0df5-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="d0df5-123">**WsFreeHeap**</span><span class="sxs-lookup"><span data-stu-id="d0df5-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="d0df5-124">**WsGetHeapProperty**</span><span class="sxs-lookup"><span data-stu-id="d0df5-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="d0df5-125">**WsResetHeap**</span><span class="sxs-lookup"><span data-stu-id="d0df5-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="d0df5-126">O identificador a seguir é usado com o heap:</span><span class="sxs-lookup"><span data-stu-id="d0df5-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="d0df5-127">HEAP do WS \_</span><span class="sxs-lookup"><span data-stu-id="d0df5-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="d0df5-128">As seguintes estruturas são usadas com o heap:</span><span class="sxs-lookup"><span data-stu-id="d0df5-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="d0df5-129">**\_Propriedades de heap do WS \_**</span><span class="sxs-lookup"><span data-stu-id="d0df5-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="d0df5-130">**\_propriedade de heap WS \_**</span><span class="sxs-lookup"><span data-stu-id="d0df5-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




