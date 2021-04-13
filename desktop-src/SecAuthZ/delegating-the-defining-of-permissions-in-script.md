---
description: Você pode delegar a administração dos armazenamentos de política de autorização armazenados no Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delegando a definição de permissões no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296960"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Delegando a definição de permissões no script

Você pode delegar a administração de armazenamentos de diretiva de autorização armazenados no Active Directory. A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo.

Em cada nível, há uma lista de administradores e leitores. Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado. Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.

Um usuário ou grupo que seja um administrador ou um leitor de um aplicativo também deve ser adicionado como um usuário delegado do repositório de políticas que contém esse aplicativo. Da mesma forma, um usuário ou grupo que é um administrador ou um leitor de um escopo deve ser adicionado como um usuário delegado do aplicativo que contém esse escopo.

**Para delegar a administração de um escopo**

1.  Adicione o usuário ou grupo à lista de usuários delegados do repositório que contém o escopo chamando o método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) do objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que contém o escopo.
2.  Adicione o usuário ou grupo à lista de usuários delegados do aplicativo que contém o escopo chamando o método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) do objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que contém o escopo.
3.  Adicione o usuário ou grupo à lista de administradores do escopo chamando o método [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) do objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .

> [!Note]  
> Os repositórios de políticas baseados em XML não dão suporte à delegação em nenhum nível.

 

Se um escopo em um repositório de autorização armazenado no Active Directory contiver definições de tarefa que incluem regras de autorização ou definições de função que incluem regras de autorização, o escopo não poderá ser delegado.

O exemplo a seguir mostra como delegar a administração de um aplicativo. O exemplo supõe que haja um repositório de política de autorização de Active Directory existente no local especificado, que esse repositório de política contém um aplicativo denominado despesas e que este aplicativo não contém tarefas com scripts de regra de negócio.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



