---
description: No Gerenciador de autorização, um grupo de aplicativos é um grupo de usuários e grupos de usuários. Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados.
ms.assetid: b01883d6-eae6-4f3a-b269-90c22827f116
title: Adicionando usuários a um grupo de aplicativos em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fa08ddd93ba1743a20e3eb14a5f62344741c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091008"
---
# <a name="adding-users-to-an-application-group-in-c"></a><span data-ttu-id="b45b0-104">Adicionando usuários a um grupo de aplicativos em C++</span><span class="sxs-lookup"><span data-stu-id="b45b0-104">Adding Users to an Application Group in C++</span></span>

<span data-ttu-id="b45b0-105">No Gerenciador de autorização, um grupo de aplicativos é um grupo de usuários e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="b45b0-105">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="b45b0-106">Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="b45b0-106">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="b45b0-107">Um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="b45b0-107">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="b45b0-108">Para permitir que os membros de um grupo de aplicativos executem uma tarefa ou um conjunto de tarefas, atribua esse grupo de aplicativos a uma função que contenha essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="b45b0-108">To allow members of an application group to perform a task or set of tasks, assign that application group to a role that contains those tasks.</span></span> <span data-ttu-id="b45b0-109">As funções são representadas por objetos [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="b45b0-109">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="b45b0-110">O exemplo a seguir mostra como criar um grupo de aplicativos, adicionar um usuário como um membro do grupo de aplicativos e atribuir o grupo de aplicativos a uma função existente.</span><span class="sxs-lookup"><span data-stu-id="b45b0-110">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="b45b0-111">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C, que esse armazenamento contém um aplicativo denominado despesas e que esse aplicativo contém uma função de administrador de despesas.</span><span class="sxs-lookup"><span data-stu-id="b45b0-111">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzApplicationGroup* pAppGroup = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR groupName = NULL;
    BSTR userName = NULL;
    BSTR roleName = NULL;
    
    
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
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
  storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Allocate a string for the group name.
    if (!(groupName = SysAllocString(L"Approvers")))
        MyHandleError("Could not allocate group name string.");

    //  Create an IAzApplicationGroup object.
    hr = pApp->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add a member to the group.
 //  Replace with valid domain and user name.
    if (!(userName = SysAllocString(L"domain\\username")))
        MyHandleError("Could not allocate user name string.");

    hr = pAppGroup->AddMemberName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add user to application group.");

    //  Save information to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save group information.");

    //  Open an IAzRole object.
    if (!(roleName = SysAllocString(L"Expense Administrator")))
        MyHandleError("Could not allocate role name string.");

    hr = pApp->OpenRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open role object.");

    //  Add the group to the role.
    hr = pRole->AddAppMember(groupName, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not add the application group to the role.");


    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pAppGroup->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(groupName);
    SysFreeString(roleName);
    SysFreeString(userName);
    VariantClear(&myVar);
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



 

 



