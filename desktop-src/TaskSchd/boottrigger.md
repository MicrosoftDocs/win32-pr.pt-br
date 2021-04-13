---
title: Objeto BootTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando o sistema é inicializado.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- gatilho de inicialização Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto BootTrigger
- Agendador de Tarefas de objeto BootTrigger, descrito
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455988"
---
# <a name="boottrigger-object"></a><span data-ttu-id="16603-106">Objeto BootTrigger</span><span class="sxs-lookup"><span data-stu-id="16603-106">BootTrigger object</span></span>

<span data-ttu-id="16603-107">Objeto de script que representa um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="16603-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="16603-108">Membros</span><span class="sxs-lookup"><span data-stu-id="16603-108">Members</span></span>

<span data-ttu-id="16603-109">O objeto **BootTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16603-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="16603-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16603-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16603-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16603-111">Properties</span></span>

<span data-ttu-id="16603-112">O objeto **BootTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16603-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="16603-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="16603-113">Property</span></span>                                                            | <span data-ttu-id="16603-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="16603-114">Access type</span></span>           | <span data-ttu-id="16603-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="16603-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16603-116">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="16603-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="16603-117">Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="16603-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="16603-118">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="16603-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="16603-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-119">Read/write</span></span><br/> | <span data-ttu-id="16603-120">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-121">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="16603-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="16603-122">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="16603-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="16603-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-123">Read/write</span></span><br/> | <span data-ttu-id="16603-124">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-125">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="16603-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="16603-126">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="16603-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="16603-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="16603-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="16603-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-128">Read/write</span></span><br/> | <span data-ttu-id="16603-129">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-130">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="16603-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="16603-131">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="16603-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="16603-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-132">Read/write</span></span><br/> | <span data-ttu-id="16603-133">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-134">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="16603-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="16603-135">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="16603-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="16603-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-136">Read/write</span></span><br/> | <span data-ttu-id="16603-137">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-138">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="16603-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="16603-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="16603-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="16603-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16603-140">Read/write</span></span><br/> | <span data-ttu-id="16603-141">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-142">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="16603-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="16603-143">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16603-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="16603-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16603-144">Read-only</span></span><br/>  | <span data-ttu-id="16603-145">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="16603-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="16603-146">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="16603-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="16603-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="16603-147">Remarks</span></span>

<span data-ttu-id="16603-148">O serviço de Agendador de Tarefas é iniciado quando o sistema operacional é inicializado e as tarefas de gatilho de inicialização são definidas para iniciar quando o serviço de Agendador de Tarefas é iniciado.</span><span class="sxs-lookup"><span data-stu-id="16603-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="16603-149">Somente um membro do grupo Administradores pode criar uma tarefa com um gatilho de inicialização.</span><span class="sxs-lookup"><span data-stu-id="16603-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="16603-150">Ao criar seu próprio XML para uma tarefa, um gatilho de inicialização é especificado usando o elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="16603-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="16603-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16603-151">Examples</span></span>

<span data-ttu-id="16603-152">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="16603-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16603-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16603-153">Requirements</span></span>



| <span data-ttu-id="16603-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="16603-154">Requirement</span></span> | <span data-ttu-id="16603-155">Valor</span><span class="sxs-lookup"><span data-stu-id="16603-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16603-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16603-156">Minimum supported client</span></span><br/> | <span data-ttu-id="16603-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16603-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="16603-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16603-158">Minimum supported server</span></span><br/> | <span data-ttu-id="16603-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16603-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16603-160">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="16603-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="16603-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="16603-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="16603-162">DLL</span><span class="sxs-lookup"><span data-stu-id="16603-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16603-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16603-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16603-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="16603-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16603-165">**Of**</span><span class="sxs-lookup"><span data-stu-id="16603-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="16603-166">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="16603-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="16603-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="16603-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





