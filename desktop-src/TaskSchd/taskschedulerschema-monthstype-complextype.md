---
title: Tipo complexo monthsType
description: Define os elementos filho e informações de sequenciamento para os elementos Months (monthlyDayOfWeekScheduleType) e Months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- tipo complexo monthsType Agendador de Tarefas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0873f07cc76af9fab827c3df98a8f08ef300de93d4ae6b316809ba32aac87ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758742"
---
# <a name="monthstype-complex-type"></a>Tipo complexo monthsType

Define os elementos filho e informações de sequenciamento para os elementos [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) e [**Months (monthlyScheduleType).**](taskschedulerschema-months-monthlyscheduletype-element.md)

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type | Descrição                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**Abril**](taskschedulerschema-april-monthstype-element.md)         | N/D  | Especifica que a tarefa é executado em abril. <br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       | N/D  | Especifica que a tarefa é executado em agosto. <br/>    |
| [**Dezembro**](taskschedulerschema-december-monthstype-element.md)   | N/D  | Especifica que a tarefa é executado em dezembro. <br/>  |
| [**Fevereiro**](taskschedulerschema-february-monthstype-element.md)   | N/D  | Especifica que a tarefa é executado em fevereiro. <br/>  |
| [**Janeiro**](taskschedulerschema-january-monthstype-element.md)     | N/D  | Especifica que a tarefa é executado em janeiro. <br/>   |
| [**Julho**](taskschedulerschema-july-monthstype-element.md)           | N/D  | Especifica que a tarefa é executado em julho. <br/>      |
| [**Junho**](taskschedulerschema-june-monthstype-element.md)           | N/D  | Especifica que a tarefa é executado em junho. <br/>      |
| [**Março**](taskschedulerschema-march-monthstype-element.md)         | N/D  | Especifica que a tarefa é executado em março. <br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             | N/D  | Especifica que a tarefa é executado em maio. <br/>       |
| [**Novembro**](taskschedulerschema-november-monthstype-element.md)   | N/D  | Especifica que a tarefa é executado em novembro. <br/>  |
| [**Outubro**](taskschedulerschema-october-monthstype-element.md)     | N/D  | Especifica que a tarefa é executado em outubro. <br/>   |
| [**Setembro**](taskschedulerschema-september-monthstype-element.md) | N/D  | Especifica que a tarefa é executado em setembro. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





