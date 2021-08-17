---
title: Propriedade RunningTask.State
description: Para scripts, obtém um identificador para o estado da tarefa em execução.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Propriedades de estado Agendador de Tarefas
- Propriedade state Agendador de Tarefas objeto , RunningTask
- Objeto RunningTask Agendador de Tarefas propriedade , State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3c83b35c348e3ab86eb04c03ef4c5d25a76ef3fe5040603ce32da54ec4e217
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975036"
---
# <a name="runningtaskstate-property"></a>Propriedade RunningTask.State

Para scripts, obtém um identificador para o estado da tarefa em execução.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
RunningTask.State As String
```



## <a name="property-value"></a>Valor da propriedade

Um identificador para o estado da tarefa em execução.



| Valor                                                                                                                                                                                                                                   | Significado                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**TAREFA \_ ESTADO \_ DESCONHECIDO**</dt> <dt>0</dt> </dl>    | O estado da tarefa é desconhecido.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**TAREFA \_ ESTADO \_ DESABILITADO**</dt> <dt>1</dt> </dl> | A tarefa está registrada, mas está desabilitada e nenhuma instância da tarefa está na fila ou em execução. A tarefa não pode ser executado até que ela seja habilitada.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**TAREFA \_ STATE \_ NA FILA**</dt> <dt>2</dt> </dl>       | As instâncias da tarefa estão na fila.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**TAREFA \_ STATE \_ READY**</dt> <dt>3</dt> </dl>          | A tarefa está pronta para ser executada, mas nenhuma instância está na fila ou em execução.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**TAREFA \_ ESTADO \_ EXECUTANDO**</dt> <dt>4</dt> </dl>    | Uma ou mais instâncias da tarefa estão em execução.<br/>                                                                                         |



 

## <a name="remarks"></a>Comentários

O [**método RunningTask.Refresh**](runningtask-refresh.md) é chamado antes que o valor da propriedade seja retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





