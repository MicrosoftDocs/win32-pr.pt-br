---
title: Objeto ActionCollection
description: Objeto de script que contém as ações executadas pela tarefa.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- ações Agendador de Tarefas, objeto de coleção
- Agendador de Tarefas de objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, descrito
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499822"
---
# <a name="actioncollection-object"></a><span data-ttu-id="9c4fb-106">Objeto ActionCollection</span><span class="sxs-lookup"><span data-stu-id="9c4fb-106">ActionCollection object</span></span>

<span data-ttu-id="9c4fb-107">Objeto de script que contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="9c4fb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9c4fb-108">Members</span></span>

<span data-ttu-id="9c4fb-109">O objeto **ActionCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9c4fb-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="9c4fb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c4fb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c4fb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c4fb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c4fb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c4fb-112">Methods</span></span>

<span data-ttu-id="9c4fb-113">O objeto **ActionCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="9c4fb-114">Método</span><span class="sxs-lookup"><span data-stu-id="9c4fb-114">Method</span></span>                                    | <span data-ttu-id="9c4fb-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c4fb-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="9c4fb-116">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="9c4fb-117">Limpa todas as ações da coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="9c4fb-118">**Criar**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="9c4fb-119">Cria e adiciona uma nova ação à coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="9c4fb-120">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="9c4fb-121">Remove uma ação especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="9c4fb-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c4fb-122">Properties</span></span>

<span data-ttu-id="9c4fb-123">O objeto **ActionCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="9c4fb-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9c4fb-124">Property</span></span>                                               | <span data-ttu-id="9c4fb-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="9c4fb-125">Access type</span></span>           | <span data-ttu-id="9c4fb-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c4fb-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="9c4fb-127">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="9c4fb-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9c4fb-128">Read/write</span></span><br/> | <span data-ttu-id="9c4fb-129">Obtém ou define o identificador da entidade de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="9c4fb-130">**Contar**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="9c4fb-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c4fb-131">Read-only</span></span><br/>  | <span data-ttu-id="9c4fb-132">Obtém o número de ações na coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="9c4fb-133">**Item**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="9c4fb-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c4fb-134">Read-only</span></span><br/>  | <span data-ttu-id="9c4fb-135">Obtém uma ação especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="9c4fb-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="9c4fb-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="9c4fb-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9c4fb-137">Read/write</span></span><br/> | <span data-ttu-id="9c4fb-138">Obtém ou define uma versão formatada em XML da coleção.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="9c4fb-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c4fb-139">Remarks</span></span>

<span data-ttu-id="9c4fb-140">Ao ler ou gravar XML, as ações de uma tarefa são especificadas no elemento [**ações**](taskschedulerschema-actions-tasktype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9c4fb-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9c4fb-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c4fb-141">Examples</span></span>

<span data-ttu-id="9c4fb-142">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md), [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9c4fb-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4fb-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c4fb-143">Requirements</span></span>



| <span data-ttu-id="9c4fb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c4fb-144">Requirement</span></span> | <span data-ttu-id="9c4fb-145">Valor</span><span class="sxs-lookup"><span data-stu-id="9c4fb-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4fb-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c4fb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4fb-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c4fb-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9c4fb-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c4fb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4fb-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c4fb-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c4fb-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9c4fb-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c4fb-151"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fb-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c4fb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9c4fb-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c4fb-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c4fb-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





