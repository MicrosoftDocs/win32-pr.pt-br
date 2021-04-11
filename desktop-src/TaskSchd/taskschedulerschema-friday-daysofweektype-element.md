---
title: Elemento sexta (daysOfWeekType)
description: Especifica que a tarefa é executada na sexta-feira.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Elemento de sexta-feira Agendador de Tarefas
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086070"
---
# <a name="friday-daysofweektype-element"></a>Elemento sexta (daysOfWeekType)

Especifica que a tarefa é executada na sexta-feira.

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

O elemento **sexta-feira** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                  | Derivado de                                                             | Descrição                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.<br/>              |



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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





