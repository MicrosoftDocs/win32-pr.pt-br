---
title: Propriedade RegisteredTask. NextRunTime
description: Para scripts, obtém a hora em que a tarefa registrada está agendada para ser executada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Agendador de Tarefas da propriedade NextRunTime
- Propriedade NextRunTime Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, Propriedade NextRunTime
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
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644969"
---
# <a name="registeredtasknextruntime-property"></a>Propriedade RegisteredTask. NextRunTime

Para scripts, obtém a hora em que a tarefa registrada está agendada para ser executada.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valor da propriedade

A hora em que a tarefa registrada está próxima agendada para ser executada.

## <a name="remarks"></a>Comentários

Se a tarefa registrada contiver gatilhos que são desabilitados individualmente, esses gatilhos ainda afetarão o próximo tempo de execução agendado que é retornado, embora estejam desabilitados.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





