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
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="574eb-103">Delegando a definição de permissões no script</span><span class="sxs-lookup"><span data-stu-id="574eb-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="574eb-104">Você pode delegar a administração de armazenamentos de diretiva de autorização armazenados no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="574eb-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="574eb-105">A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo.</span><span class="sxs-lookup"><span data-stu-id="574eb-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="574eb-106">Em cada nível, há uma lista de administradores e leitores.</span><span class="sxs-lookup"><span data-stu-id="574eb-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="574eb-107">Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado.</span><span class="sxs-lookup"><span data-stu-id="574eb-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="574eb-108">Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.</span><span class="sxs-lookup"><span data-stu-id="574eb-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="574eb-109">Um usuário ou grupo que seja um administrador ou um leitor de um aplicativo também deve ser adicionado como um usuário delegado do repositório de políticas que contém esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="574eb-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="574eb-110">Da mesma forma, um usuário ou grupo que é um administrador ou um leitor de um escopo deve ser adicionado como um usuário delegado do aplicativo que contém esse escopo.</span><span class="sxs-lookup"><span data-stu-id="574eb-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="574eb-111">**Para delegar a administração de um escopo**</span><span class="sxs-lookup"><span data-stu-id="574eb-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="574eb-112">Adicione o usuário ou grupo à lista de usuários delegados do repositório que contém o escopo chamando o método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) do objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que contém o escopo.</span><span class="sxs-lookup"><span data-stu-id="574eb-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="574eb-113">Adicione o usuário ou grupo à lista de usuários delegados do aplicativo que contém o escopo chamando o método [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) do objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que contém o escopo.</span><span class="sxs-lookup"><span data-stu-id="574eb-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="574eb-114">Adicione o usuário ou grupo à lista de administradores do escopo chamando o método [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) do objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="574eb-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="574eb-115">Os repositórios de políticas baseados em XML não dão suporte à delegação em nenhum nível.</span><span class="sxs-lookup"><span data-stu-id="574eb-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="574eb-116">Se um escopo em um repositório de autorização armazenado no Active Directory contiver definições de tarefa que incluem regras de autorização ou definições de função que incluem regras de autorização, o escopo não poderá ser delegado.</span><span class="sxs-lookup"><span data-stu-id="574eb-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="574eb-117">O exemplo a seguir mostra como delegar a administração de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="574eb-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="574eb-118">O exemplo supõe que haja um repositório de política de autorização de Active Directory existente no local especificado, que esse repositório de política contém um aplicativo denominado despesas e que este aplicativo não contém tarefas com scripts de regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="574eb-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



