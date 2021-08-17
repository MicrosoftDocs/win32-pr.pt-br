---
title: Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
description: Especifica os dias da semana em que a tarefa é executado. | Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: c7ed2a597c1b92245a34dae510c079a5b5aa7a4e7893a78dbb70d7bc5988d580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357128"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)

Especifica os dias da semana em que a tarefa é executado.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

O **elemento DaysOfWeek** é definido pelo [**tipo complexo monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                      | Derivado de                                                                                         | Descrição                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho para uma agenda mensal do dia da semana.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Type | Descrição                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Friday**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Especifica que a tarefa é executado na sexta-feira.<br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Especifica que a tarefa é executado na segunda-feira.<br/>    |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Especifica que a tarefa é executado no sábado.<br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Especifica que a tarefa é executado no domingo.<br/>    |
| [**Quinta-feira**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Especifica que a tarefa é executado na quinta-feira.<br/>  |
| [**Terça-feira**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Especifica que a tarefa é executado na terça-feira.<br/>   |
| [**Quarta-feira**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Especifica que a tarefa é executado na quarta-feira.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, os dias da semana para um calendário mensal do dia da semana são especificados usando a [**propriedade MonthlyDOWTrigger.DaysOfWeek.**](monthlydowtrigger-daysofweek.md)

Para desenvolvimento em C++, os dias da semana para um calendário mensal do dia da semana são especificados usando a propriedade [**IMonthlyDOWTrigger::D aysOfWeek.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek)

Os elementos filho acima são definidos pelo tipo complexo [**daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="examples"></a>Exemplos

O XML a seguir define um calendário mensal do dia da semana que inicia a tarefa na segunda-feira da primeira semana para cada mês do ano.


```XML
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

 

 





