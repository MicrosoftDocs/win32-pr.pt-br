---
title: Objeto LogonTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando um usuário faz logon.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- gatilho de logon Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto LogonTrigger
- Agendador de Tarefas de objeto LogonTrigger, descrito
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918747"
---
# <a name="logontrigger-object"></a><span data-ttu-id="f9654-106">Objeto LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="f9654-106">LogonTrigger object</span></span>

<span data-ttu-id="f9654-107">Objeto de script que representa um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="f9654-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="f9654-108">Quando o serviço de Agendador de Tarefas é iniciado, todos os usuários conectados são enumerados e todas as tarefas registradas com gatilhos de logon que correspondem ao usuário conectado são executadas.</span><span class="sxs-lookup"><span data-stu-id="f9654-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="f9654-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f9654-109">Members</span></span>

<span data-ttu-id="f9654-110">O objeto **LogonTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f9654-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="f9654-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9654-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9654-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9654-112">Properties</span></span>

<span data-ttu-id="f9654-113">O objeto **LogonTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9654-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="f9654-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f9654-114">Property</span></span>                                                            | <span data-ttu-id="f9654-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f9654-115">Access type</span></span>           | <span data-ttu-id="f9654-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9654-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9654-117">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="f9654-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="f9654-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-118">Read/write</span></span><br/> | <span data-ttu-id="f9654-119">Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando o trabalho é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f9654-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="f9654-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="f9654-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="f9654-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-121">Read/write</span></span><br/> | <span data-ttu-id="f9654-122">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-123">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f9654-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="f9654-124">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="f9654-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="f9654-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-125">Read/write</span></span><br/> | <span data-ttu-id="f9654-126">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-127">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="f9654-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f9654-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="f9654-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="f9654-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="f9654-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="f9654-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-130">Read/write</span></span><br/> | <span data-ttu-id="f9654-131">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-132">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f9654-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="f9654-133">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="f9654-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="f9654-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-134">Read/write</span></span><br/> | <span data-ttu-id="f9654-135">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-136">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f9654-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f9654-137">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="f9654-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="f9654-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-138">Read/write</span></span><br/> | <span data-ttu-id="f9654-139">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-140">Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f9654-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="f9654-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="f9654-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="f9654-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-142">Read/write</span></span><br/> | <span data-ttu-id="f9654-143">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-144">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="f9654-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="f9654-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9654-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="f9654-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f9654-146">Read-only</span></span><br/>  | <span data-ttu-id="f9654-147">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="f9654-148">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f9654-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="f9654-149">**ID**</span><span class="sxs-lookup"><span data-stu-id="f9654-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="f9654-150">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f9654-150">Read/write</span></span><br/> | <span data-ttu-id="f9654-151">Obtém ou define o identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9654-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f9654-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9654-152">Remarks</span></span>

<span data-ttu-id="f9654-153">Se você quiser que uma tarefa seja disparada quando qualquer membro de um grupo fizer logon no computador em vez de quando um usuário específico fizer logon, não atribua um valor à propriedade [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="f9654-154">Em vez disso, crie um gatilho de logon com uma propriedade **LogonTrigger. UserID** vazia e atribua um valor para a entidade de segurança da tarefa usando a propriedade [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="f9654-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="f9654-155">Ao ler ou gravar XML para uma tarefa, um gatilho de logon é especificado usando o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f9654-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="f9654-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9654-156">Examples</span></span>

<span data-ttu-id="f9654-157">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="f9654-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9654-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9654-158">Requirements</span></span>



| <span data-ttu-id="f9654-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9654-159">Requirement</span></span> | <span data-ttu-id="f9654-160">Valor</span><span class="sxs-lookup"><span data-stu-id="f9654-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9654-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9654-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f9654-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9654-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f9654-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9654-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f9654-164">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9654-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9654-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9654-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9654-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9654-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9654-167">DLL</span><span class="sxs-lookup"><span data-stu-id="f9654-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9654-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9654-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9654-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9654-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9654-170">**Of**</span><span class="sxs-lookup"><span data-stu-id="f9654-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





