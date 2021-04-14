---
title: Objeto TaskService
description: Para scripts, o fornece acesso ao serviço de Agendador de Tarefas para gerenciar tarefas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Agendador de Tarefas de objeto TaskService
- Agendador de Tarefas de objeto TaskService, descrito
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455698"
---
# <a name="taskservice-object"></a>Objeto TaskService

Para scripts, o fornece acesso ao serviço de Agendador de Tarefas para gerenciar tarefas registradas.

O método [**TaskService. Connect**](taskservice-connect.md) deve ser chamado antes de chamar qualquer um dos outros métodos **TaskService** .

## <a name="members"></a>Membros

O objeto **TaskService** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **TaskService** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connect**](taskservice-connect.md)                 | Conecta-se a um computador remoto e associa todas as chamadas subsequentes nesta interface a uma sessão remota.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Obtém o caminho para uma pasta de tarefas registradas.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Obtém uma coleção de tarefas em execução.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **TaskService** tem essas propriedades.



| Propriedade                                                          | Descrição                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Conectado**](taskservice-connected.md)<br/>             | Obtém um valor booliano que indica se você está conectado ao serviço de Agendador de Tarefas.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Obtém o nome do domínio ao qual o computador [**TargetServer**](taskservice-targetserver.md) está conectado.<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Obtém o nome do usuário que está conectado ao serviço de Agendador de Tarefas.<br/>                                       |
| HighestVersion<br/>                                         | Obtém a versão mais recente do Agendador de Tarefas a que um computador dá suporte.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.<br/>          |



 

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para este objeto de script, consulte o [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md), [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), [exemplo de gatilho semanal (script)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (Scripting)](logon-trigger-example--scripting-.md), [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md)ou [exibição de nomes de tarefas e Estados (scripts)](displaying-task-names-and-state--scripting-.md).

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

 

 





