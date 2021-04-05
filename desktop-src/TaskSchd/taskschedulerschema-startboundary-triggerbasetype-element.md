---
title: Elemento StartBoundary (triggerBaseType)
description: Especifica a data e a hora em que o gatilho é ativado.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Agendador de Tarefas do elemento StartBoundary
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085314"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="5e216-104">Elemento StartBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="5e216-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="5e216-105">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="5e216-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="5e216-106">O elemento **StartBoundary** é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5e216-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5e216-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5e216-107">Parent element</span></span>



| <span data-ttu-id="5e216-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e216-108">Element</span></span>                                                                                     | <span data-ttu-id="5e216-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5e216-109">Derived from</span></span>                                                                               | <span data-ttu-id="5e216-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e216-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e216-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="5e216-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5e216-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="5e216-113">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="5e216-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="5e216-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="5e216-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5e216-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="5e216-116">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="5e216-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="5e216-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="5e216-118">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="5e216-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="5e216-119">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="5e216-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="5e216-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="5e216-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5e216-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="5e216-122">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="5e216-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="5e216-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="5e216-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5e216-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="5e216-125">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="5e216-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="5e216-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="5e216-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5e216-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="5e216-128">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="5e216-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="5e216-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="5e216-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="5e216-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="5e216-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="5e216-131">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="5e216-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="5e216-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e216-132">Remarks</span></span>

<span data-ttu-id="5e216-133">O **<StartBoundary>** elemento é um elemento necessário para gatilhos de tempo e calendário ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="5e216-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="5e216-134">Para o desenvolvimento de scripts, o limite final é especificado usando a propriedade [**Trigger. StartBoundary**](trigger-startboundary.md) que é herdada por todos os objetos Trigger.</span><span class="sxs-lookup"><span data-stu-id="5e216-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="5e216-135">Para desenvolvimento em C++, o limite final é especificado usando a propriedade [**ITrigger:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) que é herdada por todas as interfaces de gatilho.</span><span class="sxs-lookup"><span data-stu-id="5e216-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="5e216-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e216-136">Examples</span></span>

<span data-ttu-id="5e216-137">O XML a seguir define um elemento de gatilho de inicialização que define um limite inicial de 1º de janeiro de 2005:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="5e216-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="5e216-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e216-138">Requirements</span></span>



| <span data-ttu-id="5e216-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e216-139">Requirement</span></span> | <span data-ttu-id="5e216-140">Valor</span><span class="sxs-lookup"><span data-stu-id="5e216-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e216-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e216-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5e216-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e216-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e216-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e216-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5e216-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e216-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e216-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e216-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e216-146">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5e216-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5e216-147">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5e216-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





