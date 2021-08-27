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
ms.openlocfilehash: 896aa6db4ce5bf2c0dddf666024c143754afc97ec76bfb557e6431f593689857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010536"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |

## <a name="see-also"></a>Confira também

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)

[Agendador de Tarefas](task-scheduler-start-page.md)
