---
title: Elemento Months (monthlyDayOfWeekScheduleType)
description: Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal do dia da semana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Elemento Months Agendador de Tarefas
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a963032a2d33f13158af249f2b867037cf50082be005efa579148031c8e30585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959596"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Elemento Months (monthlyDayOfWeekScheduleType)

Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal do dia da semana.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

O **elemento Months** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                            | Derivado de                                                                                         | Descrição                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho para uma agenda mensal do dia da semana.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type | Descrição                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Abril**](taskschedulerschema-april-monthstype-element.md)         |      | Especifica que a tarefa é executado em abril.<br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       |      | Especifica que a tarefa é executado em agosto.<br/>    |
| [**Dezembro**](taskschedulerschema-december-monthstype-element.md)   |      | Especifica que a tarefa é executado em dezembro.<br/>  |
| [**Fevereiro**](taskschedulerschema-february-monthstype-element.md)   |      | Especifica que a tarefa é executado em fevereiro.<br/>  |
| [**Janeiro**](taskschedulerschema-january-monthstype-element.md)     |      | Especifica que a tarefa é executado em janeiro.<br/>   |
| [**Julho**](taskschedulerschema-july-monthstype-element.md)           |      | Especifica que a tarefa é executado em julho.<br/>      |
| [**Junho**](taskschedulerschema-june-monthstype-element.md)           |      | Especifica que a tarefa é executado em junho.<br/>      |
| [**Março**](taskschedulerschema-march-monthstype-element.md)         |      | Especifica que a tarefa é executado em março.<br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             |      | Especifica que a tarefa é executado em maio.<br/>       |
| [**Novembro**](taskschedulerschema-november-monthstype-element.md)   |      | Especifica que a tarefa é executado em novembro.<br/>  |
| [**Outubro**](taskschedulerschema-october-monthstype-element.md)     |      | Especifica que a tarefa é executado em outubro.<br/>   |
| [**Setembro**](taskschedulerschema-september-monthstype-element.md) |      | Especifica que a tarefa é executado em setembro.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, os meses de um ano para uma agenda mensal do dia da semana são especificados usando a [**propriedade MonthlyDOWTrigger.MonthsOfYear.**](monthlydowtrigger-monthsofyear.md)

Para o desenvolvimento em C++, os meses de um ano para uma agenda mensal do dia da semana são especificados usando a propriedade [**IMonthlyDOWTrigger::MonthsOfYear.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear)

Os elementos filho acima são definidos pelo [**tipo complexo monthsType.**](taskschedulerschema-monthstype-complextype.md)

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

 

 





