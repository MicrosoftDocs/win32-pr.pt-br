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
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796305"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





