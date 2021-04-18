---
description: Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interface IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814004"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="ced7f-104">Interface IEventSubscription3</span><span class="sxs-lookup"><span data-stu-id="ced7f-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="ced7f-105">Armazena e recupera informações sobre assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="ced7f-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="ced7f-106">Essa interface estende a interface [**IEventSubscription2**](ieventsubscription2.md) .</span><span class="sxs-lookup"><span data-stu-id="ced7f-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ced7f-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="ced7f-107">When to implement</span></span>

<span data-ttu-id="ced7f-108">Você não precisa implementar a interface **IEventSubscription3** .</span><span class="sxs-lookup"><span data-stu-id="ced7f-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="ced7f-109">Uma classe de objeto de evento fornecida pelo sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="ced7f-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ced7f-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="ced7f-110">When to use</span></span>

<span data-ttu-id="ced7f-111">O sistema de [eventos com+](com--events.md) usa essa interface para obter informações sobre assinaturas individuais.</span><span class="sxs-lookup"><span data-stu-id="ced7f-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="ced7f-112">Membros</span><span class="sxs-lookup"><span data-stu-id="ced7f-112">Members</span></span>

<span data-ttu-id="ced7f-113">A interface **IEventSubscription3** herda de **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="ced7f-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="ced7f-114">**IEventSubscription3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ced7f-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="ced7f-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ced7f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ced7f-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ced7f-116">Properties</span></span>

<span data-ttu-id="ced7f-117">A interface **IEventSubscription3** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ced7f-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="ced7f-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ced7f-118">Property</span></span>                                                                                  | <span data-ttu-id="ced7f-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ced7f-119">Access type</span></span>           | <span data-ttu-id="ced7f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ced7f-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="ced7f-121">**EventClassApplicationID**</span><span class="sxs-lookup"><span data-stu-id="ced7f-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="ced7f-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ced7f-122">Read/write</span></span><br/> | <span data-ttu-id="ced7f-123">O GUID do aplicativo do objeto da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="ced7f-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="ced7f-124">**EventClassPartitionID**</span><span class="sxs-lookup"><span data-stu-id="ced7f-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="ced7f-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ced7f-125">Read/write</span></span><br/> | <span data-ttu-id="ced7f-126">O GUID da partição do objeto de classe de evento.</span><span class="sxs-lookup"><span data-stu-id="ced7f-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="ced7f-127">**SubscriberApplicationID**</span><span class="sxs-lookup"><span data-stu-id="ced7f-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="ced7f-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ced7f-128">Read/write</span></span><br/> | <span data-ttu-id="ced7f-129">O GUID do aplicativo do Assinante.</span><span class="sxs-lookup"><span data-stu-id="ced7f-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="ced7f-130">**SubscriberPartitionID**</span><span class="sxs-lookup"><span data-stu-id="ced7f-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="ced7f-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ced7f-131">Read/write</span></span><br/> | <span data-ttu-id="ced7f-132">O GUID da partição do Assinante.</span><span class="sxs-lookup"><span data-stu-id="ced7f-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ced7f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced7f-133">Requirements</span></span>



| <span data-ttu-id="ced7f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced7f-134">Requirement</span></span> | <span data-ttu-id="ced7f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ced7f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ced7f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ced7f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ced7f-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ced7f-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ced7f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ced7f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ced7f-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ced7f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ced7f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ced7f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced7f-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="ced7f-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




