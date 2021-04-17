---
title: Objeto SessionStateChangeTrigger
description: Objeto de script que dispara tarefas para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Agendador de Tarefas de objeto SessionStateChangeTrigger
- Agendador de Tarefas de objeto SessionStateChangeTrigger, descrito
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769392"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="2d513-105">Objeto SessionStateChangeTrigger</span><span class="sxs-lookup"><span data-stu-id="2d513-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="2d513-106">Objeto de script que dispara tarefas para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="2d513-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="2d513-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2d513-107">Members</span></span>

<span data-ttu-id="2d513-108">O objeto **SessionStateChangeTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2d513-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="2d513-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d513-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d513-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d513-110">Properties</span></span>

<span data-ttu-id="2d513-111">O objeto **SessionStateChangeTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d513-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="2d513-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2d513-112">Property</span></span>                                                                | <span data-ttu-id="2d513-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2d513-113">Access type</span></span>           | <span data-ttu-id="2d513-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d513-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d513-115">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="2d513-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="2d513-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-116">Read/write</span></span><br/> | <span data-ttu-id="2d513-117">Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes que uma tarefa seja iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.</span><span class="sxs-lookup"><span data-stu-id="2d513-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="2d513-118">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="2d513-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="2d513-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-119">Read/write</span></span><br/> | <span data-ttu-id="2d513-120">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-121">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2d513-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="2d513-122">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="2d513-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="2d513-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-123">Read/write</span></span><br/> | <span data-ttu-id="2d513-124">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-125">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="2d513-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="2d513-126">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="2d513-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="2d513-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="2d513-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="2d513-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-128">Read/write</span></span><br/> | <span data-ttu-id="2d513-129">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-130">Obtém ou define a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="2d513-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="2d513-131">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="2d513-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="2d513-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-132">Read/write</span></span><br/> | <span data-ttu-id="2d513-133">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-134">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2d513-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="2d513-135">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="2d513-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="2d513-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-136">Read/write</span></span><br/> | <span data-ttu-id="2d513-137">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-138">Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="2d513-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="2d513-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="2d513-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="2d513-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-140">Read/write</span></span><br/> | <span data-ttu-id="2d513-141">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-142">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="2d513-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="2d513-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="2d513-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="2d513-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-144">Read/write</span></span><br/> | <span data-ttu-id="2d513-145">Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.</span><span class="sxs-lookup"><span data-stu-id="2d513-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="2d513-146">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d513-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="2d513-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d513-147">Read-only</span></span><br/>  | <span data-ttu-id="2d513-148">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="2d513-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="2d513-149">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2d513-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="2d513-150">**ID**</span><span class="sxs-lookup"><span data-stu-id="2d513-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="2d513-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2d513-151">Read/write</span></span><br/> | <span data-ttu-id="2d513-152">Obtém ou define o usuário para a sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="2d513-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="2d513-153">Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="2d513-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="2d513-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d513-154">Remarks</span></span>

<span data-ttu-id="2d513-155">Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho de alteração de estado de sessão é especificado usando o elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="2d513-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d513-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d513-156">Requirements</span></span>



| <span data-ttu-id="2d513-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d513-157">Requirement</span></span> | <span data-ttu-id="2d513-158">Valor</span><span class="sxs-lookup"><span data-stu-id="2d513-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d513-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d513-159">Minimum supported client</span></span><br/> | <span data-ttu-id="2d513-160">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d513-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2d513-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d513-161">Minimum supported server</span></span><br/> | <span data-ttu-id="2d513-162">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d513-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d513-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2d513-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d513-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d513-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d513-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2d513-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d513-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d513-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d513-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d513-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d513-168">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="2d513-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="2d513-169">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="2d513-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





