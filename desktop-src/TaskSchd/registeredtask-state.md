---
title: Propriedade RegisteredTask.State
description: Para scripts, obtém o estado operacional da tarefa registrada.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Propriedades de estado Agendador de Tarefas
- Propriedade state Agendador de Tarefas objeto , RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas propriedade , State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6099c47590397556937b8b1cceb59bc231117aa16c92012d59964afec4f6bcf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759597"
---
# <a name="registeredtaskstate-property"></a>Propriedade RegisteredTask.State

Para scripts, obtém o estado operacional da tarefa registrada.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Valor da propriedade

Uma [**constante \_ TASK STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) que define o estado operacional da tarefa.



| Valor                                                                                                                                                                                                                                   | Significado                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**TAREFA \_ ESTADO \_ DESCONHECIDO**</dt> <dt>0</dt> </dl>    | O estado da tarefa é desconhecido.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**TAREFA \_ ESTADO \_ DESABILITADO**</dt> <dt>1</dt> </dl> | A tarefa está registrada, mas está desabilitada e nenhuma instância da tarefa está na fila ou em execução. A tarefa não pode ser executado até que ela seja habilitada.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**TAREFA \_ STATE \_ NA FILA**</dt> <dt>2</dt> </dl>       | As instâncias da tarefa estão na fila.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**TAREFA \_ STATE \_ READY**</dt> <dt>3</dt> </dl>          | A tarefa está pronta para ser executada, mas nenhuma instância está na fila ou em execução.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**TAREFA \_ ESTADO \_ EXECUTANDO**</dt> <dt>4</dt> </dl>    | Uma ou mais instâncias da tarefa estão em execução.<br/>                                                                                         |



 

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

 

 





