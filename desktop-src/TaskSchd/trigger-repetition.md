---
title: Propriedade Trigger. Repetition
description: Para scripts, Obtém ou define um valor que indica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Agendador de Tarefas da propriedade de repetição
- Agendador de Tarefas de propriedade de repetição, objeto de gatilho
- Objeto de gatilho Agendador de Tarefas, propriedade de repetição
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
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758390"
---
# <a name="triggerrepetition-property"></a>Propriedade Trigger. Repetition

Para scripts, Obtém ou define um valor que indica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**RepetitionPattern**](repetitionpattern.md) que define a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, o padrão de repetição para um gatilho é especificado no elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





