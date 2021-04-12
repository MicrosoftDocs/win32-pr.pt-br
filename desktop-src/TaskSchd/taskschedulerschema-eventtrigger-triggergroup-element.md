---
title: Elemento EventTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Agendador de Tarefas de gatilho de evento, elemento
- Agendador de Tarefas de elemento EventTrigger
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455634"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="592f9-105">Elemento EventTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="592f9-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="592f9-106">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="592f9-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="592f9-107">O elemento **EventTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="592f9-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="592f9-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="592f9-108">Parent element</span></span>



| <span data-ttu-id="592f9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="592f9-109">Element</span></span>                                                           | <span data-ttu-id="592f9-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="592f9-110">Derived from</span></span>                                                         | <span data-ttu-id="592f9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="592f9-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="592f9-112">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="592f9-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="592f9-113">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="592f9-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="592f9-114">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="592f9-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="592f9-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="592f9-115">Child elements</span></span>



| <span data-ttu-id="592f9-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="592f9-116">Element</span></span>                                                                                              | <span data-ttu-id="592f9-117">Type</span><span class="sxs-lookup"><span data-stu-id="592f9-117">Type</span></span>                                                                     | <span data-ttu-id="592f9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="592f9-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="592f9-119">**Atraso (eventTriggertype)**</span><span class="sxs-lookup"><span data-stu-id="592f9-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="592f9-120">duration</span><span class="sxs-lookup"><span data-stu-id="592f9-120">duration</span></span>                                                                 | <span data-ttu-id="592f9-121">Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="592f9-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="592f9-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="592f9-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="592f9-123">booleano</span><span class="sxs-lookup"><span data-stu-id="592f9-123">boolean</span></span>                                                                  | <span data-ttu-id="592f9-124">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="592f9-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="592f9-125">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="592f9-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="592f9-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="592f9-126">dateTime</span></span>                                                                 | <span data-ttu-id="592f9-127">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="592f9-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="592f9-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="592f9-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="592f9-129">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="592f9-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="592f9-130">**repetição**</span><span class="sxs-lookup"><span data-stu-id="592f9-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="592f9-131">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="592f9-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="592f9-132">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="592f9-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="592f9-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="592f9-133">dateTime</span></span>                                                                 | <span data-ttu-id="592f9-134">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="592f9-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="592f9-135">**Assinatura (eventTriggertype)**</span><span class="sxs-lookup"><span data-stu-id="592f9-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="592f9-136">string</span><span class="sxs-lookup"><span data-stu-id="592f9-136">string</span></span>                                                                   | <span data-ttu-id="592f9-137">Especifica a consulta XPath que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="592f9-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="592f9-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="592f9-138">Attributes</span></span>



| <span data-ttu-id="592f9-139">Nome</span><span class="sxs-lookup"><span data-stu-id="592f9-139">Name</span></span> | <span data-ttu-id="592f9-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="592f9-140">Type</span></span> | <span data-ttu-id="592f9-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="592f9-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="592f9-142">ID</span><span class="sxs-lookup"><span data-stu-id="592f9-142">Id</span></span>   | <span data-ttu-id="592f9-143">ID</span><span class="sxs-lookup"><span data-stu-id="592f9-143">ID</span></span>   | <span data-ttu-id="592f9-144">Identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="592f9-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="592f9-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="592f9-145">Remarks</span></span>

<span data-ttu-id="592f9-146">Um máximo de 500 tarefas com assinaturas de evento podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="592f9-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="592f9-147">Uma assinatura de evento que consulta uma variedade de eventos pode ser usada para disparar uma tarefa que usa a mesma ação em resposta aos eventos que estão sendo registrados.</span><span class="sxs-lookup"><span data-stu-id="592f9-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="592f9-148">Para o desenvolvimento de script, um gatilho de evento é definido pelo objeto [**EventTrigger**](eventtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="592f9-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="592f9-149">Para desenvolvimento em C++, um gatilho de evento é definido pela interface [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .</span><span class="sxs-lookup"><span data-stu-id="592f9-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="592f9-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="592f9-150">Examples</span></span>

<span data-ttu-id="592f9-151">Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="592f9-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="592f9-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="592f9-152">Requirements</span></span>



| <span data-ttu-id="592f9-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="592f9-153">Requirement</span></span> | <span data-ttu-id="592f9-154">Valor</span><span class="sxs-lookup"><span data-stu-id="592f9-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="592f9-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="592f9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="592f9-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="592f9-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="592f9-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="592f9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="592f9-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="592f9-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="592f9-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="592f9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592f9-160">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="592f9-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

