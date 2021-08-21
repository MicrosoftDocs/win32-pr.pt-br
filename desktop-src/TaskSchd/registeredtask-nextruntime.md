---
title: Propriedade RegisteredTask.NextRunTime
description: Para scripts, obtém a hora em que a tarefa registrada é agendada para ser executado.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Propriedade NextRunTime Agendador de Tarefas
- Propriedade NextRunTime Agendador de Tarefas objeto , RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas , propriedade NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060044"
---
# <a name="registeredtasknextruntime-property"></a>Propriedade RegisteredTask.NextRunTime

Para scripts, obtém a hora em que a tarefa registrada é agendada para ser executado.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valor da propriedade

A hora em que a tarefa registrada é agendada para ser executado.

## <a name="remarks"></a>Comentários

Se a tarefa registrada contiver gatilhos que estão desabilitados individualmente, esses gatilhos ainda afetarão o próximo tempo de executar agendado retornado, mesmo que eles sejam desabilitados.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





