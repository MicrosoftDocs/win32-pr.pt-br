---
title: Grupo de disparadores
description: Define o grupo de gatilhos.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Agendador de Tarefasdor de gatilho
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086443"
---
# <a name="triggergroup-group"></a><span data-ttu-id="28555-104">Grupo de disparadores</span><span class="sxs-lookup"><span data-stu-id="28555-104">triggerGroup Group</span></span>

<span data-ttu-id="28555-105">Define o grupo de gatilhos.</span><span class="sxs-lookup"><span data-stu-id="28555-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="28555-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="28555-106">Child elements</span></span>



| <span data-ttu-id="28555-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="28555-107">Element</span></span>                                                                                                 | <span data-ttu-id="28555-108">Type</span><span class="sxs-lookup"><span data-stu-id="28555-108">Type</span></span>                                                                                                   | <span data-ttu-id="28555-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="28555-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28555-110">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="28555-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="28555-112">Um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="28555-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="28555-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="28555-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="28555-115">Um gatilho que inicia uma tarefa com base em uma agenda de DOW (dia da semana) diária, semanal, mensal ou mensal.</span><span class="sxs-lookup"><span data-stu-id="28555-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="28555-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="28555-117">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="28555-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="28555-118">Um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="28555-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="28555-119">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="28555-120">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="28555-121">Um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="28555-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="28555-122">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="28555-123">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="28555-124">Um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="28555-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="28555-125">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="28555-126">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="28555-127">Um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="28555-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="28555-128">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="28555-129">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28555-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="28555-130">Um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="28555-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="28555-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="28555-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="28555-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="28555-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="28555-133">Um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="28555-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="28555-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="28555-134">Remarks</span></span>

<span data-ttu-id="28555-135">Ao ler ou gravar XML, os elementos definidos por esse grupo são os elementos filho do elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="28555-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="28555-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28555-136">Requirements</span></span>



| <span data-ttu-id="28555-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="28555-137">Requirement</span></span> | <span data-ttu-id="28555-138">Valor</span><span class="sxs-lookup"><span data-stu-id="28555-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28555-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28555-139">Minimum supported client</span></span><br/> | <span data-ttu-id="28555-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28555-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28555-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28555-141">Minimum supported server</span></span><br/> | <span data-ttu-id="28555-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28555-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28555-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="28555-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28555-144">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="28555-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





