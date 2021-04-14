---
title: Mês (monthlyDayOfWeekScheduleType) elemento
description: Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Agendador de Tarefas do elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369398"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Mês (monthlyDayOfWeekScheduleType) elemento

Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

O elemento **months** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                            | Derivado de                                                                                         | Descrição                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica um gatilho que inicia um trabalho para uma agenda mensal de dia da semana.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type | Descrição                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Amanda**](taskschedulerschema-april-monthstype-element.md)         |      | Especifica que a tarefa é executada em abril.<br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       |      | Especifica que a tarefa é executada em agosto.<br/>    |
| [**Dezembro**](taskschedulerschema-december-monthstype-element.md)   |      | Especifica que a tarefa é executada em dezembro.<br/>  |
| [**Fevereiro**](taskschedulerschema-february-monthstype-element.md)   |      | Especifica que a tarefa é executada em fevereiro.<br/>  |
| [**Janeiro**](taskschedulerschema-january-monthstype-element.md)     |      | Especifica que a tarefa é executada em Janeiro.<br/>   |
| [**Julho**](taskschedulerschema-july-monthstype-element.md)           |      | Especifica que a tarefa é executada em julho.<br/>      |
| [**Junho**](taskschedulerschema-june-monthstype-element.md)           |      | Especifica que a tarefa é executada em junho.<br/>      |
| [**Março**](taskschedulerschema-march-monthstype-element.md)         |      | Especifica que a tarefa é executada em março.<br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             |      | Especifica que a tarefa é executada em maio.<br/>       |
| [**Novembro**](taskschedulerschema-november-monthstype-element.md)   |      | Especifica que a tarefa é executada em novembro.<br/>  |
| [**Outubro**](taskschedulerschema-october-monthstype-element.md)     |      | Especifica que a tarefa é executada em outubro.<br/>   |
| [**Setembro**](taskschedulerschema-september-monthstype-element.md) |      | Especifica que a tarefa é executada em setembro.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, os meses de um ano para uma agenda mensal de dia da semana são especificados usando a propriedade [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .

Para o desenvolvimento em C++, os meses de um ano para uma agenda mensal de dia da semana são especificados usando a propriedade [**IMonthlyDOWTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .

Os elementos filho acima são definidos pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .

## <a name="examples"></a>Exemplos

O XML a seguir define um calendário mensal de dia da semana que inicia a tarefa na segunda-feira da primeira semana para cada mês do ano.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





