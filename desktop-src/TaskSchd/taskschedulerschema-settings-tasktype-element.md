---
title: Configurações elemento (taskType)
description: Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Configurações elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea754aa883f9c80c4a436357cc159c588bde375aaa66a229b358723b74b9e070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002234"
---
# <a name="settings-tasktype-element"></a>Configurações elemento (taskType)

Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

O **Configurações** elemento é definido pelo [**tipo complexo taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**Tasktype**](taskschedulerschema-tasktype-complextype.md) | Especifica a tarefa executada pelo serviço Agendador de Tarefas serviço.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                          | Type                                                                                              | Descrição                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | booleano                                                                                           | Especifica que a tarefa pode ser encerrada usando TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | booleano                                                                                           | Especifica que a tarefa pode ser iniciada usando o comando Executar ou o menu Contexto.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | booleano                                                                                           | Especifica que a tarefa não será iniciada se o computador estiver em execução em baterias.<br/>                      |
| [**habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                              | booleano                                                                                           | Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração é True.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Tempo permitido para concluir a tarefa.<br/>                                                              |
| [**Escondidos**](taskschedulerschema-hidden-settingstype-element.md)                                                | booleano                                                                                           | Especifica que a tarefa não ficará visível na interface do usuário por padrão.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica como o Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Especifica como o Agendador de Tarefas executa tarefas durante a manutenção automática.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica o nível de prioridade para a tarefa.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | booleano                                                                                           | Especifica que a tarefa é executado somente quando o computador está em um estado ocioso.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | booleano                                                                                           | Especifica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | booleano                                                                                           | Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | booleano                                                                                           | Especifica que a tarefa será interrompida se o computador estiver passando por baterias.<br/>                          |
| [**Volátil**](taskschedulerschema-volatile-element.md)                                                         | booleano                                                                                           | Especifica se a tarefa é desabilitada automaticamente por Agendador de Tarefas na Windows inicialização.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | booleano                                                                                           | Especifica que Agendador de Tarefas o computador quando for a hora de executar a tarefa.<br/>                     |



## <a name="remarks"></a>Comentários

Você pode selecionar um ou mais dos elementos filho referenciados acima.

Para desenvolvimento em C++, as informações de registro de uma tarefa são especificadas usando a [**propriedade Configurações de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Para o desenvolvimento de scripts, as informações de registro de uma tarefa são especificadas usando a [**propriedade TaskDefinition.Configurações.**](taskdefinition-settings.md)

## <a name="examples"></a>Exemplos

O exemplo de código XML a seguir define um elemento settings que permite um encerramento rígido da tarefa.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Para obter mais informações e um exemplo completo do XML para definir as configurações da tarefa, consulte [Exemplo de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





