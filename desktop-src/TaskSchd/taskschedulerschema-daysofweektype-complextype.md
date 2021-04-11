---
title: Tipo complexo daysOfWeekType
description: Define os elementos filho e as informações de sequenciamento para os elementos DaysOfWeek (weeklyScheduleType) e DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Agendador de Tarefas tipo complexo daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295915"
---
# <a name="daysofweektype-complex-type"></a>Tipo complexo daysOfWeekType

Define os elementos filho e as informações de sequenciamento para os elementos [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) e [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Type | Descrição                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Friday**](taskschedulerschema-friday-daysofweektype-element.md)       | N/D  | A tarefa é executada na sexta-feira. <br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       | N/D  | A tarefa é executada na segunda-feira.<br/>     |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   | N/D  | A tarefa é executada no sábado. <br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       | N/D  | A tarefa é executada no domingo. <br/>    |
| [**Quinta-feira**](taskschedulerschema-thursday-daysofweektype-element.md)   | N/D  | A tarefa é executada na quinta-feira <br/>   |
| [**Terça-feira**](taskschedulerschema-tuesday-daysofweektype-element.md)     | N/D  | A tarefa é executada na terça-feira. <br/>   |
| [**Quarta-feira**](taskschedulerschema-wednesday-daysofweektype-element.md) | N/D  | A tarefa é executada na quarta-feira. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





