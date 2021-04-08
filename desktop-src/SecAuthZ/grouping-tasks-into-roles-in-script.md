---
description: No Gerenciador de autorização, uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Agrupando tarefas em funções no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922519"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Agrupando tarefas em funções no script

No Gerenciador de autorização, uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar. As tarefas são agrupadas e atribuídas a uma definição de função, que é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) com sua propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) definida como **true**. Em seguida, a definição de função pode ser atribuída a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , e os usuários ou grupos de usuários são atribuídos a esse objeto. Para obter mais informações sobre tarefas e funções, consulte [funções](roles.md).

O exemplo a seguir mostra como atribuir tarefas a uma definição de função, criar um objeto de função e atribuir a definição de função ao objeto Role. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém tarefas chamadas enviar despesa e aprovar despesas.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



