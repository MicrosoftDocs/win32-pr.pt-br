---
title: Elemento timetrigger (distrigger)
description: Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Agendador de Tarefas de elemento de gatilho
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455628"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="9a0a8-104">Elemento timetrigger (distrigger)</span><span class="sxs-lookup"><span data-stu-id="9a0a8-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="9a0a8-105">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="9a0a8-106">O elemento **timetrigger** é definido pelo [**disparador.**](taskschedulerschema-triggergroup-group.md)</span><span class="sxs-lookup"><span data-stu-id="9a0a8-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="9a0a8-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9a0a8-107">Parent element</span></span>



| <span data-ttu-id="9a0a8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9a0a8-108">Element</span></span>                                                           | <span data-ttu-id="9a0a8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9a0a8-109">Derived from</span></span>                                                         | <span data-ttu-id="9a0a8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a0a8-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="9a0a8-111">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="9a0a8-112">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="9a0a8-113">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="9a0a8-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9a0a8-114">Child elements</span></span>



| <span data-ttu-id="9a0a8-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="9a0a8-115">Element</span></span>                                                                                                        | <span data-ttu-id="9a0a8-116">Type</span><span class="sxs-lookup"><span data-stu-id="9a0a8-116">Type</span></span>                                                                     | <span data-ttu-id="9a0a8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a0a8-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a0a8-118">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="9a0a8-119">booleano</span><span class="sxs-lookup"><span data-stu-id="9a0a8-119">boolean</span></span>                                                                  | <span data-ttu-id="9a0a8-120">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="9a0a8-121">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="9a0a8-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="9a0a8-122">dateTime</span></span>                                                                 | <span data-ttu-id="9a0a8-123">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="9a0a8-124">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="9a0a8-125">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="9a0a8-126">duration</span><span class="sxs-lookup"><span data-stu-id="9a0a8-126">duration</span></span>                                                                 | <span data-ttu-id="9a0a8-127">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="9a0a8-128">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="9a0a8-129">**repetição**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="9a0a8-130">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="9a0a8-131">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="9a0a8-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="9a0a8-132">dateTime</span></span>                                                                 | <span data-ttu-id="9a0a8-133">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="9a0a8-134">Este elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="9a0a8-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a0a8-135">Attributes</span></span>



| <span data-ttu-id="9a0a8-136">Nome</span><span class="sxs-lookup"><span data-stu-id="9a0a8-136">Name</span></span> | <span data-ttu-id="9a0a8-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a0a8-137">Type</span></span>       | <span data-ttu-id="9a0a8-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a0a8-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="9a0a8-139">ID</span><span class="sxs-lookup"><span data-stu-id="9a0a8-139">Id</span></span>   | <span data-ttu-id="9a0a8-140">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-140">**string**</span></span> | <span data-ttu-id="9a0a8-141">O identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9a0a8-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a0a8-142">Remarks</span></span>

<span data-ttu-id="9a0a8-143">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário (**timetrigger** e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="9a0a8-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="9a0a8-144">Para o desenvolvimento de scripts, um gatilho de tempo é especificado usando o objeto [**timetrigger**](timetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9a0a8-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="9a0a8-145">Para desenvolvimento em C++, um gatilho de tempo é especificado usando a interface [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .</span><span class="sxs-lookup"><span data-stu-id="9a0a8-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="9a0a8-146">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9a0a8-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="9a0a8-147">Esses elementos devem ser adicionados na sequência mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="9a0a8-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="9a0a8-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="9a0a8-149">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="9a0a8-150">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="9a0a8-151">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="9a0a8-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="9a0a8-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="9a0a8-153">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a0a8-153">Examples</span></span>

<span data-ttu-id="9a0a8-154">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de tempo, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="9a0a8-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0a8-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0a8-155">Requirements</span></span>



| <span data-ttu-id="9a0a8-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0a8-156">Requirement</span></span> | <span data-ttu-id="9a0a8-157">Valor</span><span class="sxs-lookup"><span data-stu-id="9a0a8-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a0a8-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0a8-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0a8-159">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a0a8-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a0a8-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0a8-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0a8-161">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a0a8-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a0a8-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a0a8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0a8-163">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9a0a8-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





