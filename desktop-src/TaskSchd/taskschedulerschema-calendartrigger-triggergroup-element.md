---
title: Elemento CalendarTrigger (triggerGroup)
description: Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- gatilho de calendário Agendador de Tarefas elemento , XML
- Elemento CalendarTrigger Agendador de Tarefas
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516966"
---
# <a name="calendartrigger-triggergroup-element"></a>Elemento CalendarTrigger (triggerGroup)

Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

O **elemento CalendarTrigger** é definido pelo tipo complexo [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                                            | Type                                                                                                 | Descrição                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | booleano                                                                                              | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                   |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)                             | Especifica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Especifica uma agenda diária.<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Especifica uma agenda mensal.<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho em uma agenda mensal do dia da semana.<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Especifica uma agenda semanal.<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Especifica a data e a hora em que o gatilho é ativado. Este elemento é obrigatório.<br/>                                    |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                               |
|------|------|-------------------------------------------|
| ID   | ID   | O identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

O [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário [**(TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e **CalendarTrigger).**

Os elementos filho listados acima são definidos pelos tipos de elemento complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

Para o desenvolvimento de scripts, os gatilhos de calendário são especificados usando um dos objetos a seguir.

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

Para o desenvolvimento em C++, os gatilhos de calendário são especificados usando uma das interfaces a seguir.

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que especifica um gatilho de calendário, consulte [Exemplo de gatilho diário (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





