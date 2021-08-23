---
title: Elemento March (monthsType)
description: Especifica que a tarefa é executado em março.
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- Elemento march Agendador de Tarefas
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d90d64e0fd275f57252cd435ae5dc42abfe8ba17613e1b20425fc27c515509e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139179"
---
# <a name="march-monthstype-element"></a>Elemento March (monthsType)

Especifica que a tarefa é executado em março.

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

O **elemento March** é definido pelo tipo complexo [**monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal do dia da semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal.<br/>             |



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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





