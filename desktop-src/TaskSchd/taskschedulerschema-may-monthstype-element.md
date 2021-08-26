---
title: Elemento May (monthsType)
description: Especifica que a tarefa é executado em maio.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Elemento May Agendador de Tarefas
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d8a7edc0429b77042a5ef7bbb6e16bf69bda8a4c6ed889bbf8c1b981b912ab1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905606"
---
# <a name="may-monthstype-element"></a>Elemento May (monthsType)

Especifica que a tarefa é executado em maio.

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

O **elemento May** é definido pelo tipo complexo [**monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                          | Derivado de                                                     | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal do dia da semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal.<br/>             |



## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em maio.


```XML
<Months>
    <May/>
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

 

 





