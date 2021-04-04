---
title: Objeto WeeklyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda semanal.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- gatilho semanal Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto WeeklyTrigger
- Agendador de Tarefas de objeto WeeklyTrigger, descrito
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645237"
---
# <a name="weeklytrigger-object"></a>Objeto WeeklyTrigger

Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda semanal. Por exemplo, a tarefa começa às 8:00. em um dia específico da semana a cada semana ou a cada semana.

## <a name="members"></a>Membros

O objeto **WeeklyTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **WeeklyTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Leitura/gravação<br/> | Obtém ou define os dias da semana em que a tarefa é executada.<br/>                                                                                                                        |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                           |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Leitura/gravação<br/> | Obtém ou define o intervalo entre as semanas no agendamento.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .

Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho semanal é especificado usando o elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho semanal (script)](weekly-trigger-example--scripting-.md).

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

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





