---
title: Objeto SessionStateChangeTrigger
description: Objeto de script que dispara tarefas para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Agendador de Tarefas de objeto SessionStateChangeTrigger
- Agendador de Tarefas de objeto SessionStateChangeTrigger, descrito
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769392"
---
# <a name="sessionstatechangetrigger-object"></a>Objeto SessionStateChangeTrigger

Objeto de script que dispara tarefas para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.

## <a name="members"></a>Membros

O objeto **SessionStateChangeTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SessionStateChangeTrigger** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso           | Descrição                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retardo**](sessionstatechangetrigger-delay.md)<br/>             | Leitura/gravação<br/> | Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes que uma tarefa seja iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.<br/>                                         |
| [**habilitado**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                              |
| [**Limite de fim**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                                 |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Leitura/gravação<br/> | Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.<br/>                                                                                                      |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                                            |
| [**ID**](sessionstatechangetrigger-userid.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.<br/>                                                               |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho de alteração de estado de sessão é especificado usando o elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





