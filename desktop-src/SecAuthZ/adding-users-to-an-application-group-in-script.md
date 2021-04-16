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
# <a name="adding-users-to-an-application-group-in-script"></a>Adicionando usuários a um grupo de aplicativos no script

No Gerenciador de autorização, um grupo de aplicativos é um grupo de usuários e grupos de usuários. Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados. Um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .

**Para permitir que os membros de um grupo de aplicativos executem uma tarefa ou um conjunto de tarefas**

-   Atribua esse grupo de aplicativos a uma função que contenha essas tarefas.

    As funções são representadas por objetos [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .

O exemplo a seguir mostra como criar um grupo de aplicativos, adicionar um usuário como um membro do grupo de aplicativos e atribuir o grupo de aplicativos a uma função existente. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém uma função de administrador de despesas.


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



 

 



