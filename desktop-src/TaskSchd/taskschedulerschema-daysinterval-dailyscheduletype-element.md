---
title: Elemento DaysInterval (dailyScheduleType)
description: Especifica o intervalo entre os dias no agendamento.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Agendador de Tarefas do elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918092"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Elemento DaysInterval (dailyScheduleType)

Especifica o intervalo entre os dias no agendamento.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                | Derivado de                                                                   | Descrição                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Especifica um agendamento diário.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, o intervalo de dias para um gatilho diário é especificado pela propriedade [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .

Para desenvolvimento em C++, o intervalo de dias para um gatilho diário é especificado pela propriedade [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .

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

 

 





