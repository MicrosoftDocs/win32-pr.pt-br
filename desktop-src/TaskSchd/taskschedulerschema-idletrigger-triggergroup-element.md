---
title: Elemento IdleTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- gatilho de ociosidade, elemento XML
- Agendador de Tarefas do elemento IdleTrigger
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009042"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="0bf20-105">Elemento IdleTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="0bf20-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="0bf20-106">Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="0bf20-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="0bf20-107">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="0bf20-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="0bf20-108">O elemento **IdleTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf20-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="0bf20-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0bf20-109">Parent element</span></span>



| <span data-ttu-id="0bf20-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bf20-110">Element</span></span>                                                           | <span data-ttu-id="0bf20-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="0bf20-111">Derived from</span></span>                                                         | <span data-ttu-id="0bf20-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bf20-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0bf20-113">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="0bf20-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="0bf20-114">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="0bf20-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="0bf20-115">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0bf20-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0bf20-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0bf20-116">Child elements</span></span>



| <span data-ttu-id="0bf20-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bf20-117">Element</span></span>                                                                                                        | <span data-ttu-id="0bf20-118">Type</span><span class="sxs-lookup"><span data-stu-id="0bf20-118">Type</span></span>                                                                     | <span data-ttu-id="0bf20-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bf20-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bf20-120">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="0bf20-121">booleano</span><span class="sxs-lookup"><span data-stu-id="0bf20-121">boolean</span></span>                                                                  | <span data-ttu-id="0bf20-122">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0bf20-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0bf20-123">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="0bf20-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="0bf20-124">dateTime</span></span>                                                                 | <span data-ttu-id="0bf20-125">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="0bf20-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0bf20-126">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="0bf20-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="0bf20-127">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="0bf20-128">duration</span><span class="sxs-lookup"><span data-stu-id="0bf20-128">duration</span></span>                                                                 | <span data-ttu-id="0bf20-129">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="0bf20-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="0bf20-130">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="0bf20-131">**repetição**</span><span class="sxs-lookup"><span data-stu-id="0bf20-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="0bf20-132">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="0bf20-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="0bf20-133">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="0bf20-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="0bf20-134">dateTime</span></span>                                                                 | <span data-ttu-id="0bf20-135">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="0bf20-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="0bf20-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="0bf20-136">Attributes</span></span>



| <span data-ttu-id="0bf20-137">Nome</span><span class="sxs-lookup"><span data-stu-id="0bf20-137">Name</span></span> | <span data-ttu-id="0bf20-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="0bf20-138">Type</span></span>   | <span data-ttu-id="0bf20-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bf20-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="0bf20-140">ID</span><span class="sxs-lookup"><span data-stu-id="0bf20-140">Id</span></span>   | <span data-ttu-id="0bf20-141">string</span><span class="sxs-lookup"><span data-stu-id="0bf20-141">string</span></span> | <span data-ttu-id="0bf20-142">O identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="0bf20-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0bf20-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bf20-143">Remarks</span></span>

<span data-ttu-id="0bf20-144">Para o desenvolvimento de scripts, um gatilho de ociosidade é especificado usando o objeto [**IdleTrigger**](idletrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf20-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="0bf20-145">Para desenvolvimento em C++, um gatilho de ociosidade é especificado usando a interface [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .</span><span class="sxs-lookup"><span data-stu-id="0bf20-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="0bf20-146">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf20-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="0bf20-147">Esses elementos devem ser adicionados na sequência mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="0bf20-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="0bf20-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="0bf20-149">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="0bf20-150">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="0bf20-151">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="0bf20-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0bf20-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="0bf20-153">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bf20-153">Examples</span></span>

<span data-ttu-id="0bf20-154">O XML a seguir define um gatilho ocioso.</span><span class="sxs-lookup"><span data-stu-id="0bf20-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="0bf20-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bf20-155">Requirements</span></span>



| <span data-ttu-id="0bf20-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bf20-156">Requirement</span></span> | <span data-ttu-id="0bf20-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0bf20-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0bf20-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bf20-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf20-159">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0bf20-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0bf20-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bf20-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf20-161">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0bf20-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0bf20-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bf20-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf20-163">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0bf20-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0bf20-164">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0bf20-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

