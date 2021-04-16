---
title: Elemento noboundal (triggerBaseType)
description: Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Elemento de limite de Agendador de Tarefas
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757943"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="91fe7-105">Elemento noboundal (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="91fe7-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="91fe7-106">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="91fe7-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="91fe7-107">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="91fe7-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="91fe7-108">O elemento de **limite** de fim é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="91fe7-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91fe7-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="91fe7-109">Parent element</span></span>



| <span data-ttu-id="91fe7-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="91fe7-110">Element</span></span>                                                                                     | <span data-ttu-id="91fe7-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="91fe7-111">Derived from</span></span>                                                                               | <span data-ttu-id="91fe7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="91fe7-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91fe7-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="91fe7-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="91fe7-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="91fe7-115">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="91fe7-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="91fe7-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="91fe7-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="91fe7-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="91fe7-118">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="91fe7-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="91fe7-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="91fe7-120">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="91fe7-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="91fe7-121">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="91fe7-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="91fe7-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="91fe7-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="91fe7-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="91fe7-124">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="91fe7-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="91fe7-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="91fe7-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="91fe7-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="91fe7-127">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="91fe7-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="91fe7-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="91fe7-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="91fe7-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="91fe7-130">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="91fe7-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="91fe7-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="91fe7-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="91fe7-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="91fe7-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="91fe7-133">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="91fe7-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="91fe7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="91fe7-134">Remarks</span></span>

<span data-ttu-id="91fe7-135">Para o desenvolvimento de scripts, o limite final é especificado usando a propriedade [**Trigger. Endboundal**](trigger-endboundary.md) que é herdada por todos os objetos Trigger.</span><span class="sxs-lookup"><span data-stu-id="91fe7-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="91fe7-136">Para desenvolvimento em C++, o limite final é especificado usando a propriedade [**ITrigger:: Endboundal**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) que é herdada por todas as interfaces de gatilho.</span><span class="sxs-lookup"><span data-stu-id="91fe7-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="91fe7-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91fe7-137">Examples</span></span>

<span data-ttu-id="91fe7-138">O XML a seguir define um elemento de gatilho de inicialização que define um limite final de 1º de janeiro de 2007:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="91fe7-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="91fe7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91fe7-139">Requirements</span></span>



| <span data-ttu-id="91fe7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="91fe7-140">Requirement</span></span> | <span data-ttu-id="91fe7-141">Valor</span><span class="sxs-lookup"><span data-stu-id="91fe7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91fe7-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91fe7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="91fe7-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91fe7-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91fe7-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91fe7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="91fe7-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91fe7-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91fe7-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="91fe7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91fe7-147">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="91fe7-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="91fe7-148">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="91fe7-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





