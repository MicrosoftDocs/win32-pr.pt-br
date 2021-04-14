---
title: Elemento Actions (taskType)
description: Contém as ações executadas pela tarefa.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Elemento Actions (taskType) Agendador de Tarefas
- ações Agendador de Tarefas, XML
- Elemento Actions Agendador de Tarefas
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369399"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="74957-106">Elemento Actions (taskType)</span><span class="sxs-lookup"><span data-stu-id="74957-106">Actions (taskType) Element</span></span>

<span data-ttu-id="74957-107">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="74957-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="74957-108">O elemento **Actions** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="74957-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="74957-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="74957-109">Parent element</span></span>



| <span data-ttu-id="74957-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="74957-110">Element</span></span>                                          | <span data-ttu-id="74957-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="74957-111">Derived from</span></span>                                                 | <span data-ttu-id="74957-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="74957-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="74957-113">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="74957-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="74957-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="74957-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="74957-115">Descreve a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="74957-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="74957-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="74957-116">Child elements</span></span>



| <span data-ttu-id="74957-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="74957-117">Element</span></span>                                                                    | <span data-ttu-id="74957-118">Type</span><span class="sxs-lookup"><span data-stu-id="74957-118">Type</span></span>                                                                       | <span data-ttu-id="74957-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="74957-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="74957-120">**Commanipulador**</span><span class="sxs-lookup"><span data-stu-id="74957-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="74957-121">**comhandletype**</span><span class="sxs-lookup"><span data-stu-id="74957-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="74957-122">Especifica uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="74957-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="74957-123">**Exec**</span><span class="sxs-lookup"><span data-stu-id="74957-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="74957-124">**exectype**</span><span class="sxs-lookup"><span data-stu-id="74957-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="74957-125">Especifica uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="74957-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="74957-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="74957-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="74957-127">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="74957-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="74957-128">Especifica uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="74957-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="74957-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="74957-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="74957-130">**defaultmessagetype**</span><span class="sxs-lookup"><span data-stu-id="74957-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="74957-131">Especifica uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="74957-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="74957-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="74957-132">Attributes</span></span>



| <span data-ttu-id="74957-133">Nome</span><span class="sxs-lookup"><span data-stu-id="74957-133">Name</span></span>    | <span data-ttu-id="74957-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="74957-134">Type</span></span> | <span data-ttu-id="74957-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="74957-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74957-136">Contexto</span><span class="sxs-lookup"><span data-stu-id="74957-136">Context</span></span> |      | <span data-ttu-id="74957-137">Identificador principal do usuário que é o contexto de segurança para as ações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="74957-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74957-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="74957-138">Remarks</span></span>

<span data-ttu-id="74957-139">Os elementos filho listados anteriormente (máximo 32) são definidos pelo grupo de [**ação**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="74957-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="74957-140">Esses elementos podem ser adicionados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="74957-140">These elements can be added in any order.</span></span>

<span data-ttu-id="74957-141">Para o desenvolvimento em C++, as ações de uma tarefa são definidas na interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .</span><span class="sxs-lookup"><span data-stu-id="74957-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="74957-142">Para o desenvolvimento de script, as ações de uma tarefa são definidas no objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="74957-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="74957-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74957-143">Examples</span></span>

<span data-ttu-id="74957-144">Para obter mais informações e um exemplo completo do XML para uma tarefa que contém uma única ação de execução, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="74957-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74957-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74957-145">Requirements</span></span>



| <span data-ttu-id="74957-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="74957-146">Requirement</span></span> | <span data-ttu-id="74957-147">Valor</span><span class="sxs-lookup"><span data-stu-id="74957-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74957-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74957-148">Minimum supported client</span></span><br/> | <span data-ttu-id="74957-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74957-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74957-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74957-150">Minimum supported server</span></span><br/> | <span data-ttu-id="74957-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74957-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74957-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="74957-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74957-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="74957-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="74957-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="74957-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="74957-155">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="74957-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="74957-156">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="74957-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





