---
title: Tipo complexo weeklyScheduleType
description: Define os elementos filho e as informações de sequenciamento para o elemento ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- Agendador de Tarefas tipo complexo weeklyScheduleType
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f886b2901a5cf1ff1c9db0c8ec761a796b8e68a0f3bdc746afa13a9d8e32ee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099776"
---
# <a name="weeklyscheduletype-complex-type"></a>Tipo complexo weeklyScheduleType

Define os elementos filho e as informações de sequenciamento para o elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
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
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Type                                                                     | Descrição                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executada.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | Especifica o intervalo entre as semanas no agendamento.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





