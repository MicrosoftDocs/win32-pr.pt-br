---
title: Objeto de gatilho
description: Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de gatilho.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- disparadores Agendador de Tarefas, objeto de gatilho
- Agendador de Tarefas do objeto de gatilho
- Agendador de Tarefas do objeto de gatilho, descrito
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824280"
---
# <a name="trigger-object"></a><span data-ttu-id="d25a0-106">Objeto de gatilho</span><span class="sxs-lookup"><span data-stu-id="d25a0-106">Trigger object</span></span>

<span data-ttu-id="d25a0-107">Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de gatilho.</span><span class="sxs-lookup"><span data-stu-id="d25a0-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="d25a0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d25a0-108">Members</span></span>

<span data-ttu-id="d25a0-109">O objeto de **gatilho** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d25a0-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="d25a0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d25a0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d25a0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d25a0-111">Properties</span></span>

<span data-ttu-id="d25a0-112">O objeto de **gatilho** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d25a0-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="d25a0-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d25a0-113">Property</span></span>                                                            | <span data-ttu-id="d25a0-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d25a0-114">Access type</span></span>           | <span data-ttu-id="d25a0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d25a0-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d25a0-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="d25a0-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="d25a0-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-117">Read/write</span></span><br/> | <span data-ttu-id="d25a0-118">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d25a0-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="d25a0-119">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="d25a0-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="d25a0-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-120">Read/write</span></span><br/> | <span data-ttu-id="d25a0-121">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="d25a0-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d25a0-122">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="d25a0-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="d25a0-123">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="d25a0-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="d25a0-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-124">Read/write</span></span><br/> | <span data-ttu-id="d25a0-125">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="d25a0-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="d25a0-126">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="d25a0-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="d25a0-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-127">Read/write</span></span><br/> | <span data-ttu-id="d25a0-128">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d25a0-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d25a0-129">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="d25a0-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="d25a0-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-130">Read/write</span></span><br/> | <span data-ttu-id="d25a0-131">Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="d25a0-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="d25a0-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="d25a0-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="d25a0-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d25a0-133">Read/write</span></span><br/> | <span data-ttu-id="d25a0-134">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="d25a0-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="d25a0-135">O gatilho pode iniciar a tarefa depois que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="d25a0-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="d25a0-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d25a0-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="d25a0-137">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d25a0-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d25a0-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d25a0-138">Remarks</span></span>

<span data-ttu-id="d25a0-139">O Agendador de Tarefas fornece os seguintes objetos individuais para os diferentes gatilhos que uma tarefa pode usar:</span><span class="sxs-lookup"><span data-stu-id="d25a0-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="d25a0-140">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="d25a0-141">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="d25a0-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="d25a0-143">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="d25a0-144">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="d25a0-145">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="d25a0-146">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="d25a0-147">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="d25a0-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="d25a0-149">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="d25a0-150">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d25a0-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="d25a0-151">Ao ler ou gravar XML, os gatilhos de uma tarefa são especificados no elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d25a0-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="d25a0-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d25a0-152">Examples</span></span>

<span data-ttu-id="d25a0-153">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="d25a0-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d25a0-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d25a0-154">Requirements</span></span>



| <span data-ttu-id="d25a0-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d25a0-155">Requirement</span></span> | <span data-ttu-id="d25a0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d25a0-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d25a0-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d25a0-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d25a0-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d25a0-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d25a0-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d25a0-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d25a0-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d25a0-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d25a0-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d25a0-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="d25a0-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d25a0-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d25a0-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d25a0-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d25a0-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d25a0-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d25a0-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="d25a0-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25a0-166">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="d25a0-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





