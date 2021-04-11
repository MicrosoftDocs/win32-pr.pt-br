---
title: Objeto timetrigger (Windows. ApplicationModel. Background. h)
description: Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Agendador de Tarefas do gatilho de tempo, objeto
- Agendador de Tarefas de objeto timetrigger
- Agendador de Tarefas de objeto timetrigger, descrito
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295824"
---
# <a name="timetrigger-object"></a><span data-ttu-id="48e63-106">Objeto timetrigger</span><span class="sxs-lookup"><span data-stu-id="48e63-106">TimeTrigger object</span></span>

<span data-ttu-id="48e63-107">Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.</span><span class="sxs-lookup"><span data-stu-id="48e63-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="48e63-108">Membros</span><span class="sxs-lookup"><span data-stu-id="48e63-108">Members</span></span>

<span data-ttu-id="48e63-109">O objeto **timetrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48e63-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="48e63-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48e63-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48e63-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48e63-111">Properties</span></span>

<span data-ttu-id="48e63-112">O objeto **timetrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48e63-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="48e63-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="48e63-113">Property</span></span>                                                            | <span data-ttu-id="48e63-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="48e63-114">Access type</span></span>           | <span data-ttu-id="48e63-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e63-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e63-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="48e63-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="48e63-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-117">Read/write</span></span><br/> | <span data-ttu-id="48e63-118">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-119">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="48e63-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="48e63-120">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="48e63-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="48e63-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-121">Read/write</span></span><br/> | <span data-ttu-id="48e63-122">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-123">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="48e63-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="48e63-124">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="48e63-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="48e63-125">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="48e63-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="48e63-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-126">Read/write</span></span><br/> | <span data-ttu-id="48e63-127">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-128">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="48e63-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="48e63-129">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="48e63-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="48e63-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-130">Read/write</span></span><br/> | <span data-ttu-id="48e63-131">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-132">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="48e63-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="48e63-133">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="48e63-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="48e63-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-134">Read/write</span></span><br/> | <span data-ttu-id="48e63-135">Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="48e63-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="48e63-136">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="48e63-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="48e63-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-137">Read/write</span></span><br/> | <span data-ttu-id="48e63-138">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-139">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="48e63-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="48e63-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="48e63-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="48e63-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="48e63-141">Read/write</span></span><br/> | <span data-ttu-id="48e63-142">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-143">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="48e63-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="48e63-144">Este elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48e63-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="48e63-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48e63-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="48e63-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e63-146">Read-only</span></span><br/>  | <span data-ttu-id="48e63-147">Herdado do [**gatilho**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="48e63-148">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="48e63-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="48e63-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="48e63-149">Remarks</span></span>

<span data-ttu-id="48e63-150">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="48e63-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="48e63-151">Ao ler ou gravar XML para uma tarefa, um gatilho de ociosidade é especificado usando o elemento [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="48e63-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="48e63-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48e63-152">Examples</span></span>

<span data-ttu-id="48e63-153">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="48e63-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48e63-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48e63-154">Requirements</span></span>



| <span data-ttu-id="48e63-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e63-155">Requirement</span></span> | <span data-ttu-id="48e63-156">Valor</span><span class="sxs-lookup"><span data-stu-id="48e63-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e63-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48e63-157">Minimum supported client</span></span><br/> | <span data-ttu-id="48e63-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48e63-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="48e63-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48e63-159">Minimum supported server</span></span><br/> | <span data-ttu-id="48e63-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48e63-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="48e63-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48e63-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e63-162"><dt>Windows. ApplicationModel. Background. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e63-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="48e63-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="48e63-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="48e63-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48e63-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="48e63-165">DLL</span><span class="sxs-lookup"><span data-stu-id="48e63-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e63-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e63-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="48e63-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="48e63-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e63-168">**Of**</span><span class="sxs-lookup"><span data-stu-id="48e63-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="48e63-169">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="48e63-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="48e63-170">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="48e63-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





