---
title: Elemento ValueQueries (eventTriggertype)
description: Contém uma sequência de elementos que cada um contém um nome e um valor de consulta XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Agendador de Tarefas do elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918141"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="ce82b-104">Elemento ValueQueries (eventTriggertype)</span><span class="sxs-lookup"><span data-stu-id="ce82b-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="ce82b-105">Contém uma sequência de elementos que cada um contém um nome e um valor de consulta XPath.</span><span class="sxs-lookup"><span data-stu-id="ce82b-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="ce82b-106">As consultas são aplicadas a um evento retornado da assinatura de evento especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce82b-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="ce82b-107">O nome do valor de consulta XPath pode ser usado como uma variável na seção de ação de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce82b-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="ce82b-108">O elemento **ValueQueries** é definido pelo tipo complexo [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ce82b-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce82b-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="ce82b-109">Parent element</span></span>



| <span data-ttu-id="ce82b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce82b-110">Element</span></span>                                                                                      | <span data-ttu-id="ce82b-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ce82b-111">Derived from</span></span>                                                                 | <span data-ttu-id="ce82b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce82b-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="ce82b-113">**EventTrigger (The Trigger)**</span><span class="sxs-lookup"><span data-stu-id="ce82b-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="ce82b-114">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="ce82b-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="ce82b-115">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="ce82b-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce82b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce82b-116">Remarks</span></span>

<span data-ttu-id="ce82b-117">Para desenvolvimento em C++, consulte a [**Propriedade ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="ce82b-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="ce82b-118">Para desenvolvimento de script, consulte [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="ce82b-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ce82b-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce82b-119">Examples</span></span>

<span data-ttu-id="ce82b-120">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de evento usando esse elemento, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ce82b-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce82b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce82b-121">Requirements</span></span>



| <span data-ttu-id="ce82b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce82b-122">Requirement</span></span> | <span data-ttu-id="ce82b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce82b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce82b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce82b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce82b-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce82b-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce82b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce82b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce82b-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce82b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

