---
title: Propriedade Trigger.Repetition
description: Para scripts, obtém ou define um valor que indica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Propriedade de repetição Agendador de Tarefas
- Propriedade de repetição Agendador de Tarefas , objeto Trigger
- Gatilho de objeto Agendador de Tarefas , propriedade De repetição
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e14b8dc23b329d9646647fdcc1c5bcb3166c5bf885886a5308c329e186dc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002104"
---
# <a name="triggerrepetition-property"></a>Propriedade Trigger.Repetition

Para scripts, obtém ou define um valor que indica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto RepetitionPattern**](repetitionpattern.md) que define a frequência com que a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou escrever seu próprio XML para uma tarefa, o padrão de repetição de um gatilho é especificado no elemento [**De**](taskschedulerschema-repetition-triggerbasetype-element.md) repetição do Agendador de Tarefas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





