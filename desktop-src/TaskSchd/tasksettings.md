---
title: Objeto TaskSettings
description: Um objeto de script que fornece as configurações que o serviço de Agendador de Tarefas usa para executar a tarefa.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Agendador de Tarefas de objeto TaskSettings
- Agendador de Tarefas de objeto TaskSettings, descrito
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7690ba59b4794f952ca3b381fc28247f0dfb4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766955"
---
# <a name="tasksettings-object"></a>Objeto TaskSettings

Um objeto de script que fornece as configurações que o serviço de Agendador de Tarefas usa para executar a tarefa.

## <a name="members"></a>Membros

O objeto **TaskSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **TaskSettings** tem essas propriedades.



| Propriedade                                                                                 | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa pode ser encerrada usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilidade**](tasksettings-compatibility.md)<br/>                           | Leitura/gravação<br/> | Obtém ou define um valor inteiro que indica a qual versão do Agendador de Tarefas uma tarefa é compatível.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Leitura/gravação<br/> | Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado com energia da bateria.<br/>                                                                                                                                                                                                                                                                                        |
| [**habilitado**](tasksettings-enabled.md)<br/>                                       | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define a quantidade de tempo permitido para concluir a tarefa.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Hidden**](tasksettings-hidden.md)<br/>                                         | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa não estará visível na interface do usuário. No entanto, os administradores podem substituir essa configuração por meio do uso de um "comutador mestre" que torna todas as tarefas visíveis na interface do usuário.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define as informações que especificam como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define o objeto de configurações de rede que contém um identificador e nome de perfil de rede. Se a propriedade [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de **TaskSettings** for **true** e um propfile de rede for especificado na propriedade [**NetworkSettings**](tasksettings-networksettings.md) , a tarefa será executada somente se o perfil de rede especificado estiver disponível.<br/> |
| [**Priority**](tasksettings-priority.md)<br/>                                     | Leitura/gravação<br/> | Obtém ou define o nível de prioridade da tarefa.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em um estado ocioso.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa será interrompida se o computador começar a ser executado com energia da bateria.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | Leitura/gravação<br/> | Obtém ou define uma definição formatada em XML das configurações da tarefa.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Por padrão, uma tarefa será interrompida em 72 horas depois de começar a ser executada. Você pode alterar isso alterando a configuração [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md) .

Ao ler ou gravar XML para uma tarefa, as configurações de tarefa são definidas no elemento [**configurações**](taskschedulerschema-settings-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

