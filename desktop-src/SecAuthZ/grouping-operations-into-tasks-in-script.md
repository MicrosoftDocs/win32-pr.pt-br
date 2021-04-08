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
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="05d5e-103">Agrupando operações em tarefas no script</span><span class="sxs-lookup"><span data-stu-id="05d5e-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="05d5e-104">No Gerenciador de autorização, uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir.</span><span class="sxs-lookup"><span data-stu-id="05d5e-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="05d5e-105">As tarefas são feitas de operações, que são funções e métodos de nível baixo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05d5e-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="05d5e-106">Uma tarefa é então atribuída a essas funções que devem executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="05d5e-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="05d5e-107">Uma tarefa é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="05d5e-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="05d5e-108">Para obter mais informações sobre operações e tarefas, consulte [operações e tarefas](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="05d5e-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="05d5e-109">O exemplo a seguir mostra como agrupar operações para criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="05d5e-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="05d5e-110">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém operações definidas no tópico [definindo operações no script](defining-operations-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="05d5e-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


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



 

 



