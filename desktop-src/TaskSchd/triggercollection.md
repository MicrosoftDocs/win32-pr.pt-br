---
title: Objeto TriggerCollection (Windows. UI. XAML. h)
description: Objeto de script que é usado para adicionar, remover e recuperar os gatilhos de uma tarefa.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- disparadores Agendador de Tarefas, objeto de coleção de gatilho
- Agendador de Tarefas de objeto TriggerCollection
- Agendador de Tarefas de objeto TriggerCollection, descrito
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085360"
---
# <a name="triggercollection-object"></a><span data-ttu-id="e198b-106">Objeto TriggerCollection</span><span class="sxs-lookup"><span data-stu-id="e198b-106">TriggerCollection object</span></span>

<span data-ttu-id="e198b-107">Objeto de script que é usado para adicionar, remover e recuperar os gatilhos de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e198b-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="e198b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e198b-108">Members</span></span>

<span data-ttu-id="e198b-109">O objeto **TriggerCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e198b-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="e198b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e198b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e198b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e198b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e198b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e198b-112">Methods</span></span>

<span data-ttu-id="e198b-113">O objeto **TriggerCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e198b-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="e198b-114">Método</span><span class="sxs-lookup"><span data-stu-id="e198b-114">Method</span></span>                                     | <span data-ttu-id="e198b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e198b-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e198b-116">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="e198b-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="e198b-117">Limpa todos os gatilhos da coleção.</span><span class="sxs-lookup"><span data-stu-id="e198b-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="e198b-118">**Criar**</span><span class="sxs-lookup"><span data-stu-id="e198b-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="e198b-119">Cria um novo gatilho para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e198b-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="e198b-120">**Remover**</span><span class="sxs-lookup"><span data-stu-id="e198b-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="e198b-121">Remove o gatilho especificado da coleção de gatilhos usados pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="e198b-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e198b-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e198b-122">Properties</span></span>

<span data-ttu-id="e198b-123">O objeto **TriggerCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e198b-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="e198b-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e198b-124">Property</span></span>                                            | <span data-ttu-id="e198b-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="e198b-125">Access type</span></span>          | <span data-ttu-id="e198b-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="e198b-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="e198b-127">**Contar**</span><span class="sxs-lookup"><span data-stu-id="e198b-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="e198b-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e198b-128">Read-only</span></span><br/> | <span data-ttu-id="e198b-129">Obtém o número de gatilhos na coleção.</span><span class="sxs-lookup"><span data-stu-id="e198b-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="e198b-130">**Item**</span><span class="sxs-lookup"><span data-stu-id="e198b-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="e198b-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e198b-131">Read-only</span></span><br/> | <span data-ttu-id="e198b-132">Obtém o gatilho especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="e198b-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e198b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e198b-133">Remarks</span></span>

<span data-ttu-id="e198b-134">Ao ler ou gravar XML para uma tarefa, os gatilhos para a tarefa são especificados no elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e198b-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e198b-135">Para obter informações sobre cada tipo de gatilho, consulte [tipos de gatilho](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="e198b-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e198b-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e198b-136">Examples</span></span>

<span data-ttu-id="e198b-137">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="e198b-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e198b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e198b-138">Requirements</span></span>



| <span data-ttu-id="e198b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e198b-139">Requirement</span></span> | <span data-ttu-id="e198b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e198b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e198b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e198b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e198b-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e198b-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e198b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e198b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e198b-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e198b-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e198b-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e198b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e198b-146"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="e198b-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="e198b-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e198b-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="e198b-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e198b-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="e198b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e198b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e198b-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e198b-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="e198b-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="e198b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e198b-152">**Of**</span><span class="sxs-lookup"><span data-stu-id="e198b-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





