---
title: Elemento Settings (taskType)
description: Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Agendador de Tarefas do elemento Settings
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369465"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="75c3c-104">Elemento Settings (taskType)</span><span class="sxs-lookup"><span data-stu-id="75c3c-104">Settings (taskType) Element</span></span>

<span data-ttu-id="75c3c-105">Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="75c3c-106">O elemento **Settings** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75c3c-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="75c3c-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="75c3c-107">Parent element</span></span>



| <span data-ttu-id="75c3c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="75c3c-108">Element</span></span>                                          | <span data-ttu-id="75c3c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="75c3c-109">Derived from</span></span>                                                 | <span data-ttu-id="75c3c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="75c3c-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="75c3c-111">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="75c3c-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="75c3c-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="75c3c-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="75c3c-113">Especifica a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="75c3c-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="75c3c-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="75c3c-114">Child elements</span></span>



| <span data-ttu-id="75c3c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="75c3c-115">Element</span></span>                                                                                                          | <span data-ttu-id="75c3c-116">Type</span><span class="sxs-lookup"><span data-stu-id="75c3c-116">Type</span></span>                                                                                              | <span data-ttu-id="75c3c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="75c3c-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75c3c-118">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="75c3c-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="75c3c-119">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-119">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-120">Especifica que a tarefa pode ser encerrada usando TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="75c3c-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="75c3c-121">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="75c3c-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="75c3c-122">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-122">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-123">Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="75c3c-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="75c3c-124">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="75c3c-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="75c3c-125">duration</span><span class="sxs-lookup"><span data-stu-id="75c3c-125">duration</span></span>                                                                                          | <span data-ttu-id="75c3c-126">Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.</span><span class="sxs-lookup"><span data-stu-id="75c3c-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="75c3c-127">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="75c3c-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="75c3c-128">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-128">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-129">Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="75c3c-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="75c3c-130">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="75c3c-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="75c3c-131">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-131">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-132">Especifica que a tarefa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="75c3c-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="75c3c-133">A tarefa pode ser executada somente quando essa configuração for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="75c3c-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="75c3c-134">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="75c3c-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="75c3c-135">duration</span><span class="sxs-lookup"><span data-stu-id="75c3c-135">duration</span></span>                                                                                          | <span data-ttu-id="75c3c-136">Quantidade de tempo permitido para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="75c3c-137">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="75c3c-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="75c3c-138">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-138">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-139">Especifica que a tarefa não será visível na interface do usuário por padrão.</span><span class="sxs-lookup"><span data-stu-id="75c3c-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="75c3c-140">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="75c3c-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="75c3c-141">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="75c3c-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="75c3c-142">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="75c3c-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="75c3c-143">**MaintenanceSettings**</span><span class="sxs-lookup"><span data-stu-id="75c3c-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="75c3c-144">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="75c3c-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="75c3c-145">Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="75c3c-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="75c3c-146">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="75c3c-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="75c3c-147">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="75c3c-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="75c3c-148">Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="75c3c-149">**Priority**</span><span class="sxs-lookup"><span data-stu-id="75c3c-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="75c3c-150">**prioritytype**</span><span class="sxs-lookup"><span data-stu-id="75c3c-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="75c3c-151">Especifica o nível de prioridade para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="75c3c-152">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="75c3c-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="75c3c-153">**Restart**</span><span class="sxs-lookup"><span data-stu-id="75c3c-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="75c3c-154">Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="75c3c-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="75c3c-155">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="75c3c-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="75c3c-156">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-156">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-157">Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="75c3c-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="75c3c-158">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="75c3c-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="75c3c-159">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-159">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-160">Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="75c3c-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="75c3c-161">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="75c3c-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="75c3c-162">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-162">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-163">Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.</span><span class="sxs-lookup"><span data-stu-id="75c3c-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="75c3c-164">**StopIfGoingOnBatteries (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="75c3c-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="75c3c-165">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-165">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-166">Especifica que a tarefa será interrompida se o computador estiver indo para baterias.</span><span class="sxs-lookup"><span data-stu-id="75c3c-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="75c3c-167">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="75c3c-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="75c3c-168">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-168">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-169">Especifica se a tarefa é desabilitada automaticamente pelo Agendador de Tarefas na inicialização do Windows.</span><span class="sxs-lookup"><span data-stu-id="75c3c-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="75c3c-170">**WakeToRun (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="75c3c-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="75c3c-171">booleano</span><span class="sxs-lookup"><span data-stu-id="75c3c-171">boolean</span></span>                                                                                           | <span data-ttu-id="75c3c-172">Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="75c3c-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c3c-173">Remarks</span></span>

<span data-ttu-id="75c3c-174">Você pode selecionar um ou mais dos elementos filho mencionados acima.</span><span class="sxs-lookup"><span data-stu-id="75c3c-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="75c3c-175">Para o desenvolvimento em C++, as informações de registro de uma tarefa são especificadas usando a [**propriedade Settings de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span><span class="sxs-lookup"><span data-stu-id="75c3c-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="75c3c-176">Para o desenvolvimento de scripts, as informações de registro de uma tarefa são especificadas usando a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="75c3c-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="75c3c-177">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75c3c-177">Examples</span></span>

<span data-ttu-id="75c3c-178">O exemplo de código XML a seguir define um elemento Settings que permite um encerramento rígido da tarefa.</span><span class="sxs-lookup"><span data-stu-id="75c3c-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="75c3c-179">Para obter mais informações e um exemplo completo do XML para definir as configurações de tarefa, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="75c3c-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75c3c-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c3c-180">Requirements</span></span>



| <span data-ttu-id="75c3c-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c3c-181">Requirement</span></span> | <span data-ttu-id="75c3c-182">Valor</span><span class="sxs-lookup"><span data-stu-id="75c3c-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75c3c-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75c3c-183">Minimum supported client</span></span><br/> | <span data-ttu-id="75c3c-184">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75c3c-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75c3c-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75c3c-185">Minimum supported server</span></span><br/> | <span data-ttu-id="75c3c-186">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75c3c-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75c3c-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="75c3c-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c3c-188">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="75c3c-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="75c3c-189">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="75c3c-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





