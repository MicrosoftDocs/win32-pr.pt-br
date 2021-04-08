---
description: No Gerenciador de autorização, uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Agrupando operações em tarefas no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829745"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Agrupando operações em tarefas no script

No Gerenciador de autorização, uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir. As tarefas são feitas de operações, que são funções e métodos de nível baixo do aplicativo. Uma tarefa é então atribuída a essas funções que devem executar essa tarefa. Uma tarefa é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Para obter mais informações sobre operações e tarefas, consulte [operações e tarefas](operations-and-tasks.md).

O exemplo a seguir mostra como agrupar operações para criar uma tarefa. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém operações definidas no tópico [definindo operações no script](defining-operations-in-script.md).


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



