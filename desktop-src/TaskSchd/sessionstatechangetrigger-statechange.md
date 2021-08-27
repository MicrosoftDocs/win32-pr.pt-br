---
title: Propriedade SessionStateChangeTrigger.StateChange
description: Para scripts, obtém ou define o tipo de alteração de sessão do Servidor de Terminal que dispararia uma iniciação de tarefa.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Propriedade StateChange Agendador de Tarefas
- Propriedade StateChange Agendador de Tarefas objeto , SessionStateChangeTrigger
- Objeto SessionStateChangeTrigger Agendador de Tarefas propriedade , StateChange
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
ms.openlocfilehash: cfbd2037f19ca2d9fe8ec5d0ba046e69894f431b81d623b61b9474515bcef3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100156"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Propriedade SessionStateChangeTrigger.StateChange

Para scripts, obtém ou define o tipo de alteração de sessão do Servidor de Terminal que dispararia uma iniciação de tarefa.

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valor da propriedade

O tipo de alteração de sessão do Servidor de Terminal que dispara uma tarefa a ser lançada.

Os valores possíveis são da [**enumeração TASK \_ SESSION STATE \_ CHANGE \_ \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type)



| Valor                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**TAREFA \_ CONSOLE \_ CONNECT**</dt> <dt>1</dt> </dl>          | Alteração de estado de conexão do console do Servidor do Terminal. Por exemplo, quando você se conecta a uma sessão de usuário no computador local, alternando usuários no computador. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**TAREFA \_ CONSOLE \_ DISCONNECT**</dt> <dt>2</dt> </dl> | Alteração de estado de desconexão do console do Servidor do Terminal. Por exemplo, quando você se desconecta a uma sessão de usuário no computador local, alternando usuários no computador.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**TAREFA \_ REMOTE \_ CONNECT**</dt> <dt>3</dt> </dl>             | Alteração de estado de conexão remota do Servidor terminal. Por exemplo, quando um usuário se conecta a uma sessão de usuário usando o Conexão de Área de Trabalho Remota de um computador remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**TAREFA \_ REMOTE \_ DISCONNECT**</dt> <dt>4</dt> </dl>    | Alteração de estado de desconexão remota do Servidor terminal. Por exemplo, quando um usuário se desconecta de uma sessão de usuário ao usar o Conexão de Área de Trabalho Remota de um computador remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**TAREFA \_ BLOQUEIO \_ DE SESSÃO**</dt> <dt>7</dt> </dl>                   | Alteração de estado bloqueado da sessão do Servidor do Terminal. Por exemplo, essa alteração de estado faz com que a tarefa seja executado quando o computador está bloqueado. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**TAREFA \_ DESBLOQUEIO \_ DE SESSÃO**</dt> <dt>8</dt> </dl>             | Alteração de estado desbloqueada da sessão do Servidor do Terminal. Por exemplo, essa alteração de estado faz com que a tarefa seja executado quando o computador é desbloqueado.<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





