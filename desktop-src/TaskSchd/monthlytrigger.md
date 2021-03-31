---
title: Objeto MonthlyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento mensal.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Agendador de Tarefas do gatilho mensal, objeto
- Agendador de Tarefas de objeto MonthlyTrigger
- Agendador de Tarefas de objeto MonthlyTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644745"
---
# <a name="monthlytrigger-object"></a>Objeto MonthlyTrigger

Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento mensal. Por exemplo, a tarefa é iniciada em dias específicos de meses específicos.

## <a name="members"></a>Membros

O objeto **MonthlyTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **MonthlyTrigger** tem essas propriedades.



| Propriedade                                                                     | Tipo de acesso           | Description                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define os dias do mês durante os quais a tarefa é executada.<br/>                                                                                                                   |
| [**habilitado**](trigger-enabled.md)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                |
| [Limite de fim](trigger-endboundary.md)<br/>                            | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                           |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | Leitura/gravação<br/> | Obtém ou define os meses do ano durante os quais a tarefa é executada.<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                          | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que a tarefa é executada no último dia do mês.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Escreva**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .

Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho mensal é especificado usando o elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

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

 

 





