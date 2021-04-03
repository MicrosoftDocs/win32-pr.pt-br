---
title: Elemento Subscription (eventTriggertype)
description: Especifica a consulta XPath que identifica o evento que dispara o gatilho.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Elemento de assinatura Agendador de Tarefas
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645216"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="5205d-104">Elemento Subscription (eventTriggertype)</span><span class="sxs-lookup"><span data-stu-id="5205d-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="5205d-105">Especifica a consulta XPath que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="5205d-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="5205d-106">O elemento **Subscription** é definido pelo tipo complexo [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5205d-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5205d-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5205d-107">Parent element</span></span>



| <span data-ttu-id="5205d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5205d-108">Element</span></span>                                                                       | <span data-ttu-id="5205d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5205d-109">Derived from</span></span>                                                                 | <span data-ttu-id="5205d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5205d-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5205d-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="5205d-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="5205d-112">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="5205d-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="5205d-113">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="5205d-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5205d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5205d-114">Remarks</span></span>

<span data-ttu-id="5205d-115">Para o desenvolvimento de script, a assinatura de evento é especificada pela propriedade [**EventTrigger. Subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="5205d-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="5205d-116">Para desenvolvimento em C++, a assinatura de evento é especificada pela propriedade [**IEventTrigger:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .</span><span class="sxs-lookup"><span data-stu-id="5205d-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5205d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5205d-117">Requirements</span></span>



| <span data-ttu-id="5205d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5205d-118">Requirement</span></span> | <span data-ttu-id="5205d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5205d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5205d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5205d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5205d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5205d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5205d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5205d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5205d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5205d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5205d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5205d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5205d-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5205d-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5205d-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5205d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





