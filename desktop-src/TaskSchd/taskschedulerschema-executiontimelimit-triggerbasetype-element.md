---
title: Elemento ExecutionTimeLimit (triggerBaseType)
description: Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Agendador de Tarefas do elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455635"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="ceb02-104">Elemento ExecutionTimeLimit (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="ceb02-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="ceb02-105">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="ceb02-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="ceb02-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="ceb02-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="ceb02-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="ceb02-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="ceb02-108">O elemento **ExecutionTimeLimit** é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb02-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ceb02-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="ceb02-109">Parent element</span></span>



| <span data-ttu-id="ceb02-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ceb02-110">Element</span></span>                                                                                     | <span data-ttu-id="ceb02-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ceb02-111">Derived from</span></span>                                                                               | <span data-ttu-id="ceb02-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ceb02-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb02-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="ceb02-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ceb02-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="ceb02-115">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="ceb02-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="ceb02-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="ceb02-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ceb02-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="ceb02-118">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="ceb02-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="ceb02-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="ceb02-120">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="ceb02-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="ceb02-121">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="ceb02-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="ceb02-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="ceb02-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ceb02-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="ceb02-124">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="ceb02-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="ceb02-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="ceb02-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ceb02-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="ceb02-127">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="ceb02-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="ceb02-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="ceb02-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ceb02-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="ceb02-130">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="ceb02-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="ceb02-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="ceb02-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="ceb02-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="ceb02-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="ceb02-133">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="ceb02-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="ceb02-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceb02-134">Remarks</span></span>

<span data-ttu-id="ceb02-135">Para o desenvolvimento de scripts, o limite de tempo de execução é especificado usando a propriedade [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) que é herdada por todos os objetos de gatilho.</span><span class="sxs-lookup"><span data-stu-id="ceb02-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="ceb02-136">Para desenvolvimento em C++, o limite de tempo de execução é especificado usando a propriedade [**ITrigger:: ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) que é herdada por todas as interfaces de gatilho.</span><span class="sxs-lookup"><span data-stu-id="ceb02-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb02-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceb02-137">Requirements</span></span>



| <span data-ttu-id="ceb02-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb02-138">Requirement</span></span> | <span data-ttu-id="ceb02-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb02-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ceb02-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceb02-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb02-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ceb02-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ceb02-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceb02-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb02-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ceb02-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ceb02-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceb02-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb02-145">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="ceb02-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ceb02-146">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="ceb02-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





