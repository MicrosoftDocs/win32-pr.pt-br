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
# <a name="grouping-tasks-into-roles-in-script"></a><span data-ttu-id="0e604-103">Agrupando tarefas em funções no script</span><span class="sxs-lookup"><span data-stu-id="0e604-103">Grouping Tasks into Roles in Script</span></span>

<span data-ttu-id="0e604-104">No Gerenciador de autorização, uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar.</span><span class="sxs-lookup"><span data-stu-id="0e604-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="0e604-105">As tarefas são agrupadas e atribuídas a uma definição de função, que é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) com sua propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="0e604-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **True**.</span></span> <span data-ttu-id="0e604-106">Em seguida, a definição de função pode ser atribuída a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , e os usuários ou grupos de usuários são atribuídos a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="0e604-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="0e604-107">Para obter mais informações sobre tarefas e funções, consulte [funções](roles.md).</span><span class="sxs-lookup"><span data-stu-id="0e604-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="0e604-108">O exemplo a seguir mostra como atribuir tarefas a uma definição de função, criar um objeto de função e atribuir a definição de função ao objeto Role.</span><span class="sxs-lookup"><span data-stu-id="0e604-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="0e604-109">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém tarefas chamadas enviar despesa e aprovar despesas.</span><span class="sxs-lookup"><span data-stu-id="0e604-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


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



 

 



