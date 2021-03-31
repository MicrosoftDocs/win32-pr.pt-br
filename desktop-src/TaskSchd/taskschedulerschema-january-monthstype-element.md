---
title: Elemento Janeiro (monthtype)
description: Especifica que a tarefa é executada em Janeiro.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Elemento de janeiro Agendador de Tarefas
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644385"
---
# <a name="january-monthstype-element"></a>Elemento Janeiro (monthtype)

Especifica que a tarefa é executada em Janeiro.

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

O elemento **janeiro** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.<br/>             |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em Janeiro.


```XML
<Months>
    <January/>
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

 

 





