---
title: Elemento BootTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- gatilho de inicialização Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295838"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="997eb-105">Elemento BootTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="997eb-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="997eb-106">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="997eb-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="997eb-107">O elemento **BootTrigger** é definido pelo tipo complexo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="997eb-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="997eb-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="997eb-108">Parent element</span></span>



| <span data-ttu-id="997eb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="997eb-109">Element</span></span>                                                           | <span data-ttu-id="997eb-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="997eb-110">Derived from</span></span>                                                         | <span data-ttu-id="997eb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="997eb-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="997eb-112">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="997eb-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="997eb-113">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="997eb-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="997eb-114">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="997eb-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="997eb-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="997eb-115">Child elements</span></span>



| <span data-ttu-id="997eb-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="997eb-116">Element</span></span>                                                                                                        | <span data-ttu-id="997eb-117">Type</span><span class="sxs-lookup"><span data-stu-id="997eb-117">Type</span></span>                                                                     | <span data-ttu-id="997eb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="997eb-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="997eb-119">**Atraso (bootTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="997eb-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="997eb-120">duration</span><span class="sxs-lookup"><span data-stu-id="997eb-120">duration</span></span>                                                                 | <span data-ttu-id="997eb-121">Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="997eb-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="997eb-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="997eb-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="997eb-123">booleano</span><span class="sxs-lookup"><span data-stu-id="997eb-123">boolean</span></span>                                                                  | <span data-ttu-id="997eb-124">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="997eb-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="997eb-125">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="997eb-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="997eb-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="997eb-126">dateTime</span></span>                                                                 | <span data-ttu-id="997eb-127">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="997eb-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="997eb-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="997eb-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="997eb-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="997eb-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="997eb-130">duration</span><span class="sxs-lookup"><span data-stu-id="997eb-130">duration</span></span>                                                                 | <span data-ttu-id="997eb-131">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="997eb-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="997eb-132">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="997eb-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="997eb-133">**repetição**</span><span class="sxs-lookup"><span data-stu-id="997eb-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="997eb-134">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="997eb-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="997eb-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="997eb-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="997eb-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="997eb-136">dateTime</span></span>                                                                 | <span data-ttu-id="997eb-137">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="997eb-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="997eb-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="997eb-138">Attributes</span></span>



| <span data-ttu-id="997eb-139">Nome</span><span class="sxs-lookup"><span data-stu-id="997eb-139">Name</span></span> | <span data-ttu-id="997eb-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="997eb-140">Type</span></span>       | <span data-ttu-id="997eb-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="997eb-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="997eb-142">ID</span><span class="sxs-lookup"><span data-stu-id="997eb-142">Id</span></span>   | <span data-ttu-id="997eb-143">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="997eb-143">**string**</span></span> | <span data-ttu-id="997eb-144">O identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="997eb-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="997eb-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="997eb-145">Remarks</span></span>

<span data-ttu-id="997eb-146">Para o desenvolvimento de script, um gatilho de inicialização é definido pelo objeto [**BootTrigger**](boottrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="997eb-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="997eb-147">Para desenvolvimento em C++, um gatilho de inicialização é definido pelo objeto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .</span><span class="sxs-lookup"><span data-stu-id="997eb-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="997eb-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="997eb-148">Examples</span></span>

<span data-ttu-id="997eb-149">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de inicialização, consulte [exemplo de gatilho de inicialização (XML)](boot-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="997eb-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="997eb-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="997eb-150">Requirements</span></span>



| <span data-ttu-id="997eb-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="997eb-151">Requirement</span></span> | <span data-ttu-id="997eb-152">Valor</span><span class="sxs-lookup"><span data-stu-id="997eb-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="997eb-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="997eb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="997eb-154">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="997eb-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="997eb-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="997eb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="997eb-156">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="997eb-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="997eb-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="997eb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997eb-158">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="997eb-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="997eb-159">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="997eb-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





