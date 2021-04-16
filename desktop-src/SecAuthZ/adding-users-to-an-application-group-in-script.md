---
description: Um grupo de aplicativos é um grupo de usuários e grupos de usuários. Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados. Um grupo de aplicativos é representado por um objeto IAzApplicationGroup.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Adicionando usuários a um grupo de aplicativos no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752423"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="e02eb-105">Adicionando usuários a um grupo de aplicativos no script</span><span class="sxs-lookup"><span data-stu-id="e02eb-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="e02eb-106">No Gerenciador de autorização, um grupo de aplicativos é um grupo de usuários e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="e02eb-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="e02eb-107">Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="e02eb-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="e02eb-108">Um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="e02eb-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="e02eb-109">**Para permitir que os membros de um grupo de aplicativos executem uma tarefa ou um conjunto de tarefas**</span><span class="sxs-lookup"><span data-stu-id="e02eb-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="e02eb-110">Atribua esse grupo de aplicativos a uma função que contenha essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="e02eb-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="e02eb-111">As funções são representadas por objetos [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="e02eb-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="e02eb-112">O exemplo a seguir mostra como criar um grupo de aplicativos, adicionar um usuário como um membro do grupo de aplicativos e atribuir o grupo de aplicativos a uma função existente.</span><span class="sxs-lookup"><span data-stu-id="e02eb-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="e02eb-113">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém uma função de administrador de despesas.</span><span class="sxs-lookup"><span data-stu-id="e02eb-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



