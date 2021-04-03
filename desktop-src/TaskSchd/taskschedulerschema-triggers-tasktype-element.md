---
title: Elemento Triggers (taskType)
description: Especifica os gatilhos que iniciam a tarefa.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Elemento triggers Agendador de Tarefas
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645213"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="cda32-104">Elemento Triggers (taskType)</span><span class="sxs-lookup"><span data-stu-id="cda32-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="cda32-105">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="cda32-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="cda32-106">O elemento **triggers** é definido pelo tipo complexo [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cda32-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cda32-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="cda32-107">Parent element</span></span>



| <span data-ttu-id="cda32-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cda32-108">Element</span></span>                                          | <span data-ttu-id="cda32-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="cda32-109">Derived from</span></span>                                                 | <span data-ttu-id="cda32-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cda32-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="cda32-111">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="cda32-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="cda32-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="cda32-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="cda32-113">Define a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="cda32-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="cda32-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cda32-114">Child elements</span></span>



| <span data-ttu-id="cda32-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="cda32-115">Element</span></span>                                                                                     | <span data-ttu-id="cda32-116">Type</span><span class="sxs-lookup"><span data-stu-id="cda32-116">Type</span></span>                                                                                       | <span data-ttu-id="cda32-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cda32-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cda32-118">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="cda32-119">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="cda32-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="cda32-120">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="cda32-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="cda32-121">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="cda32-122">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="cda32-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="cda32-123">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="cda32-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="cda32-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="cda32-125">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="cda32-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="cda32-126">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="cda32-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="cda32-127">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="cda32-128">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="cda32-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="cda32-129">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="cda32-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="cda32-130">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="cda32-131">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="cda32-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="cda32-132">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="cda32-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="cda32-133">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="cda32-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="cda32-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="cda32-135">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="cda32-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="cda32-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="cda32-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="cda32-137">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="cda32-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="cda32-138">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="cda32-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="cda32-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda32-139">Remarks</span></span>

<span data-ttu-id="cda32-140">Os elementos filho listados acima podem ser adicionados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="cda32-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="cda32-141">Para desenvolvimento em C++, os gatilhos de uma tarefa são especificados usando a [**Propriedade Triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span><span class="sxs-lookup"><span data-stu-id="cda32-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="cda32-142">Para o desenvolvimento de scripts, os gatilhos de uma tarefa são especificados usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="cda32-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="cda32-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cda32-143">Examples</span></span>

<span data-ttu-id="cda32-144">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="cda32-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda32-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda32-145">Requirements</span></span>



| <span data-ttu-id="cda32-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda32-146">Requirement</span></span> | <span data-ttu-id="cda32-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cda32-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cda32-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda32-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cda32-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cda32-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cda32-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda32-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cda32-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cda32-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cda32-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda32-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda32-153">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cda32-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cda32-154">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cda32-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





