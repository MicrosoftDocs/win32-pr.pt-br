---
title: Propriedade Trigger. Type
description: Para scripts, obtém o tipo do gatilho.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Agendador de Tarefas de propriedade de tipo
- Propriedade Type Agendador de Tarefas, objeto Trigger
- Agendador de Tarefas de objeto de gatilho, Propriedade Type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644472"
---
# <a name="triggertype-property"></a><span data-ttu-id="fc784-106">Propriedade Trigger. Type</span><span class="sxs-lookup"><span data-stu-id="fc784-106">Trigger.Type property</span></span>

<span data-ttu-id="fc784-107">Para scripts, obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="fc784-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="fc784-108">O tipo de gatilho é definido quando o gatilho é criado e não pode ser alterado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="fc784-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="fc784-109">Para obter informações sobre como criar um gatilho, consulte [**Disparecollection. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="fc784-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc784-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc784-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="fc784-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fc784-111">Property value</span></span>

<span data-ttu-id="fc784-112">Uma das tarefas a [**seguir \_ disparam \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) os valores de enumeração TYPE2.</span><span class="sxs-lookup"><span data-stu-id="fc784-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="fc784-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fc784-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="fc784-114">Significado</span><span class="sxs-lookup"><span data-stu-id="fc784-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="fc784-115"><dt>**Tarefa \_ do \_Evento de gatilho**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="fc784-116">Inicia a tarefa quando ocorre um evento específico.</span><span class="sxs-lookup"><span data-stu-id="fc784-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="fc784-117"><dt>**Tarefa \_ do \_Tempo de gatilho**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="fc784-118">Inicia a tarefa em uma hora específica do dia.</span><span class="sxs-lookup"><span data-stu-id="fc784-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="fc784-119"><dt>**Tarefa \_ do GATILHO \_ diário**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="fc784-120">Inicia a tarefa diariamente.</span><span class="sxs-lookup"><span data-stu-id="fc784-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="fc784-121"><dt>**Tarefa \_ do GATILHO \_ semanal**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="fc784-122">Inicia a tarefa semanalmente.</span><span class="sxs-lookup"><span data-stu-id="fc784-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="fc784-123"><dt>**Tarefa \_ do GATILHO \_ mensal**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="fc784-124">Inicia a tarefa mensalmente.</span><span class="sxs-lookup"><span data-stu-id="fc784-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="fc784-125"><dt>**Tarefa \_ do DISPARAR \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="fc784-126">Inicia a tarefa todos os meses em um dia específico da semana.</span><span class="sxs-lookup"><span data-stu-id="fc784-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="fc784-127"><dt>**Tarefa \_ do GATILHO \_ ocioso**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="fc784-128">Inicia a tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="fc784-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="fc784-129"><dt>**Tarefa \_ do \_Registro de gatilho**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="fc784-130">Inicia a tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="fc784-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="fc784-131"><dt>**Tarefa \_ do DISPARAR \_ inicialização**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="fc784-132">Inicia a tarefa quando o computador é inicializado.</span><span class="sxs-lookup"><span data-stu-id="fc784-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="fc784-133"><dt>**Tarefa \_ do \_Logon de gatilho**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="fc784-134">Inicia a tarefa quando um usuário específico faz logon.</span><span class="sxs-lookup"><span data-stu-id="fc784-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="fc784-135"><dt>**Tarefa \_ do DISPARAR \_ \_ \_ alteração de estado de sessão**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="fc784-136">Dispara a tarefa quando um estado de sessão específico é alterado.</span><span class="sxs-lookup"><span data-stu-id="fc784-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="fc784-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc784-137">Requirements</span></span>



| <span data-ttu-id="fc784-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc784-138">Requirement</span></span> | <span data-ttu-id="fc784-139">Valor</span><span class="sxs-lookup"><span data-stu-id="fc784-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc784-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc784-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fc784-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc784-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fc784-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc784-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fc784-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc784-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc784-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fc784-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc784-145"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc784-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fc784-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc784-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc784-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc784-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc784-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc784-149">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="fc784-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="fc784-150">**Gatilho de tarefa \_ \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="fc784-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="fc784-151">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fc784-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





