---
title: Interface IReferenceClock
description: A interface IReferenceClock fornece acesso a um relógio externo. Essa interface é fornecida para permitir que todas as rotinas de renderização sejam sincronizadas com o mesmo relógio. Essa interface pode ser Obtida de um objeto leitor.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Formato de mídia do Windows da interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, descrito
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105773099"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="83484-106">Interface IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="83484-106">IReferenceClock interface</span></span>

<span data-ttu-id="83484-107">A interface **IReferenceClock** fornece acesso a um relógio externo.</span><span class="sxs-lookup"><span data-stu-id="83484-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="83484-108">Essa interface é fornecida para permitir que todas as rotinas de renderização sejam sincronizadas com o mesmo relógio.</span><span class="sxs-lookup"><span data-stu-id="83484-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="83484-109">Essa interface pode ser Obtida de um objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="83484-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="83484-110">Membros</span><span class="sxs-lookup"><span data-stu-id="83484-110">Members</span></span>

<span data-ttu-id="83484-111">A interface **IReferenceClock** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="83484-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="83484-112">**IReferenceClock** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83484-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="83484-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="83484-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="83484-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="83484-114">Methods</span></span>

<span data-ttu-id="83484-115">A interface **IReferenceClock** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="83484-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="83484-116">Método</span><span class="sxs-lookup"><span data-stu-id="83484-116">Method</span></span>                                                   | <span data-ttu-id="83484-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="83484-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="83484-118">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="83484-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="83484-119">Não implementado por este SDK.</span><span class="sxs-lookup"><span data-stu-id="83484-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="83484-120">**Aviso de**</span><span class="sxs-lookup"><span data-stu-id="83484-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="83484-121">Solicita uma notificação assíncrona que um tempo decorreu.</span><span class="sxs-lookup"><span data-stu-id="83484-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="83484-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="83484-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="83484-123">Recupera o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="83484-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="83484-124">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="83484-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="83484-125">Cancela uma solicitação de notificação.</span><span class="sxs-lookup"><span data-stu-id="83484-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="83484-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="83484-126">Remarks</span></span>

<span data-ttu-id="83484-127">Para obter informações sobre outras interfaces que podem ser obtidas usando o método QueryInterface dessa interface, consulte leitor Object.</span><span class="sxs-lookup"><span data-stu-id="83484-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="83484-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="83484-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83484-129">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="83484-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

