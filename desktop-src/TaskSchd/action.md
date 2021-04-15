---
title: Objeto de ação
description: Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de ação.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Agendador de Tarefas de objeto de ação
- Agendador de Tarefas de objeto de ação, descrito
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499528"
---
# <a name="action-object"></a><span data-ttu-id="9cf21-105">Objeto de ação</span><span class="sxs-lookup"><span data-stu-id="9cf21-105">Action object</span></span>

<span data-ttu-id="9cf21-106">Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de ação.</span><span class="sxs-lookup"><span data-stu-id="9cf21-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="9cf21-107">Um objeto Action é criado pelo método [**ActionCollection. Create**](actioncollection-create.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf21-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="9cf21-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9cf21-108">Members</span></span>

<span data-ttu-id="9cf21-109">O objeto de **ação** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9cf21-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="9cf21-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9cf21-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9cf21-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9cf21-111">Properties</span></span>

<span data-ttu-id="9cf21-112">O objeto de **ação** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9cf21-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="9cf21-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9cf21-113">Property</span></span>                               | <span data-ttu-id="9cf21-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="9cf21-114">Access type</span></span>           | <span data-ttu-id="9cf21-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cf21-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="9cf21-116">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="9cf21-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="9cf21-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9cf21-117">Read/write</span></span><br/> | <span data-ttu-id="9cf21-118">Obtém ou define o identificador da ação.</span><span class="sxs-lookup"><span data-stu-id="9cf21-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="9cf21-119">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="9cf21-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="9cf21-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cf21-120">Read-only</span></span><br/>  | <span data-ttu-id="9cf21-121">Obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="9cf21-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="9cf21-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cf21-122">Remarks</span></span>

<span data-ttu-id="9cf21-123">Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [ações da tarefa](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9cf21-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="9cf21-124">A tabela a seguir contém os objetos de script que representam as ações que podem ser executadas:</span><span class="sxs-lookup"><span data-stu-id="9cf21-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="9cf21-125">API</span><span class="sxs-lookup"><span data-stu-id="9cf21-125">API</span></span>                                            | <span data-ttu-id="9cf21-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cf21-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="9cf21-127">**Comhandleaction**</span><span class="sxs-lookup"><span data-stu-id="9cf21-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="9cf21-128">Representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="9cf21-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="9cf21-129">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="9cf21-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="9cf21-130">Representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9cf21-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="9cf21-131">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="9cf21-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="9cf21-132">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9cf21-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="9cf21-133">**Permessageaction**</span><span class="sxs-lookup"><span data-stu-id="9cf21-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="9cf21-134">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9cf21-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="9cf21-135">Ao ler ou gravar XML, as ações de uma tarefa são especificadas no elemento [**ações**](taskschedulerschema-actions-tasktype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9cf21-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9cf21-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9cf21-136">Examples</span></span>

<span data-ttu-id="9cf21-137">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) , [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9cf21-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf21-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cf21-138">Requirements</span></span>



| <span data-ttu-id="9cf21-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cf21-139">Requirement</span></span> | <span data-ttu-id="9cf21-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9cf21-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf21-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cf21-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf21-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cf21-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9cf21-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cf21-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf21-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cf21-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9cf21-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9cf21-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cf21-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9cf21-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9cf21-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9cf21-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cf21-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cf21-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cf21-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cf21-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf21-150">Agendador de Tarefas objetos de script</span><span class="sxs-lookup"><span data-stu-id="9cf21-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="9cf21-151">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9cf21-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





