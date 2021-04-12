---
title: Elemento repetition (triggerBaseType)
description: Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento de repetição Agendador de Tarefas
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455500"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="35bb8-104">Elemento repetition (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="35bb8-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="35bb8-105">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="35bb8-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="35bb8-106">O elemento de **repetição** é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="35bb8-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="35bb8-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="35bb8-107">Parent element</span></span>



| <span data-ttu-id="35bb8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="35bb8-108">Element</span></span>                                                                                     | <span data-ttu-id="35bb8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="35bb8-109">Derived from</span></span>                                                                               | <span data-ttu-id="35bb8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35bb8-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35bb8-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb8-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb8-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="35bb8-113">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="35bb8-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="35bb8-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="35bb8-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb8-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="35bb8-116">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="35bb8-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="35bb8-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="35bb8-118">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="35bb8-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="35bb8-119">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="35bb8-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="35bb8-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb8-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb8-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="35bb8-122">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="35bb8-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="35bb8-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="35bb8-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb8-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="35bb8-125">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="35bb8-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="35bb8-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="35bb8-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb8-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="35bb8-128">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="35bb8-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="35bb8-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb8-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb8-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="35bb8-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="35bb8-131">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="35bb8-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="35bb8-132">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="35bb8-132">Child elements</span></span>



| <span data-ttu-id="35bb8-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="35bb8-133">Element</span></span>                                                                                   | <span data-ttu-id="35bb8-134">Type</span><span class="sxs-lookup"><span data-stu-id="35bb8-134">Type</span></span>     | <span data-ttu-id="35bb8-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="35bb8-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35bb8-136">**Permanência**</span><span class="sxs-lookup"><span data-stu-id="35bb8-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="35bb8-137">duration</span><span class="sxs-lookup"><span data-stu-id="35bb8-137">duration</span></span> | <span data-ttu-id="35bb8-138">Especifica por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="35bb8-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="35bb8-139">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="35bb8-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="35bb8-140">duration</span><span class="sxs-lookup"><span data-stu-id="35bb8-140">duration</span></span> | <span data-ttu-id="35bb8-141">Especifica a quantidade de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="35bb8-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="35bb8-142">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="35bb8-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="35bb8-143">booleano</span><span class="sxs-lookup"><span data-stu-id="35bb8-143">boolean</span></span>  | <span data-ttu-id="35bb8-144">Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="35bb8-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35bb8-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="35bb8-145">Remarks</span></span>

<span data-ttu-id="35bb8-146">Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.</span><span class="sxs-lookup"><span data-stu-id="35bb8-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="35bb8-147">Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes.</span><span class="sxs-lookup"><span data-stu-id="35bb8-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="35bb8-148">As cinco repetições podem ser definidas pelo padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="35bb8-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="35bb8-149">Uma tarefa é iniciada no início do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="35bb8-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="35bb8-150">A próxima tarefa é iniciada no final do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="35bb8-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="35bb8-151">A próxima tarefa é iniciada no final do segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="35bb8-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="35bb8-152">A próxima tarefa começa no final do terceiro minuto.</span><span class="sxs-lookup"><span data-stu-id="35bb8-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="35bb8-153">A próxima tarefa é iniciada no final do quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="35bb8-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="35bb8-154">**Windows Server 2003, Windows XP e windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.</span><span class="sxs-lookup"><span data-stu-id="35bb8-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="35bb8-155">**Windows Vista, Windows 7, Windows server 2008, Windows 8 e Windows Server 2012:** Normalmente, definir a duração da repetição como um múltiplo exato do intervalo produz os números descritos acima.</span><span class="sxs-lookup"><span data-stu-id="35bb8-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="35bb8-156">No entanto, sob determinadas condições de carga pesada, é possível que a duração do tempo limite seja iniciada antes que TaskScheduler possa iniciar o intervalo final da tarefa.</span><span class="sxs-lookup"><span data-stu-id="35bb8-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="35bb8-157">Para o desenvolvimento de scripts, o padrão de repetição é especificado usando a propriedade [**Trigger. Repetition**](trigger-repetition.md) que é herdada por todos os objetos Trigger.</span><span class="sxs-lookup"><span data-stu-id="35bb8-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="35bb8-158">Para desenvolvimento em C++, o padrão de repetição é especificado usando a propriedade [**ITRigger:: repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) que é herdada por todas as interfaces de gatilho.</span><span class="sxs-lookup"><span data-stu-id="35bb8-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="35bb8-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35bb8-159">Examples</span></span>

<span data-ttu-id="35bb8-160">O XML a seguir define um elemento de gatilho de inicialização que especifica um padrão de repetição para um gatilho.</span><span class="sxs-lookup"><span data-stu-id="35bb8-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="35bb8-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35bb8-161">Requirements</span></span>



| <span data-ttu-id="35bb8-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="35bb8-162">Requirement</span></span> | <span data-ttu-id="35bb8-163">Valor</span><span class="sxs-lookup"><span data-stu-id="35bb8-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35bb8-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35bb8-164">Minimum supported client</span></span><br/> | <span data-ttu-id="35bb8-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35bb8-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35bb8-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35bb8-166">Minimum supported server</span></span><br/> | <span data-ttu-id="35bb8-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35bb8-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35bb8-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="35bb8-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35bb8-169">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="35bb8-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="35bb8-170">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="35bb8-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





