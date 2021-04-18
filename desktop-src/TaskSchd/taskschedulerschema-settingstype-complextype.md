---
title: Tipo complexo settingstype
description: Define os elementos filho e as informações de sequenciamento para o elemento Settings (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- tipo complexo settingstype Agendador de Tarefas
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810988"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="1b8c7-104">Tipo complexo settingstype</span><span class="sxs-lookup"><span data-stu-id="1b8c7-104">settingsType Complex Type</span></span>

<span data-ttu-id="1b8c7-105">Define os elementos filho e as informações de sequenciamento para o elemento [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8c7-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1b8c7-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1b8c7-106">Child elements</span></span>



| <span data-ttu-id="1b8c7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b8c7-107">Element</span></span>                                                                                                             | <span data-ttu-id="1b8c7-108">Type</span><span class="sxs-lookup"><span data-stu-id="1b8c7-108">Type</span></span>                                                                                              | <span data-ttu-id="1b8c7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b8c7-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b8c7-110">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="1b8c7-111">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-111">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-112">Especifica se o serviço de Agendador de Tarefas permite o encerramento físico da tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="1b8c7-113">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="1b8c7-114">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-114">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-115">Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="1b8c7-116">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="1b8c7-117">duration</span><span class="sxs-lookup"><span data-stu-id="1b8c7-117">duration</span></span>                                                                                          | <span data-ttu-id="1b8c7-118">Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="1b8c7-119">Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas não excluirá a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1b8c7-120">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="1b8c7-121">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-121">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-122">Especifica que a tarefa não será iniciada se o computador estiver sendo executado com energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="1b8c7-123">**DisallowStartOnRemoteAppSession**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="1b8c7-124">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-124">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-125">Especifica que a tarefa não deve ser iniciada se a tarefa for disparada para ser executada em uma sessão do trilho (integrada localmente) de aplicativos remotos.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="1b8c7-126">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="1b8c7-127">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-127">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-128">Especifica que a tarefa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="1b8c7-129">A tarefa pode ser executada somente quando essa configuração for **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="1b8c7-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="1b8c7-131">duration</span><span class="sxs-lookup"><span data-stu-id="1b8c7-131">duration</span></span>                                                                                          | <span data-ttu-id="1b8c7-132">Especifica a quantidade de tempo permitido para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1b8c7-133">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="1b8c7-134">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-134">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-135">Especifica, por padrão, que a tarefa não estará visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="1b8c7-136">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="1b8c7-137">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="1b8c7-138">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="1b8c7-139">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="1b8c7-140">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="1b8c7-141">Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="1b8c7-142">**NetworkProfileName**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="1b8c7-143">string</span><span class="sxs-lookup"><span data-stu-id="1b8c7-143">string</span></span>                                                                                            | <span data-ttu-id="1b8c7-144">Especifica o nome de um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="1b8c7-145">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="1b8c7-146">O nome é usado para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="1b8c7-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="1b8c7-148">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="1b8c7-149">Especifica as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="1b8c7-150">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="1b8c7-151">**Priority**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="1b8c7-152">**prioritytype**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="1b8c7-153">Especifica o nível de prioridade para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1b8c7-154">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="1b8c7-155">**Restart**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="1b8c7-156">Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se falhar por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="1b8c7-157">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="1b8c7-158">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-158">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-159">Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="1b8c7-160">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="1b8c7-161">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-161">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-162">Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="1b8c7-163">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="1b8c7-164">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-164">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-165">Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="1b8c7-166">**StopIfGoingOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="1b8c7-167">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-167">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-168">Especifica que a tarefa será interrompida se o computador mudar para a energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="1b8c7-169">**UseUnifiedSchedulingEngine**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="1b8c7-170">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-170">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-171">Especifica que a tarefa é executada usando o mecanismo de agendamento unificado.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="1b8c7-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="1b8c7-173">booleano</span><span class="sxs-lookup"><span data-stu-id="1b8c7-173">boolean</span></span>                                                                                           | <span data-ttu-id="1b8c7-174">Especifica que Agendador de Tarefas irá ativar o computador antes de executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="1b8c7-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b8c7-175">Requirements</span></span>



| <span data-ttu-id="1b8c7-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b8c7-176">Requirement</span></span> | <span data-ttu-id="1b8c7-177">Valor</span><span class="sxs-lookup"><span data-stu-id="1b8c7-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b8c7-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b8c7-178">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8c7-179">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b8c7-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b8c7-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b8c7-180">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8c7-181">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b8c7-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b8c7-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b8c7-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8c7-183">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1b8c7-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1b8c7-184">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1b8c7-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





