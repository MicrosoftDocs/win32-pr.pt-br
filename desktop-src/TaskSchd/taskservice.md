---
title: Objeto TaskService
description: Para scripts, fornece acesso ao serviço Agendador de Tarefas para gerenciar tarefas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objeto TaskService Agendador de Tarefas
- Objeto TaskService Agendador de Tarefas , descrito
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
ms.openlocfilehash: 74f20840a5580d0188354ca6b65ab3ce5b7402d57ea7346462d2f990ecfe34cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658646"
---
# <a name="taskservice-object"></a>Objeto TaskService

Para scripts, fornece acesso ao serviço Agendador de Tarefas para gerenciar tarefas registradas.

O [**método TaskService.Conexão**](taskservice-connect.md) deve ser chamado antes de chamar qualquer um dos outros **métodos TaskService.**

## <a name="members"></a>Membros

O **objeto TaskService** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto TaskService** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](taskservice-connect.md)                 | Conecta-se a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota.<br/>                                                                                                 |
| [**Getfolder**](taskservice-getfolder.md)             | Obtém o caminho para uma pasta de tarefas registradas.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Obtém uma coleção de tarefas em execução.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto TaskService** tem essas propriedades.



| Propriedade                                                          | Descrição                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Conectado**](taskservice-connected.md)<br/>             | Obtém um valor booliana que indica se você está conectado ao Agendador de Tarefas serviço.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Obtém o nome do domínio ao qual o [**computador TargetServer**](taskservice-targetserver.md) está conectado.<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Obtém o nome do usuário que está conectado ao Agendador de Tarefas serviço.<br/>                                       |
| HighestVersion<br/>                                         | Obtém a versão mais alta do Agendador de Tarefas compatível com um computador.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Obtém o nome do computador que está executando o Agendador de Tarefas serviço ao que o usuário está conectado.<br/>          |



 

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte Exemplo de gatilho de tempo [(script),](time-trigger-example--scripting-.md)exemplo de gatilho de evento [(script),](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))exemplo de gatilho diário [(script),](daily-trigger-example--scripting-.md)exemplo de gatilho de [registro (script),](registration-trigger-example--scripting-.md)exemplo de gatilho semanal [(script),](weekly-trigger-example--scripting-.md)exemplo de gatilho de [logon (script),](logon-trigger-example--scripting-.md)exemplo de gatilho de inicialização [(script)](boot-trigger-example--scripting-.md)ou exibindo nomes e estados de tarefas [(scripts).](displaying-task-names-and-state--scripting-.md)

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
</dt> </dl>

 

 





