---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Especifica uma agenda mensal do dia da semana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Elemento ScheduleByMonthDayOfWeek Agendador de Tarefas
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 185608ea5a8805511de8430c82e6eecabd9cc5b9622fed85d71e26dd39f20cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099876"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)

Especifica uma agenda mensal do dia da semana. Por exemplo, a tarefa começa em dias específicos da semana, semanas do mês e meses do ano.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

O **elemento ScheduleByMonthDayOfWeek** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                   | Type                                                                     | Descrição                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado.<br/>       |
| [**Meses**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Especifica os meses do ano durante os quais a tarefa é executado.<br/> |
| [**Semanas**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Especifica o intervalo entre as semanas na agenda.<br/>    |



## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pelo [**elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Para o desenvolvimento de scripts, um gatilho mensal de dia da semana é especificado usando o [**objeto MonthlyDOWTrigger.**](monthlydowtrigger.md)

Para o desenvolvimento em C++, um gatilho mensal de dia da semana é especificado usando a interface [**IMonthlyDOWTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

Os elementos filho listados acima são definidos pelos tipos de elemento complexo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário mensal de dia da semana que inicia uma tarefa ( às 8h) na segunda-feira da primeira semana de cada mês do ano.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
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

 

 





