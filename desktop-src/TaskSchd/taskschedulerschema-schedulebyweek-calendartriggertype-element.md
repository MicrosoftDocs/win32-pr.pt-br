---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Especifica uma agenda semanal.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- gatilho semanal Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento ScheduleByWeek
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369878"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Elemento ScheduleByWeek (calendarTriggerType)

Especifica uma agenda semanal. Por exemplo, a tarefa começa às 8:00 em um dia específico da semana a cada semana ou em um dia específico da semana a cada semana.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

O elemento **ScheduleByWeek** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Type                                                                     | Descrição                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executada.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Especifica o intervalo entre as semanas no agendamento.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Para o desenvolvimento de scripts, um gatilho semanal é especificado usando o objeto [**WeeklyTrigger**](weeklytrigger.md) .

Para desenvolvimento em C++, um gatilho semanal é especificado usando a interface [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário semanal que inicia uma tarefa de segunda-feira a sexta-feira (às 8:00) todas as semanas.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





