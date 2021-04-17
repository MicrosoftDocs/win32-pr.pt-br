---
description: Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delegando a definição de permissões em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752619"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="1f889-103">Delegando a definição de permissões em C++</span><span class="sxs-lookup"><span data-stu-id="1f889-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="1f889-104">Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração.</span><span class="sxs-lookup"><span data-stu-id="1f889-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="1f889-105">A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo.</span><span class="sxs-lookup"><span data-stu-id="1f889-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="1f889-106">Em cada nível, há uma lista de administradores e leitores.</span><span class="sxs-lookup"><span data-stu-id="1f889-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="1f889-107">Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado.</span><span class="sxs-lookup"><span data-stu-id="1f889-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="1f889-108">Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.</span><span class="sxs-lookup"><span data-stu-id="1f889-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="1f889-109">Um usuário ou grupo que seja um administrador ou um leitor de um aplicativo também deve ser adicionado como um usuário delegado do repositório de políticas que contém esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f889-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="1f889-110">Da mesma forma, um usuário ou grupo que é um administrador ou um leitor de um escopo deve ser adicionado como um usuário delegado do aplicativo que contém esse escopo.</span><span class="sxs-lookup"><span data-stu-id="1f889-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="1f889-111">Por exemplo, para delegar a administração de um escopo, primeiro adicione o usuário ou grupo à lista de usuários delegados do repositório que contém o escopo chamando o método [**IAzAuthorizationStore:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="1f889-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="1f889-112">Em seguida, adicione o usuário ou grupo à lista de usuários delegados do aplicativo que contém o escopo chamando o método [**IAzApplication:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="1f889-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="1f889-113">Por fim, adicione o usuário ou grupo à lista de administradores do escopo chamando o método [**IAzScope:: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .</span><span class="sxs-lookup"><span data-stu-id="1f889-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="1f889-114">Os repositórios de políticas baseados em XML não dão suporte à delegação em nenhum nível.</span><span class="sxs-lookup"><span data-stu-id="1f889-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="1f889-115">Um escopo dentro de um repositório de autorização armazenado no Active Directory não poderá ser delegado se o escopo contiver definições de tarefa que incluem regras de autorização ou definições de função que incluem regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="1f889-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="1f889-116">O exemplo a seguir mostra como delegar a administração de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f889-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="1f889-117">O exemplo supõe que haja um repositório de política de autorização de Active Directory existente no local especificado, que esse repositório de política contém um aplicativo denominado despesas e que este aplicativo não contém tarefas com scripts de regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="1f889-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



