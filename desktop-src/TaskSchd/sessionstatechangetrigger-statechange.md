---
title: Propriedade SessionStateChangeTrigger. StateChange
description: Para scripts, Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Agendador de Tarefas da propriedade StateChange
- Propriedade StateChange Agendador de Tarefas, objeto SessionStateChangeTrigger
- Objeto SessionStateChangeTrigger Agendador de Tarefas, Propriedade StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644428"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Propriedade SessionStateChangeTrigger. StateChange

Para scripts, Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valor da propriedade

O tipo de Terminal Server alteração de sessão que dispara uma tarefa a ser iniciada.

Os valores possíveis são da enumeração [**de \_ \_ tipo de \_ alteração \_ de estado de sessão de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .



| Valor                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**Tarefa \_ do CONSOLE \_ Connect**</dt> <dt>1</dt> </dl>          | Terminal Server alteração de estado da conexão do console. Por exemplo, quando você se conecta a uma sessão de usuário no computador local, alternando os usuários no computador. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**Tarefa \_ do \_Desconexão do console**</dt> <dt>2</dt> </dl> | Alteração do estado de desconexão do Console Terminal Server. Por exemplo, quando você se desconecta a uma sessão de usuário no computador local, alternando os usuários no computador.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**Tarefa \_ do \_Conexão remota**</dt> <dt>3</dt> </dl>             | Terminal Server alteração de estado da conexão remota. Por exemplo, quando um usuário se conecta a uma sessão de usuário usando o programa Conexão de Área de Trabalho Remota de um computador remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**Tarefa \_ do \_Desconexão remota**</dt> <dt>4</dt> </dl>    | Terminal Server alteração de estado de desconexão remota. Por exemplo, quando um usuário se desconecta de uma sessão de usuário enquanto usa o programa de Conexão de Área de Trabalho Remota de um computador remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**Tarefa \_ do \_Bloqueio de sessão**</dt> <dt>7</dt> </dl>                   | Alteração de estado bloqueado da sessão de Terminal Server. Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é bloqueado. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**Tarefa \_ do \_Desbloqueio de sessão**</dt> <dt>8</dt> </dl>             | Alteração de estado desbloqueado da sessão de Terminal Server. Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é desbloqueado.<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





