---
title: Tipo complexo triggerBaseType
description: Define o atributo, os elementos filho de base e as informações de sequenciamento para todos os tipos complexos de gatilho.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- Agendador de Tarefas tipo complexo triggerBaseType
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295907"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="2df59-104">Tipo complexo triggerBaseType</span><span class="sxs-lookup"><span data-stu-id="2df59-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="2df59-105">Define o atributo, os elementos filho de base e as informações de sequenciamento para todos os tipos complexos de gatilho.</span><span class="sxs-lookup"><span data-stu-id="2df59-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2df59-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2df59-106">Child elements</span></span>



| <span data-ttu-id="2df59-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2df59-107">Element</span></span>                                                                                      | <span data-ttu-id="2df59-108">Type</span><span class="sxs-lookup"><span data-stu-id="2df59-108">Type</span></span>                                                                     | <span data-ttu-id="2df59-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2df59-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2df59-110">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="2df59-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="2df59-111">booleano</span><span class="sxs-lookup"><span data-stu-id="2df59-111">boolean</span></span>                                                                  | <span data-ttu-id="2df59-112">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2df59-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="2df59-113">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="2df59-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="2df59-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="2df59-114">dateTime</span></span>                                                                 | <span data-ttu-id="2df59-115">A data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="2df59-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="2df59-116">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="2df59-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="2df59-117">duration</span><span class="sxs-lookup"><span data-stu-id="2df59-117">duration</span></span>                                                                 | <span data-ttu-id="2df59-118">Especifica o intervalo quando o gatilho pode iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="2df59-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="2df59-119">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="2df59-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="2df59-120">**repetição**</span><span class="sxs-lookup"><span data-stu-id="2df59-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="2df59-121">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido quando o gatilho é acionado.</span><span class="sxs-lookup"><span data-stu-id="2df59-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="2df59-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="2df59-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="2df59-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="2df59-123">dateTime</span></span>                                                                 | <span data-ttu-id="2df59-124">A data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="2df59-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="2df59-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="2df59-125">Attributes</span></span>



| <span data-ttu-id="2df59-126">Nome</span><span class="sxs-lookup"><span data-stu-id="2df59-126">Name</span></span> | <span data-ttu-id="2df59-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2df59-127">Type</span></span> | <span data-ttu-id="2df59-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="2df59-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="2df59-129">id</span><span class="sxs-lookup"><span data-stu-id="2df59-129">id</span></span>   | <span data-ttu-id="2df59-130">ID</span><span class="sxs-lookup"><span data-stu-id="2df59-130">ID</span></span>   | <span data-ttu-id="2df59-131">Identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2df59-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2df59-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="2df59-132">Remarks</span></span>

<span data-ttu-id="2df59-133">Os tipos complexos de gatilho incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="2df59-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="2df59-134">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2df59-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="2df59-135">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2df59-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="2df59-136">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="2df59-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="2df59-137">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2df59-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="2df59-138">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2df59-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="2df59-139">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2df59-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="2df59-140">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="2df59-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="2df59-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2df59-141">Requirements</span></span>



| <span data-ttu-id="2df59-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2df59-142">Requirement</span></span> | <span data-ttu-id="2df59-143">Valor</span><span class="sxs-lookup"><span data-stu-id="2df59-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2df59-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2df59-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2df59-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2df59-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2df59-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2df59-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2df59-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2df59-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2df59-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2df59-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df59-149">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2df59-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="2df59-150">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2df59-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





