---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Especifica os dias do mês durante os quais a tarefa é executada.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Agendador de Tarefas do elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760141"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>Elemento DaysOfMonth (monthlyScheduleType)

Especifica os dias do mês durante os quais a tarefa é executada.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

O elemento **DaysOfMonth** é definido pelo tipo complexo [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                    | Derivado de                                                                                         | Descrição                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho para uma agenda mensal de dia da semana.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                        | Type                                                                    | Descrição                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Dia**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Especifica um dia do mês durante o qual a tarefa é executada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, os dias do mês para o agendamento são especificados usando a propriedade [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .

Para o desenvolvimento em C++, os dias do mês para o agendamento são especificados usando a propriedade [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .

O elemento filho deve ser repetido para cada dia do mês em que a tarefa será executada.

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário mensal que inicia uma tarefa (às 8:30 AM) no primeiro dia de cada mês.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





