---
title: Objeto TaskFolder
description: Objeto de script que fornece os métodos que são usados para registrar (criar) tarefas na pasta, remover tarefas da pasta e criar ou remover subpastas da pasta.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Agendador de Tarefas de objeto TaskFolder
- Agendador de Tarefas de objeto TaskFolder, descrito
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499648"
---
# <a name="taskfolder-object"></a>Objeto TaskFolder

Objeto de script que fornece os métodos que são usados para registrar (criar) tarefas na pasta, remover tarefas da pasta e criar ou remover subpastas da pasta.

## <a name="members"></a>Membros

O objeto **TaskFolder** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **TaskFolder** tem esses métodos.



| Método                                                              | Descrição                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | Cria uma pasta para tarefas relacionadas.<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | Exclui uma subpasta da pasta pai.<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | Exclui uma tarefa da pasta.<br/>                                                                                                     |
| [**GetFolder**](taskfolder-getfolder.md)                           | Obtém uma pasta que contém tarefas em um local especificado.<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | Obtém todas as subpastas na pasta.<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | Obtém o descritor de segurança para a pasta.<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | Obtém uma tarefa em um local especificado em uma pasta.<br/>                                                                                    |
| [**Gettarefas**](taskfolder-gettasks.md)                             | Obtém todas as tarefas na pasta.<br/>                                                                                                   |
| [**RegisterTask**](taskfolder-registertask.md)                     | Registra (cria) uma nova tarefa na pasta usando XML para definir a tarefa.<br/>                                                          |
| [**RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) | Registra (cria) uma tarefa em um local especificado usando a interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) para definir uma tarefa.<br/> |
| [**SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)   | Define o descritor de segurança para a pasta.<br/>                                                                                        |



 

### <a name="properties"></a>Propriedades

O objeto **TaskFolder** tem essas propriedades.



| Propriedade                                   | Tipo de acesso          | Descrição                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Nome**](taskfolder-name.md)<br/> | Somente leitura<br/> | Obtém o nome usado para identificar a pasta que contém uma tarefa.<br/> |
| [**Caminho**](taskfolder-path.md)<br/> | Somente leitura<br/> | Obtém o caminho para onde a pasta é armazenada.<br/>                            |



 

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

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





