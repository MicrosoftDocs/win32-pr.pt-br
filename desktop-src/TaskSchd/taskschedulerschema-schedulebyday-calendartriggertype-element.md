---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica um agendamento diário.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- gatilho diário Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento ScheduleByDay
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918939"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Elemento ScheduleByDay (calendarTriggerType)

Especifica um agendamento diário. Por exemplo, a tarefa começa às 8:00, todos os dias, a cada dia, a cada terceiro dia e assim por diante.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

O elemento **ScheduleByDay** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type             | Descrição                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Especifica o intervalo entre os dias no agendamento.<br/> |



## <a name="remarks"></a>Comentários

O elemento filho listado anteriormente é definido pelos tipos de elementos complexos [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Para o desenvolvimento de scripts, um gatilho diário é especificado usando o objeto [**DailyTrigger**](weeklytrigger.md) .

Para desenvolvimento em C++, um gatilho diário é especificado usando a interface [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário diário que inicia a tarefa todos os dias.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Para obter um exemplo completo do XML para uma tarefa que especifica um agendamento diário, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).

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

 

 





