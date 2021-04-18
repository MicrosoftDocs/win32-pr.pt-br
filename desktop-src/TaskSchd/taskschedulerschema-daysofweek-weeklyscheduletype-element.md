---
title: Elemento DaysOfWeek (weeklyScheduleType)
description: Especifica os dias da semana em que a tarefa é executada. | Elemento DaysOfWeek (weeklyScheduleType)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- Elemento DaysOfWeek Agendador de Tarefas
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105767731"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>Elemento DaysOfWeek (weeklyScheduleType)

Especifica os dias da semana em que a tarefa é executada.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

O elemento **DaysOfWeek** é definido pelo tipo complexo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                                     | Description                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Especifica uma agenda semanal.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Type | Description                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Friday**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Especifica que a tarefa é executada na sexta-feira.<br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Especifica que a tarefa é executada na segunda-feira.<br/>    |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Especifica que a tarefa é executada no sábado.<br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Especifica que a tarefa é executada no domingo.<br/>    |
| [**Quinta-feira**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Especifica que a tarefa é executada na quinta-feira.<br/>  |
| [**Terça-feira**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Especifica que a tarefa é executada na terça-feira.<br/>   |
| [**Quarta-feira**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Especifica que a tarefa é executada na quarta-feira.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho anteriores são definidos pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

Para o desenvolvimento de scripts, o intervalo semanal é especificado usando a propriedade [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

Para desenvolvimento em C++, o intervalo semanal é especificado usando a propriedade [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário diário que inicia uma tarefa de segunda-feira a sexta-feira (às 8:00) todas as semanas.


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



Para obter um exemplo completo do XML para uma tarefa que usa um gatilho semanal, consulte [exemplo de gatilho semanal (XML)](weekly-trigger-example--xml-.md).

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

 

 





