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
ms.openlocfilehash: e2c9ff851eab7b5e9cfb124bf03c83986d24b391d5ea109865ff2d59e2e33536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002154"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





