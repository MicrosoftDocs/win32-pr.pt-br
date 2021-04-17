---
title: Método TriggerCollection. Create
description: Para scripts, o cria um novo gatilho para a tarefa.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- disparadores Agendador de Tarefas, criando
- Criar Agendador de Tarefas do método
- Método Create Agendador de tarefas, disparador
- Agendador de Tarefas de objeto TriggerCollection, método Create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768557"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="02cf1-107">Método TriggerCollection. Create</span><span class="sxs-lookup"><span data-stu-id="02cf1-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="02cf1-108">Para scripts, o cria um novo gatilho para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="02cf1-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cf1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02cf1-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="02cf1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02cf1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02cf1-111">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="02cf1-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02cf1-112">Esse parâmetro é definido como uma das seguintes constantes de enumeração [**\_ \_ TYPE2 de gatilho de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .</span><span class="sxs-lookup"><span data-stu-id="02cf1-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="02cf1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="02cf1-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="02cf1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="02cf1-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="02cf1-115"><dt>**Tarefa \_ do \_Evento de gatilho**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="02cf1-116">Dispara a tarefa quando um evento específico ocorre.</span><span class="sxs-lookup"><span data-stu-id="02cf1-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="02cf1-117"><dt>**Tarefa \_ do \_Tempo de gatilho**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="02cf1-118">Dispara a tarefa em uma hora específica do dia.</span><span class="sxs-lookup"><span data-stu-id="02cf1-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="02cf1-119"><dt>**Tarefa \_ do GATILHO \_ diário**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="02cf1-120">Dispara a tarefa em um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="02cf1-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="02cf1-121">Por exemplo, a tarefa é iniciada em uma hora específica todos os dias, a cada dia, a cada terceiro dia e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="02cf1-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="02cf1-122"><dt>**Tarefa \_ do GATILHO \_ semanal**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="02cf1-123">Dispara a tarefa em uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="02cf1-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="02cf1-124">Por exemplo, a tarefa começa às 8:00 em um dia específico toda semana ou outra semana.</span><span class="sxs-lookup"><span data-stu-id="02cf1-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="02cf1-125"><dt>**Tarefa \_ do GATILHO \_ mensal**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="02cf1-126">Dispara a tarefa em um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="02cf1-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="02cf1-127">Por exemplo, a tarefa é iniciada em dias específicos de meses específicos.</span><span class="sxs-lookup"><span data-stu-id="02cf1-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="02cf1-128"><dt>**Tarefa \_ do DISPARAR \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="02cf1-129">Dispara a tarefa em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="02cf1-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="02cf1-130">Por exemplo, a tarefa é iniciada em um período específico da semana, semanas do mês e meses do ano.</span><span class="sxs-lookup"><span data-stu-id="02cf1-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="02cf1-131"><dt>**Tarefa \_ do GATILHO \_ ocioso**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="02cf1-132">Dispara a tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="02cf1-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="02cf1-133"><dt>**Tarefa \_ do \_Registro de gatilho**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="02cf1-134">Dispara a tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="02cf1-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="02cf1-135"><dt>**Tarefa \_ do DISPARAR \_ inicialização**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="02cf1-136">Dispara a tarefa quando o computador é inicializado.</span><span class="sxs-lookup"><span data-stu-id="02cf1-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="02cf1-137"><dt>**Tarefa \_ do \_Logon de gatilho**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="02cf1-138">Dispara a tarefa quando um usuário específico faz logon.</span><span class="sxs-lookup"><span data-stu-id="02cf1-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="02cf1-139"><dt>**Tarefa \_ do DISPARAR \_ \_ \_ alteração de estado de sessão**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="02cf1-140">Dispara a tarefa quando um estado de sessão específico é alterado.</span><span class="sxs-lookup"><span data-stu-id="02cf1-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02cf1-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02cf1-141">Return value</span></span>

<span data-ttu-id="02cf1-142">Um objeto de [**gatilho**](trigger.md) que representa o novo gatilho.</span><span class="sxs-lookup"><span data-stu-id="02cf1-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="02cf1-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="02cf1-143">Remarks</span></span>

<span data-ttu-id="02cf1-144">Para obter informações sobre cada tipo de gatilho, consulte [tipos de gatilho](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="02cf1-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02cf1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02cf1-145">Requirements</span></span>



| <span data-ttu-id="02cf1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="02cf1-146">Requirement</span></span> | <span data-ttu-id="02cf1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="02cf1-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02cf1-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02cf1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="02cf1-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02cf1-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="02cf1-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02cf1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="02cf1-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02cf1-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02cf1-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="02cf1-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="02cf1-153"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02cf1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="02cf1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02cf1-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02cf1-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02cf1-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="02cf1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cf1-157">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="02cf1-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="02cf1-158">**Of**</span><span class="sxs-lookup"><span data-stu-id="02cf1-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





