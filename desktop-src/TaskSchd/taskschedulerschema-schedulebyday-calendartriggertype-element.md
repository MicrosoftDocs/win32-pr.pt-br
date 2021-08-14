---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica uma agenda diária.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- gatilho diário Agendador de Tarefas elemento , XML
- Elemento ScheduleByDay Agendador de Tarefas
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f29cc4b702ba93aec44e3460279976f50c5563463accfb58b920ad79b757126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131578"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Elemento ScheduleByDay (calendarTriggerType)

Especifica uma agenda diária. Por exemplo, a tarefa começa às 8h todos os dias, todos os dias, a cada três dias e assim por diante.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

O **elemento ScheduleByDay** é definido pelo tipo complexo [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                             | Derivado de                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type             | Descrição                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Especifica o intervalo entre os dias na agenda.<br/> |



## <a name="remarks"></a>Comentários

O elemento filho listado anteriormente é definido pelos tipos de elemento complexo [**dailyScheduleType.**](taskschedulerschema-dailyscheduletype-complextype.md)

A hora do dia em que a tarefa é iniciada é definida pelo [**elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Para o desenvolvimento de scripts, um gatilho diário é especificado usando o [**objeto DailyTrigger.**](weeklytrigger.md)

Para o desenvolvimento em C++, um gatilho diário é especificado usando a interface [**IDailyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)

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



Para ver um exemplo completo do XML para uma tarefa que especifica uma agenda diária, consulte Exemplo de gatilho diário [(XML)](daily-trigger-example--xml-.md).

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

 

 





