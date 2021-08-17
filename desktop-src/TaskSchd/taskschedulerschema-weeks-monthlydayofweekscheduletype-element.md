---
title: Elemento Weeks (monthlyDayOfWeekScheduleType)
description: Especifica as semanas do mês em que a tarefa é executado.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento Weeks Agendador de Tarefas
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757973"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Elemento Weeks (monthlyDayOfWeekScheduleType)

Especifica as semanas do mês em que a tarefa é executado.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

O **elemento Weeks** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                      | Derivado de                                                                                         | Descrição                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho em uma agenda mensal do dia da semana.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                    | Type                                                        | Descrição                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Semana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Especifica uma semana específica do mês.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, as semanas do mês são especificadas usando a [**propriedade MonthlyDOWTrigger.WeeksOfMonth.**](monthlydowtrigger-weeksofmonth.md)

Para desenvolvimento em C++, as semanas do mês são especificadas usando a propriedade [**IMonthlyDOWTrigger::WeeksOfMonth.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth)

Ao especificar as semanas do mês, use de 1 a 4 para especificar as primeiras quatro semanas do mês ou use a cadeia de caracteres "Last" para indicar a última semana, independentemente de qual é a semana.

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

 

 





