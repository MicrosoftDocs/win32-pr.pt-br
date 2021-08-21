---
title: Propriedade Trigger.Type
description: Para scripts, obtém o tipo do gatilho.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Tipo de propriedade Agendador de Tarefas
- Propriedade type Agendador de Tarefas , objeto Trigger
- Disparar objeto Agendador de Tarefas propriedade , Tipo
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc44e385324d161ca051b4270096e674adbba878448667ef176a9c1c63bb24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002034"
---
# <a name="triggertype-property"></a>Propriedade Trigger.Type

Para scripts, obtém o tipo do gatilho. O tipo de gatilho é definido quando o gatilho é criado e não pode ser alterado posteriormente. Para obter informações sobre como criar um gatilho, consulte [**TriggerCollection.Create**](triggercollection-create.md).

## <a name="syntax"></a>Syntax


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valor da propriedade

Um dos seguintes valores [**de enumeração TASK \_ TRIGGER \_ TYPE2.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)



| Valor                                                                                                                                                                                                                                                                                | Significado                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**TAREFA \_ EVENTO \_ DE GATILHO**</dt> <dt>0</dt> </dl>                                                 | Inicia a tarefa quando ocorre um evento específico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**TAREFA \_ HORA \_ DO GATILHO**</dt> <dt>1</dt> </dl>                                                    | Inicia a tarefa em uma hora específica do dia.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**TAREFA \_ DISPARAR \_ DIARIAMENTE**</dt> <dt>2</dt> </dl>                                                 | Inicia a tarefa diariamente.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**TAREFA \_ DISPARAR \_ SEMANAL**</dt> <dt>3</dt> </dl>                                              | Inicia a tarefa semanalmente.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**TAREFA \_ DISPARAR \_ MENSALMENTE**</dt> <dt>4</dt> </dl>                                           | Inicia a tarefa mensalmente.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**TAREFA \_ DISPARAR \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Inicia a tarefa todos os meses em um dia específico da semana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**TAREFA \_ GATILHO \_ OCIOSO**</dt> <dt>6</dt> </dl>                                                    | Inicia a tarefa quando o computador entra em um estado ocioso.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**TAREFA \_ REGISTRO \_ DE GATILHO**</dt> <dt>7</dt> </dl>                            | Inicia a tarefa quando a tarefa é registrada.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**TAREFA \_ INICIALIZAÇÃO \_ DE GATILHO**</dt> <dt>8</dt> </dl>                                                    | Inicia a tarefa quando o computador é inicializado.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**TAREFA \_ LOGON \_ DO GATILHO**</dt> <dt>9</dt> </dl>                                                 | Inicia a tarefa quando um usuário específico faz login.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**TAREFA \_ DISPARAR \_ ALTERAÇÃO DE ESTADO DE \_ \_ SESSÃO**</dt> <dt>11</dt> </dl> | Dispara a tarefa quando um estado de sessão específico muda.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> <dt>

[**TIPO \_ DE GATILHO DE \_ TAREFA2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





