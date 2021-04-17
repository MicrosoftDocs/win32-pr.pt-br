---
title: Tipo complexo eventTriggertype
description: Define os elementos filho e as informações de sequenciamento para o elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- tipo complexo de eventTriggertype Agendador de Tarefas
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813038"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="040be-104">Tipo complexo eventTriggertype</span><span class="sxs-lookup"><span data-stu-id="040be-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="040be-105">Define os elementos filho e as informações de sequenciamento para o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="040be-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="040be-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="040be-106">Child elements</span></span>



| <span data-ttu-id="040be-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="040be-107">Element</span></span>                                                                           | <span data-ttu-id="040be-108">Type</span><span class="sxs-lookup"><span data-stu-id="040be-108">Type</span></span>                                                                    | <span data-ttu-id="040be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="040be-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="040be-110">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="040be-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="040be-111">duration</span><span class="sxs-lookup"><span data-stu-id="040be-111">duration</span></span>                                                                | <span data-ttu-id="040be-112">Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="040be-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="040be-113">**Subscription**</span><span class="sxs-lookup"><span data-stu-id="040be-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="040be-114">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="040be-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="040be-115">Especifica a consulta XPath que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="040be-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="040be-116">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="040be-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="040be-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="040be-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="040be-118">Especifica uma sequência de elementos que cada um contém um nome e um valor de consulta XPath.</span><span class="sxs-lookup"><span data-stu-id="040be-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="040be-119">As consultas são aplicadas a um evento retornado da assinatura de evento especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="040be-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="040be-120">O nome para o valor de consulta XPath pode ser usado como uma variável no elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) na seção de ação de " [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md) " de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="040be-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="040be-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="040be-121">Remarks</span></span>

<span data-ttu-id="040be-122">Além do elemento filho definido aqui, o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="040be-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="040be-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040be-123">Requirements</span></span>



| <span data-ttu-id="040be-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="040be-124">Requirement</span></span> | <span data-ttu-id="040be-125">Valor</span><span class="sxs-lookup"><span data-stu-id="040be-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="040be-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="040be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="040be-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="040be-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="040be-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="040be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="040be-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="040be-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="040be-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="040be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040be-131">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="040be-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="040be-132">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="040be-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





