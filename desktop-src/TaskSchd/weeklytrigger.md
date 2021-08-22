---
title: Objeto WeeklyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento semanal.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- gatilho semanal Agendador de Tarefas , objeto
- Objeto WeeklyTrigger Agendador de Tarefas
- Objeto WeeklyTrigger Agendador de Tarefas , descrito
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
ms.openlocfilehash: 51eb48b03efb49bd5642909af4b99b99bfb1f7f139b97f8410e0d5f014843ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001784"
---
# <a name="weeklytrigger-object"></a>Objeto WeeklyTrigger

Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento semanal. Por exemplo, a tarefa começa às 8h em um dia específico da semana toda semana ou a cada outra semana.

## <a name="members"></a>Membros

O **objeto WeeklyTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto WeeklyTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Leitura/gravação<br/> | Obtém ou define os dias da semana em que a tarefa é executado.<br/>                                                                                                                        |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a quantidade máxima de tempo que a tarefa lançada pelo gatilho tem permissão para ser executado.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a frequência com que a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**objeto Trigger.**](trigger.md) Obtém o tipo do gatilho.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Leitura/gravação<br/> | Obtém ou define o intervalo entre as semanas na agenda.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pela [**propriedade StartBoundary.**](trigger-startboundary.md)

Ao ler ou escrever seu próprio XML para uma tarefa, um gatilho semanal é especificado usando o [**elemento ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) do esquema Agendador de Tarefas dados.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [Exemplo de gatilho semanal (Scripts).](weekly-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gatilho**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





