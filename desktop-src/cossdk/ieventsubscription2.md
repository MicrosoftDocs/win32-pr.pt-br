---
description: Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interface IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810541"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="83b7c-104">Interface IEventSubscription2</span><span class="sxs-lookup"><span data-stu-id="83b7c-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="83b7c-105">Armazena e recupera informações sobre assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="83b7c-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="83b7c-106">Essa interface estende a interface [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .</span><span class="sxs-lookup"><span data-stu-id="83b7c-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="83b7c-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="83b7c-107">When to implement</span></span>

<span data-ttu-id="83b7c-108">Você não precisa implementar a interface **IEventSubscription2** .</span><span class="sxs-lookup"><span data-stu-id="83b7c-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="83b7c-109">Uma classe de objeto de evento fornecida pelo sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="83b7c-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="83b7c-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="83b7c-110">When to use</span></span>

<span data-ttu-id="83b7c-111">O sistema de [eventos com+](com--events.md) usa essa interface para obter informações sobre assinaturas individuais.</span><span class="sxs-lookup"><span data-stu-id="83b7c-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="83b7c-112">Membros</span><span class="sxs-lookup"><span data-stu-id="83b7c-112">Members</span></span>

<span data-ttu-id="83b7c-113">A interface **IEventSubscription2** herda de **IEventSubscription**.</span><span class="sxs-lookup"><span data-stu-id="83b7c-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="83b7c-114">**IEventSubscription2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83b7c-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="83b7c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83b7c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83b7c-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83b7c-116">Properties</span></span>

<span data-ttu-id="83b7c-117">A interface **IEventSubscription2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="83b7c-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="83b7c-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="83b7c-118">Property</span></span>                                                                      | <span data-ttu-id="83b7c-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="83b7c-119">Access type</span></span>           | <span data-ttu-id="83b7c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="83b7c-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="83b7c-121">**FilterCriteria**</span><span class="sxs-lookup"><span data-stu-id="83b7c-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="83b7c-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83b7c-122">Read/write</span></span><br/> | <span data-ttu-id="83b7c-123">Os critérios de filtro que regem a assinatura.</span><span class="sxs-lookup"><span data-stu-id="83b7c-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="83b7c-124">**SubscriberMoniker**</span><span class="sxs-lookup"><span data-stu-id="83b7c-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="83b7c-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83b7c-125">Read/write</span></span><br/> | <span data-ttu-id="83b7c-126">O moniker do Assinante.</span><span class="sxs-lookup"><span data-stu-id="83b7c-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="83b7c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83b7c-127">Requirements</span></span>



| <span data-ttu-id="83b7c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b7c-128">Requirement</span></span> | <span data-ttu-id="83b7c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="83b7c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="83b7c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83b7c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83b7c-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83b7c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="83b7c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83b7c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83b7c-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83b7c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="83b7c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="83b7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b7c-135">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="83b7c-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




