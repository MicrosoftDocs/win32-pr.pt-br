---
title: Elemento RegistrationTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- gatilho de registro Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761807"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="5cab5-105">Elemento RegistrationTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="5cab5-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="5cab5-106">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="5cab5-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="5cab5-107">O elemento **RegistrationTrigger** é definido pelo tipo complexo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5cab5-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5cab5-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5cab5-108">Parent element</span></span>



| <span data-ttu-id="5cab5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="5cab5-109">Element</span></span>                                                           | <span data-ttu-id="5cab5-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5cab5-110">Derived from</span></span>                                                         | <span data-ttu-id="5cab5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cab5-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5cab5-112">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="5cab5-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="5cab5-113">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="5cab5-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="5cab5-114">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5cab5-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5cab5-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5cab5-115">Child elements</span></span>



| <span data-ttu-id="5cab5-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="5cab5-116">Element</span></span>                                                                                                        | <span data-ttu-id="5cab5-117">Type</span><span class="sxs-lookup"><span data-stu-id="5cab5-117">Type</span></span>                                                                     | <span data-ttu-id="5cab5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cab5-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cab5-119">**Atraso (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="5cab5-120">duration</span><span class="sxs-lookup"><span data-stu-id="5cab5-120">duration</span></span>                                                                 | <span data-ttu-id="5cab5-121">Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="5cab5-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="5cab5-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="5cab5-123">booleano</span><span class="sxs-lookup"><span data-stu-id="5cab5-123">boolean</span></span>                                                                  | <span data-ttu-id="5cab5-124">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5cab5-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="5cab5-125">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="5cab5-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="5cab5-126">dateTime</span></span>                                                                 | <span data-ttu-id="5cab5-127">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="5cab5-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="5cab5-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="5cab5-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="5cab5-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="5cab5-130">duration</span><span class="sxs-lookup"><span data-stu-id="5cab5-130">duration</span></span>                                                                 | <span data-ttu-id="5cab5-131">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="5cab5-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="5cab5-132">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="5cab5-133">**repetição**</span><span class="sxs-lookup"><span data-stu-id="5cab5-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="5cab5-134">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="5cab5-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="5cab5-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="5cab5-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="5cab5-136">dateTime</span></span>                                                                 | <span data-ttu-id="5cab5-137">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="5cab5-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="5cab5-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="5cab5-138">Attributes</span></span>



| <span data-ttu-id="5cab5-139">Nome</span><span class="sxs-lookup"><span data-stu-id="5cab5-139">Name</span></span> | <span data-ttu-id="5cab5-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cab5-140">Type</span></span> | <span data-ttu-id="5cab5-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cab5-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="5cab5-142">ID</span><span class="sxs-lookup"><span data-stu-id="5cab5-142">Id</span></span>   | <span data-ttu-id="5cab5-143">ID</span><span class="sxs-lookup"><span data-stu-id="5cab5-143">ID</span></span>   | <span data-ttu-id="5cab5-144">Identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="5cab5-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5cab5-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cab5-145">Remarks</span></span>

<span data-ttu-id="5cab5-146">Para o desenvolvimento de scripts, um gatilho de registro é especificado usando o objeto [**RegistrationTrigger**](registrationtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5cab5-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="5cab5-147">Para desenvolvimento em C++, um gatilho de registro é especificado usando a interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .</span><span class="sxs-lookup"><span data-stu-id="5cab5-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="5cab5-148">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5cab5-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="5cab5-149">Esses elementos devem ser adicionados na sequência mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="5cab5-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="5cab5-150">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="5cab5-151">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="5cab5-152">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="5cab5-153">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="5cab5-154">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="5cab5-155">**Atraso (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="5cab5-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="5cab5-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5cab5-156">Examples</span></span>

<span data-ttu-id="5cab5-157">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de inicialização, consulte [exemplo de gatilho de registro (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="5cab5-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cab5-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cab5-158">Requirements</span></span>



| <span data-ttu-id="5cab5-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cab5-159">Requirement</span></span> | <span data-ttu-id="5cab5-160">Valor</span><span class="sxs-lookup"><span data-stu-id="5cab5-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cab5-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cab5-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5cab5-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cab5-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cab5-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cab5-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5cab5-164">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cab5-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cab5-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cab5-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cab5-166">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5cab5-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5cab5-167">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5cab5-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





