---
title: Elemento Friday (daysOfWeekType)
description: Especifica que a tarefa é executado na sexta-feira.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Elemento Friday Agendador de Tarefas
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 587bfec264065ad3287cb9e37c4705b8e45df0d4dce1aa858e97dc7ecfe5bb5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991236"
---
# <a name="friday-daysofweektype-element"></a>Elemento Friday (daysOfWeekType)

Especifica que a tarefa é executado na sexta-feira.

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

O **elemento Friday** é definido pelo tipo complexo [**daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                  | Derivado de                                                             | Descrição                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado para uma agenda mensal do dia da semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executado para uma agenda semanal.<br/>              |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de dia da semana que inicia uma tarefa na sexta-feira.


```XML
<DaysOfWeek>
    <Friday/>
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

 

 





