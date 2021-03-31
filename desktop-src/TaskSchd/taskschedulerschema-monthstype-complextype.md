---
title: Tipo complexo monthtype
description: Define os elementos filho e as informações de sequenciamento dos elementos months (monthlyDayOfWeekScheduleType) e months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- tipo complexo monthtype Agendador de Tarefas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644384"
---
# <a name="monthstype-complex-type"></a>Tipo complexo monthtype

Define os elementos filho e as informações de sequenciamento dos elementos [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) e [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .

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
| [**Amanda**](taskschedulerschema-april-monthstype-element.md)         | N/D  | Especifica que a tarefa é executada em abril. <br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       | N/D  | Especifica que a tarefa é executada em agosto. <br/>    |
| [**Dezembro**](taskschedulerschema-december-monthstype-element.md)   | N/D  | Especifica que a tarefa é executada em dezembro. <br/>  |
| [**Fevereiro**](taskschedulerschema-february-monthstype-element.md)   | N/D  | Especifica que a tarefa é executada em fevereiro. <br/>  |
| [**Janeiro**](taskschedulerschema-january-monthstype-element.md)     | N/D  | Especifica que a tarefa é executada em Janeiro. <br/>   |
| [**Julho**](taskschedulerschema-july-monthstype-element.md)           | N/D  | Especifica que a tarefa é executada em julho. <br/>      |
| [**Junho**](taskschedulerschema-june-monthstype-element.md)           | N/D  | Especifica que a tarefa é executada em junho. <br/>      |
| [**Março**](taskschedulerschema-march-monthstype-element.md)         | N/D  | Especifica que a tarefa é executada em março. <br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             | N/D  | Especifica que a tarefa é executada em maio. <br/>       |
| [**Novembro**](taskschedulerschema-november-monthstype-element.md)   | N/D  | Especifica que a tarefa é executada em novembro. <br/>  |
| [**Outubro**](taskschedulerschema-october-monthstype-element.md)     | N/D  | Especifica que a tarefa é executada em outubro. <br/>   |
| [**Setembro**](taskschedulerschema-september-monthstype-element.md) | N/D  | Especifica que a tarefa é executada em setembro. <br/> |



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

 

 





