---
title: Elemento LogonTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- gatilho de logon, elemento XML
- Agendador de Tarefas do elemento LogonTrigger
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294793"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="f2766-105">Elemento LogonTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="f2766-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="f2766-106">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="f2766-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="f2766-107">O elemento **LogonTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="f2766-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f2766-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f2766-108">Parent element</span></span>



| <span data-ttu-id="f2766-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2766-109">Element</span></span>                                                           | <span data-ttu-id="f2766-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f2766-110">Derived from</span></span>                                                         | <span data-ttu-id="f2766-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2766-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f2766-112">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="f2766-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="f2766-113">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="f2766-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="f2766-114">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f2766-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f2766-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f2766-115">Child elements</span></span>



| <span data-ttu-id="f2766-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2766-116">Element</span></span>                                                                                                        | <span data-ttu-id="f2766-117">Type</span><span class="sxs-lookup"><span data-stu-id="f2766-117">Type</span></span>                                                                     | <span data-ttu-id="f2766-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2766-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2766-119">**Atraso (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="f2766-120">duration</span><span class="sxs-lookup"><span data-stu-id="f2766-120">duration</span></span>                                                                 | <span data-ttu-id="f2766-121">Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f2766-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="f2766-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="f2766-123">booleano</span><span class="sxs-lookup"><span data-stu-id="f2766-123">boolean</span></span>                                                                  | <span data-ttu-id="f2766-124">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f2766-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f2766-125">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="f2766-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="f2766-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="f2766-126">dateTime</span></span>                                                                 | <span data-ttu-id="f2766-127">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="f2766-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f2766-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="f2766-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="f2766-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="f2766-130">duration</span><span class="sxs-lookup"><span data-stu-id="f2766-130">duration</span></span>                                                                 | <span data-ttu-id="f2766-131">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="f2766-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="f2766-132">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="f2766-133">**repetição**</span><span class="sxs-lookup"><span data-stu-id="f2766-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f2766-134">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f2766-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="f2766-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="f2766-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="f2766-136">dateTime</span></span>                                                                 | <span data-ttu-id="f2766-137">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="f2766-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="f2766-138">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="f2766-139">string</span><span class="sxs-lookup"><span data-stu-id="f2766-139">string</span></span>                                                                   | <span data-ttu-id="f2766-140">Identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2766-140">Identifier of the user.</span></span> <span data-ttu-id="f2766-141">A tarefa é iniciada quando esse usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="f2766-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="f2766-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2766-142">Remarks</span></span>

<span data-ttu-id="f2766-143">Para o desenvolvimento de scripts, um gatilho de logon é especificado usando o objeto [**LogonTrigger**](logontrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f2766-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="f2766-144">Para desenvolvimento em C++, um gatilho de logon é especificado usando a interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .</span><span class="sxs-lookup"><span data-stu-id="f2766-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="f2766-145">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2766-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="f2766-146">Esses elementos devem ser adicionados na sequência mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="f2766-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="f2766-147">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f2766-148">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="f2766-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f2766-149">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="f2766-150">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="f2766-151">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="f2766-152">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="f2766-153">**Atraso (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f2766-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="f2766-154">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2766-154">Attributes</span></span>

<span data-ttu-id="f2766-155">O atributo listado abaixo é definido pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2766-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="f2766-156">ID: identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f2766-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="f2766-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2766-157">Examples</span></span>

<span data-ttu-id="f2766-158">Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de logon, consulte [exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="f2766-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2766-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2766-159">Requirements</span></span>



| <span data-ttu-id="f2766-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2766-160">Requirement</span></span> | <span data-ttu-id="f2766-161">Valor</span><span class="sxs-lookup"><span data-stu-id="f2766-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2766-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2766-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f2766-163">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2766-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2766-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2766-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f2766-165">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2766-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2766-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2766-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2766-167">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f2766-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





