---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Especifica uma agenda semanal.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- gatilho semanal Agendador de Tarefas , elemento XML
- Elemento ScheduleByWeek Agendador de Tarefas
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddf37c6261ba28c4cb4f59c47ee8ebd8c09afc4e36c3d1aa218efe8caa81e8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002274"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Elemento ScheduleByWeek (calendarTriggerType)

Especifica uma agenda semanal. Por exemplo, a tarefa começa às 8h em um dia específico da semana toda semana ou em um dia específico da semana a cada outra semana.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

O **elemento ScheduleByWeek** é definido pelo tipo complexo [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Type                                                                     | Descrição                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Especifica o intervalo entre as semanas na agenda.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados acima são definidos pelos tipos [**de elementos complexos weeklyScheduleType.**](taskschedulerschema-weeklyscheduletype-complextype.md)

A hora do dia em que a tarefa é iniciada é definida pelo [**elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Para o desenvolvimento de scripts, um gatilho semanal é especificado usando o [**objeto WeeklyTrigger.**](weeklytrigger.md)

Para o desenvolvimento em C++, um gatilho semanal é especificado usando a interface [**IWeeklyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário semanal que inicia uma tarefa de segunda a sexta-feira (às 8h) toda semana.


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





