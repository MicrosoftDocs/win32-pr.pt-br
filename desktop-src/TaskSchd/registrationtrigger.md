---
title: Objeto RegistrationTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- gatilho de registro Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RegistrationTrigger
- Agendador de Tarefas de objeto RegistrationTrigger, descrito
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499475"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="f5e90-106">Objeto RegistrationTrigger</span><span class="sxs-lookup"><span data-stu-id="f5e90-106">RegistrationTrigger object</span></span>

<span data-ttu-id="f5e90-107">Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="f5e90-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="f5e90-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f5e90-108">Members</span></span>

<span data-ttu-id="f5e90-109">O objeto **RegistrationTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f5e90-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="f5e90-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5e90-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5e90-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5e90-111">Properties</span></span>

<span data-ttu-id="f5e90-112">O objeto **RegistrationTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5e90-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="f5e90-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f5e90-113">Property</span></span>                                                            | <span data-ttu-id="f5e90-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f5e90-114">Access type</span></span>           | <span data-ttu-id="f5e90-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5e90-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5e90-116">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="f5e90-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="f5e90-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-117">Read/write</span></span><br/> | <span data-ttu-id="f5e90-118">Obtém ou define o período de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f5e90-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="f5e90-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="f5e90-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="f5e90-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-120">Read/write</span></span><br/> | <span data-ttu-id="f5e90-121">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-122">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f5e90-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="f5e90-123">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="f5e90-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="f5e90-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-124">Read/write</span></span><br/> | <span data-ttu-id="f5e90-125">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-126">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="f5e90-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f5e90-127">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="f5e90-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="f5e90-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="f5e90-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="f5e90-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-129">Read/write</span></span><br/> | <span data-ttu-id="f5e90-130">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-131">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f5e90-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="f5e90-132">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="f5e90-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="f5e90-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-133">Read/write</span></span><br/> | <span data-ttu-id="f5e90-134">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-135">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f5e90-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="f5e90-136">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="f5e90-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="f5e90-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-137">Read/write</span></span><br/> | <span data-ttu-id="f5e90-138">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-139">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f5e90-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="f5e90-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="f5e90-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="f5e90-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5e90-141">Read/write</span></span><br/> | <span data-ttu-id="f5e90-142">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-143">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="f5e90-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="f5e90-144">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="f5e90-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="f5e90-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5e90-145">Read-only</span></span><br/>  | <span data-ttu-id="f5e90-146">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e90-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f5e90-147">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f5e90-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="f5e90-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5e90-148">Remarks</span></span>

<span data-ttu-id="f5e90-149">Ao criar seu próprio XML para uma tarefa, um gatilho de registro é especificado usando o elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f5e90-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="f5e90-150">Se uma tarefa com um gatilho de registro atrasado for registrada e o computador em que a tarefa está registrada for desligado ou reiniciado durante o atraso, antes da execução da tarefa, a tarefa não será executada e o atraso será perdido.</span><span class="sxs-lookup"><span data-stu-id="f5e90-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="f5e90-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5e90-151">Examples</span></span>

<span data-ttu-id="f5e90-152">Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="f5e90-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e90-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e90-153">Requirements</span></span>



| <span data-ttu-id="f5e90-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e90-154">Requirement</span></span> | <span data-ttu-id="f5e90-155">Valor</span><span class="sxs-lookup"><span data-stu-id="f5e90-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e90-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5e90-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e90-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5e90-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f5e90-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5e90-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e90-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5e90-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5e90-160">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f5e90-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5e90-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f5e90-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f5e90-162">DLL</span><span class="sxs-lookup"><span data-stu-id="f5e90-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5e90-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5e90-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e90-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5e90-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e90-165">**Of**</span><span class="sxs-lookup"><span data-stu-id="f5e90-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="f5e90-166">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="f5e90-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="f5e90-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="f5e90-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





