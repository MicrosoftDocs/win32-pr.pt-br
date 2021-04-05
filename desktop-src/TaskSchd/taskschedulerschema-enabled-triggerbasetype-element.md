---
title: Elemento Enabled (triggerBaseType)
description: Especifica que o gatilho está habilitado.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Elemento habilitado Agendador de Tarefas
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009761"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="35c2c-104">Elemento Enabled (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="35c2c-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="35c2c-105">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="35c2c-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="35c2c-106">O elemento **Enabled** é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="35c2c-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="35c2c-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="35c2c-107">Parent element</span></span>



| <span data-ttu-id="35c2c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="35c2c-108">Element</span></span>                                                                                     | <span data-ttu-id="35c2c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="35c2c-109">Derived from</span></span>                                                                               | <span data-ttu-id="35c2c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35c2c-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35c2c-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="35c2c-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35c2c-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="35c2c-113">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="35c2c-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="35c2c-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="35c2c-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35c2c-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="35c2c-116">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="35c2c-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="35c2c-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="35c2c-118">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="35c2c-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="35c2c-119">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="35c2c-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="35c2c-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="35c2c-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35c2c-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="35c2c-122">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="35c2c-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="35c2c-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="35c2c-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35c2c-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="35c2c-125">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="35c2c-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="35c2c-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="35c2c-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35c2c-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="35c2c-128">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="35c2c-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="35c2c-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="35c2c-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="35c2c-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="35c2c-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="35c2c-131">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="35c2c-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="35c2c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="35c2c-132">Remarks</span></span>

<span data-ttu-id="35c2c-133">Para o desenvolvimento de scripts, essas informações são acessadas por meio da propriedade [**Trigger. Enabled**](trigger-enabled.md) que é herdada por todos os objetos Trigger.</span><span class="sxs-lookup"><span data-stu-id="35c2c-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="35c2c-134">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITrigger:: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) que é herdada por todas as interfaces de gatilho.</span><span class="sxs-lookup"><span data-stu-id="35c2c-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c2c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35c2c-135">Requirements</span></span>



| <span data-ttu-id="35c2c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c2c-136">Requirement</span></span> | <span data-ttu-id="35c2c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="35c2c-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35c2c-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35c2c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35c2c-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35c2c-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35c2c-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35c2c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35c2c-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35c2c-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35c2c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="35c2c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c2c-143">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="35c2c-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="35c2c-144">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="35c2c-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





