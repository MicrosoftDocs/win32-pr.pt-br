---
title: Elemento April (monthtype)
description: Especifica que a tarefa é executada em abril.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Elemento de abril Agendador de Tarefas
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f717e015c320c03b6d41e4c17d04cf3a255f85eb150a3f292933c370a516ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125876"
---
# <a name="april-monthstype-element"></a>Elemento April (monthtype)

Especifica que a tarefa é executada em abril.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

O elemento **abril** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.<br/>             |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthtype**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.<br/> |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em abril.


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





