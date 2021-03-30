---
title: Propriedade Trigger. Type
description: Para scripts, obtém o tipo do gatilho.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Agendador de Tarefas de propriedade de tipo
- Propriedade Type Agendador de Tarefas, objeto Trigger
- Agendador de Tarefas de objeto de gatilho, Propriedade Type
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
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644472"
---
# <a name="triggertype-property"></a>Propriedade Trigger. Type

Para scripts, obtém o tipo do gatilho. O tipo de gatilho é definido quando o gatilho é criado e não pode ser alterado posteriormente. Para obter informações sobre como criar um gatilho, consulte [**Disparecollection. Create**](triggercollection-create.md).

## <a name="syntax"></a>Sintaxe


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valor da propriedade

Uma das tarefas a [**seguir \_ disparam \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) os valores de enumeração TYPE2.



| Valor                                                                                                                                                                                                                                                                                | Significado                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tarefa \_ do \_Evento de gatilho**</dt> <dt>0</dt> </dl>                                                 | Inicia a tarefa quando ocorre um evento específico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tarefa \_ do \_Tempo de gatilho**</dt> <dt>1</dt> </dl>                                                    | Inicia a tarefa em uma hora específica do dia.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tarefa \_ do GATILHO \_ diário**</dt> <dt>2</dt> </dl>                                                 | Inicia a tarefa diariamente.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tarefa \_ do GATILHO \_ semanal**</dt> <dt>3</dt> </dl>                                              | Inicia a tarefa semanalmente.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tarefa \_ do GATILHO \_ mensal**</dt> <dt>4</dt> </dl>                                           | Inicia a tarefa mensalmente.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Inicia a tarefa todos os meses em um dia específico da semana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tarefa \_ do GATILHO \_ ocioso**</dt> <dt>6</dt> </dl>                                                    | Inicia a tarefa quando o computador entra em um estado ocioso.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tarefa \_ do \_Registro de gatilho**</dt> <dt>7</dt> </dl>                            | Inicia a tarefa quando a tarefa é registrada.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ inicialização**</dt> <dt>8</dt> </dl>                                                    | Inicia a tarefa quando o computador é inicializado.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tarefa \_ do \_Logon de gatilho**</dt> <dt>9</dt> </dl>                                                 | Inicia a tarefa quando um usuário específico faz logon.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ \_ \_ alteração de estado de sessão**</dt> <dt>11</dt> </dl> | Dispara a tarefa quando um estado de sessão específico é alterado.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> <dt>

[**Gatilho de tarefa \_ \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





