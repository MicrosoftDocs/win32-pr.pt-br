---
title: Elemento Week (weektype)
description: Especifica uma semana específica do mês.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Elemento Week Agendador de Tarefas
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758202"
---
# <a name="week-weekstype-element"></a>Elemento Week (weektype)

Especifica uma semana específica do mês.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

O elemento **Week** é definido pelo tipo complexo [**weektype**](taskschedulerschema-weekstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                        | Derivado de                                                   | Descrição                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Semanas (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weektype**](taskschedulerschema-weekstype-complextype.md) | Especifica as semanas do mês em que a tarefa é executada.<br/> |



## <a name="remarks"></a>Comentários

Ao especificar as semanas do mês, use os números 1-4 para as primeiras quatro semanas do mês ou use a cadeia de caracteres "Last" para indicar que a última semana do mês.

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

 

 





