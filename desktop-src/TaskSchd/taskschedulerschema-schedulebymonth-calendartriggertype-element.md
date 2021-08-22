---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Especifica uma agenda mensal.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Elemento ScheduleByMonth Agendador de Tarefas
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a03fcc3b30e4fe684926baaba2815132c9f2f06bf4373b4e9fbbc181e187bf6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513806"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Elemento ScheduleByMonth (calendarTriggerType)

Especifica uma agenda mensal. Por exemplo, a tarefa começa às 8h em dias específicos do mês em meses específicos.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

O **elemento ScheduleByMonth** é definido pelo tipo complexo [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                  | Type                                                                       | Descrição                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica os dias do mês durante os quais a tarefa é executado.<br/>  |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Especifica os meses do ano durante os quais a tarefa é executado.<br/> |



## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pelo [**elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Para desenvolvimento de script, um gatilho mensal é especificado usando o [**objeto MonthlyTrigger.**](monthlytrigger.md)

Para o desenvolvimento em C++, um gatilho mensal é especificado usando a interface [**IMonthlyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)

Os elementos filho listados abaixo são definidos pelos tipos de elemento complexo [**monthlyScheduleType.**](taskschedulerschema-monthlyscheduletype-complextype.md)

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário mensal que inicia uma tarefa ( às 8h) no 1º e no 15º dia de cada mês do ano.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
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

 

 





