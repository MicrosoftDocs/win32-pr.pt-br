---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Especifica o intervalo entre as semanas na agenda.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Elemento WeeksInterval Agendador de Tarefas
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c59e4f4b163e5e96418c84bf2925e45cf3a54da1bbb50e17ad9282409438ff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059754"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>Elemento WeeksInterval (weeklyScheduleType)

Especifica o intervalo entre as semanas na agenda.

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo [**weeklyScheduleType.**](taskschedulerschema-weeklyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                                     | Descrição                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Especifica uma agenda semanal.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o intervalo semanal é especificado usando a [**propriedade WeeklyTrigger.WeeksInterval.**](weeklytrigger-weeksinterval.md)

Para o desenvolvimento em C++, o intervalo semanal é especificado usando a [**propriedade IWeeklyTrigger::WeeksInterval.**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval)

## <a name="examples"></a>Exemplos

O XML a seguir define um gatilho de calendário semanal que inicia uma tarefa de segunda a sexta-feira ( às 8h) toda semana.


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

 

 





