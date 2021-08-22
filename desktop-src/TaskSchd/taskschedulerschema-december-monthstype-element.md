---
title: Elemento December (monthsType)
description: Especifica que a tarefa é executado em dezembro.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- Elemento December Agendador de Tarefas
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9212641956abc4e52f455a83ac6d5e58a8560fa44cd68068dc809280b30e5faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516916"
---
# <a name="december-monthstype-element"></a>Elemento December (monthsType)

Especifica que a tarefa é executado em dezembro.

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

O **elemento December** é definido pelo tipo complexo [**monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal do dia da semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal.<br/>             |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em dezembro.


```XML
<Months>
    <December/>
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

 

 





