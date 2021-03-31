---
title: Propriedade RunningTask. State
description: Para scripts, obtém um identificador para o estado da tarefa em execução.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Agendador de Tarefas de propriedade de estado
- Agendador de Tarefas de propriedade de estado, objeto RunningTask
- Agendador de Tarefas de objeto RunningTask, propriedade State
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
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644488"
---
# <a name="runningtaskstate-property"></a>Propriedade RunningTask. State

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
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**Tarefa \_ do ESTADO \_ desconhecido**</dt> <dt>0</dt> </dl>    | O estado da tarefa é desconhecido.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**Tarefa \_ do ESTADO \_ desabilitado**</dt> <dt>1</dt> </dl> | A tarefa está registrada, mas está desabilitada e nenhuma instância da tarefa está em fila ou em execução. A tarefa não pode ser executada até que esteja habilitada.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**Tarefa \_ do ESTADO \_ na fila**</dt> <dt>2</dt> </dl>       | As instâncias da tarefa são enfileiradas.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**Tarefa \_ do ESTADO \_ pronto**</dt> <dt>3</dt> </dl>          | A tarefa está pronta para ser executada, mas nenhuma instância está enfileirada ou em execução.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**Tarefa \_ do ESTADO \_ em execução**</dt> <dt>4</dt> </dl>    | Uma ou mais instâncias da tarefa estão em execução.<br/>                                                                                         |



 

## <a name="remarks"></a>Comentários

O método [**RunningTask. Refresh**](runningtask-refresh.md) é chamado antes que o valor da propriedade seja retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





