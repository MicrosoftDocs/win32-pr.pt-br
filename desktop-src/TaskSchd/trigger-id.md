---
title: Propriedade Trigger.Id
description: Para scripts, Obtém ou define o identificador do gatilho.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Agendador de Tarefas de propriedade de ID
- Agendador de Tarefas de propriedade de ID, objeto de gatilho
- Objeto de gatilho Agendador de Tarefas, propriedade de ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499301"
---
# <a name="triggerid-property"></a>Propriedade Trigger.Id

Para scripts, Obtém ou define o identificador do gatilho.

## <a name="syntax"></a>Syntax


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador do gatilho. Esse identificador é usado pelo Agendador de Tarefas para fins de log.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o identificador do gatilho é especificado no atributo ID dos elementos de gatilho individuais (por exemplo, o atributo ID do elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) do esquema de Agendador de tarefas.

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
</dt> </dl>

 

 





