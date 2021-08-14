---
title: Tipo complexo settingstype
description: define os elementos filho e as informações de sequenciamento para o elemento Configurações (taskType).
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
ms.openlocfilehash: a48a124230a27a0c23cc9c2a9fa983b6ef3088b8ec22e8ac03fc371caadf0f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356348"
---
# <a name="settingstype-complex-type"></a>Tipo complexo settingstype

define os elementos filho e as informações de sequenciamento para o elemento [**Configurações (taskType)**](taskschedulerschema-settings-tasktype-element.md) .

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

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                             | Type                                                                                              | Descrição                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | booleano                                                                                           | Especifica se o serviço de Agendador de Tarefas permite o encerramento físico da tarefa.<br/>                                                                                                                                                                                                                             |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | booleano                                                                                           | Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto. <br/>                                                                                                                                                                                                             |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | duration                                                                                          | Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas não excluirá a tarefa.<br/>                                                                                           |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | booleano                                                                                           | Especifica que a tarefa não será iniciada se o computador estiver sendo executado com energia da bateria.<br/>                                                                                                                                                                                                                 |
| [**DisallowStartOnRemoteAppSession**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | booleano                                                                                           | Especifica que a tarefa não deve ser iniciada se a tarefa for disparada para ser executada em uma sessão do trilho (integrada localmente) de aplicativos remotos.<br/>                                                                                                                                                                     |
| [**habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                                 | booleano                                                                                           | Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for **verdadeira**.<br/>                                                                                                                                                                                                        |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | duration                                                                                          | Especifica a quantidade de tempo permitido para concluir a tarefa.<br/>                                                                                                                                                                                                                                               |
| [**Oculto**](taskschedulerschema-hidden-settingstype-element.md)                                                   | booleano                                                                                           | Especifica, por padrão, que a tarefa não estará visível na interface do usuário.<br/>                                                                                                                                                                                                                     |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/>                                                                                                                                                                                                                   |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa. <br/>                                                                                                                                                                                                     |
| [**NetworkProfileName**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | string                                                                                            | Especifica o nome de um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**. O nome é usado para fins de exibição.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)                | Especifica as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.<br/> |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                               | [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica o nível de prioridade para a tarefa.<br/>                                                                                                                                                                                                                                                               |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**Restart**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se falhar por qualquer motivo. <br/>                                                                                                                                                                                                          |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | booleano                                                                                           | Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.<br/>                                                                                                                                                                                                                               |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | booleano                                                                                           | Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.<br/>                                                                                                                                                                                                                    |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | booleano                                                                                           | Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.<br/>                                                                                                                                                                                                    |
| [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | booleano                                                                                           | Especifica que a tarefa será interrompida se o computador mudar para a energia da bateria. <br/>                                                                                                                                                                                                                      |
| [**UseUnifiedSchedulingEngine**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | booleano                                                                                           | Especifica que a tarefa é executada usando o mecanismo de agendamento unificado.<br/>                                                                                                                                                                                                                                   |
| [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md)                                             | booleano                                                                                           | Especifica que Agendador de Tarefas irá ativar o computador antes de executar a tarefa.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





