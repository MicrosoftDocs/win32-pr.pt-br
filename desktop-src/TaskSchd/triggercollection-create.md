---
title: Método TriggerCollection. Create
description: Para scripts, o cria um novo gatilho para a tarefa.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- disparadores Agendador de Tarefas, criando
- Criar Agendador de Tarefas do método
- Método Create Agendador de tarefas, disparador
- Agendador de Tarefas de objeto TriggerCollection, método Create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768557"
---
# <a name="triggercollectioncreate-method"></a>Método TriggerCollection. Create

Para scripts, o cria um novo gatilho para a tarefa.

## <a name="syntax"></a>Sintaxe


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Esse parâmetro é definido como uma das seguintes constantes de enumeração [**\_ \_ TYPE2 de gatilho de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .



| Valor                                                                                                                                                                                                                                                                                | Significado                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tarefa \_ do \_Evento de gatilho**</dt> <dt>0</dt> </dl>                                                 | Dispara a tarefa quando um evento específico ocorre.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tarefa \_ do \_Tempo de gatilho**</dt> <dt>1</dt> </dl>                                                    | Dispara a tarefa em uma hora específica do dia.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tarefa \_ do GATILHO \_ diário**</dt> <dt>2</dt> </dl>                                                 | Dispara a tarefa em um agendamento diário. Por exemplo, a tarefa é iniciada em uma hora específica todos os dias, a cada dia, a cada terceiro dia e assim por diante.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tarefa \_ do GATILHO \_ semanal**</dt> <dt>3</dt> </dl>                                              | Dispara a tarefa em uma agenda semanal. Por exemplo, a tarefa começa às 8:00 em um dia específico toda semana ou outra semana.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tarefa \_ do GATILHO \_ mensal**</dt> <dt>4</dt> </dl>                                           | Dispara a tarefa em um agendamento mensal. Por exemplo, a tarefa é iniciada em dias específicos de meses específicos.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Dispara a tarefa em uma agenda mensal de dia da semana. Por exemplo, a tarefa é iniciada em um período específico da semana, semanas do mês e meses do ano.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tarefa \_ do GATILHO \_ ocioso**</dt> <dt>6</dt> </dl>                                                    | Dispara a tarefa quando o computador entra em um estado ocioso.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tarefa \_ do \_Registro de gatilho**</dt> <dt>7</dt> </dl>                            | Dispara a tarefa quando a tarefa é registrada.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ inicialização**</dt> <dt>8</dt> </dl>                                                    | Dispara a tarefa quando o computador é inicializado.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tarefa \_ do \_Logon de gatilho**</dt> <dt>9</dt> </dl>                                                 | Dispara a tarefa quando um usuário específico faz logon.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tarefa \_ do DISPARAR \_ \_ \_ alteração de estado de sessão**</dt> <dt>11</dt> </dl> | Dispara a tarefa quando um estado de sessão específico é alterado.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto de [**gatilho**](trigger.md) que representa o novo gatilho.

## <a name="remarks"></a>Comentários

Para obter informações sobre cada tipo de gatilho, consulte [tipos de gatilho](trigger-types.md).

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

[**Of**](trigger.md)
</dt> </dl>

 

 





