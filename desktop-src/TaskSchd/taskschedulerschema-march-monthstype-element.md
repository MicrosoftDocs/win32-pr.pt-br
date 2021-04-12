---
title: Elemento de março (monthtype)
description: Especifica que a tarefa é executada em março.
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- Elemento de março Agendador de Tarefas
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf6792cf65ab3aecb74bff82282daa0d8fb2bdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295836"
---
# <a name="march-monthstype-element"></a>Elemento de março (monthtype)

Especifica que a tarefa é executada em março.

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

O elemento **março** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.<br/>             |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em março.


```XML
<Months>
    <March/>
</Months>
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

 

 





