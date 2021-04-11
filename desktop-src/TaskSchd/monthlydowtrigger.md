---
title: Objeto MonthlyDOWTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa em uma agenda mensal de dia da semana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Agendador de Tarefas do gatilho de DOW mensal, objeto
- Agendador de Tarefas de objeto MonthlyDOWTrigger
- Agendador de Tarefas de objeto MonthlyDOWTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009158"
---
# <a name="monthlydowtrigger-object"></a>Objeto MonthlyDOWTrigger

Objeto de script que representa um gatilho que inicia uma tarefa em uma agenda mensal de dia da semana. Por exemplo, a tarefa começa em todas as primeiras quintas-feiras, pode até outubro.

## <a name="members"></a>Membros

O objeto **MonthlyDOWTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **MonthlyDOWTrigger** tem essas propriedades.



| Propriedade                                                                          | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define os dias da semana durante os quais a tarefa é executada.<br/>                                                                                                                    |
| [**habilitado**](trigger-enabled.md)<br/>                                     | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                |
| [Limite de fim](trigger-endboundary.md)<br/>                                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada por esse gatilho tem permissão para ser executada.<br/>                          |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define os meses do ano durante os quais a tarefa é executada.<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa é executada na última semana do mês.<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define as semanas do mês em que a tarefa é executada.<br/>                                                                                                                  |



 

## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .

Ao ler ou gravar XML para uma tarefa, um gatilho mensal de dia da semana é especificado usando o elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





