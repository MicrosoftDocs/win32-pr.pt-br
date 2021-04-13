---
title: Objeto EventTrigger (Windows. UI. XAML. h)
description: Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre um evento do sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Agendador de Tarefas de gatilho de evento, objeto
- Agendador de Tarefas de objeto EventTrigger
- Agendador de Tarefas de objeto EventTrigger, descrito
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499650"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="fe9c8-106">Objeto EventTrigger</span><span class="sxs-lookup"><span data-stu-id="fe9c8-106">EventTrigger object</span></span>

<span data-ttu-id="fe9c8-107">Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="fe9c8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fe9c8-108">Members</span></span>

<span data-ttu-id="fe9c8-109">O objeto **EventTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fe9c8-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="fe9c8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe9c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe9c8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe9c8-111">Properties</span></span>

<span data-ttu-id="fe9c8-112">O objeto **EventTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="fe9c8-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fe9c8-113">Property</span></span>                                                            | <span data-ttu-id="fe9c8-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fe9c8-114">Access type</span></span>           | <span data-ttu-id="fe9c8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe9c8-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe9c8-116">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="fe9c8-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-117">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-118">Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="fe9c8-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="fe9c8-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-120">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-121">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-122">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="fe9c8-123">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="fe9c8-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-124">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-125">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-126">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="fe9c8-127">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="fe9c8-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="fe9c8-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-129">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-130">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-131">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada por esse gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="fe9c8-132">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="fe9c8-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-133">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-134">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-135">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="fe9c8-136">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="fe9c8-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-137">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-138">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-139">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="fe9c8-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="fe9c8-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-141">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-142">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-143">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="fe9c8-144">**Subscription**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="fe9c8-145">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-145">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-146">Obtém ou define a cadeia de caracteres de consulta XPath que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="fe9c8-147">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="fe9c8-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe9c8-148">Read-only</span></span><br/>  | <span data-ttu-id="fe9c8-149">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="fe9c8-150">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="fe9c8-151">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="fe9c8-152">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe9c8-152">Read/write</span></span><br/> | <span data-ttu-id="fe9c8-153">Obtém ou define uma coleção de consultas XPath nomeadas.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="fe9c8-154">Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de [**assinatura**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="fe9c8-155">O nome da consulta pode ser usado como uma variável na mensagem de uma ação de [**Exmessageaction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="fe9c8-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe9c8-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe9c8-156">Remarks</span></span>

<span data-ttu-id="fe9c8-157">Um máximo de 500 tarefas com assinaturas de evento podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="fe9c8-158">Uma assinatura de evento que consulta uma variedade de eventos pode ser usada para disparar uma tarefa que usa a mesma ação em resposta aos eventos que estão sendo registrados.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="fe9c8-159">Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho de evento é especificado usando o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fe9c8-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="fe9c8-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe9c8-160">Examples</span></span>

<span data-ttu-id="fe9c8-161">Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho de evento (script)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe9c8-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9c8-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe9c8-162">Requirements</span></span>



| <span data-ttu-id="fe9c8-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe9c8-163">Requirement</span></span> | <span data-ttu-id="fe9c8-164">Valor</span><span class="sxs-lookup"><span data-stu-id="fe9c8-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9c8-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe9c8-165">Minimum supported client</span></span><br/> | <span data-ttu-id="fe9c8-166">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe9c8-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe9c8-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe9c8-167">Minimum supported server</span></span><br/> | <span data-ttu-id="fe9c8-168">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe9c8-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe9c8-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe9c8-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe9c8-170"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9c8-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="fe9c8-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fe9c8-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe9c8-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe9c8-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="fe9c8-173">DLL</span><span class="sxs-lookup"><span data-stu-id="fe9c8-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe9c8-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe9c8-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="fe9c8-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe9c8-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9c8-176">**Of**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="fe9c8-177">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="fe9c8-178">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="fe9c8-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

