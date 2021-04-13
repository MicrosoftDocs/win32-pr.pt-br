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
# <a name="settings-tasktype-element"></a>Elemento Settings (taskType)

Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

O elemento **Settings** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Especifica a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                          | Type                                                                                              | Descrição                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | booleano                                                                                           | Especifica que a tarefa pode ser encerrada usando TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | booleano                                                                                           | Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | booleano                                                                                           | Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.<br/>                      |
| [**habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                              | booleano                                                                                           | Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Quantidade de tempo permitido para concluir a tarefa.<br/>                                                              |
| [**Hidden**](taskschedulerschema-hidden-settingstype-element.md)                                                | booleano                                                                                           | Especifica que a tarefa não será visível na interface do usuário por padrão.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica o nível de prioridade para a tarefa.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**Restart**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | booleano                                                                                           | Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | booleano                                                                                           | Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | booleano                                                                                           | Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.<br/>     |
| [**StopIfGoingOnBatteries (settingstype)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | booleano                                                                                           | Especifica que a tarefa será interrompida se o computador estiver indo para baterias.<br/>                          |
| [**Volátil**](taskschedulerschema-volatile-element.md)                                                         | booleano                                                                                           | Especifica se a tarefa é desabilitada automaticamente pelo Agendador de Tarefas na inicialização do Windows.<br/>                     |
| [**WakeToRun (settingstype)**](taskschedulerschema-waketorun-settingstype-element.md)                           | booleano                                                                                           | Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.<br/>                     |



## <a name="remarks"></a>Comentários

Você pode selecionar um ou mais dos elementos filho mencionados acima.

Para o desenvolvimento em C++, as informações de registro de uma tarefa são especificadas usando a [**propriedade Settings de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Para o desenvolvimento de scripts, as informações de registro de uma tarefa são especificadas usando a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) .

## <a name="examples"></a>Exemplos

O exemplo de código XML a seguir define um elemento Settings que permite um encerramento rígido da tarefa.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Para obter mais informações e um exemplo completo do XML para definir as configurações de tarefa, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





