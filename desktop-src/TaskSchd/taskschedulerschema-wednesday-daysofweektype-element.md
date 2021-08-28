---
title: Elemento Wednesday (daysOfWeekType)
description: Especifica que a tarefa é executado na quarta-feira.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Elemento Wednesday Agendador de Tarefas
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80f26c921a10df8bd62714021345e7cd2bbbcd065940403f82bae3207445f0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002224"
---
# <a name="wednesday-daysofweektype-element"></a>Elemento Wednesday (daysOfWeekType)

Especifica que a tarefa é executado na quarta-feira.

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

O **elemento Wednesday** é definido pelo tipo complexo [**daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                  | Derivado de                                                             | Descrição                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado para uma agenda mensal do dia da semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado para uma agenda semanal.<br/>              |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de dia da semana que inicia uma tarefa na quarta-feira.


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
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

 

 





