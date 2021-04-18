---
title: Elemento StopAtDurationEnd (rerepetiçãotype)
description: Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Agendador de Tarefas do elemento StopAtDurationEnd
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753334"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Elemento StopAtDurationEnd (rerepetiçãotype)

Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição. Isso será aplicável somente se as repetições estiverem definidas.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

O elemento **StopAtDurationEnd** é definido pelo tipo complexo [**rerepetiçãotype**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Elemento pai

| Elemento | Derivado de | Descrição |
|-|-|-|
| [**Repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |

## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, essa configuração é especificada usando a propriedade [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .

Para desenvolvimento em C++, essa configuração é especificada usando a propriedade [**IRepetitionPattern:: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |

## <a name="see-also"></a>Confira também

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)

[Agendador de Tarefas](task-scheduler-start-page.md)
