---
description: No Gerenciador de autorização, um objeto IAzApplicationGroup representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Definindo grupos de usuários em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837100"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="e5bce-104">Definindo grupos de usuários em C++</span><span class="sxs-lookup"><span data-stu-id="e5bce-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="e5bce-105">No Gerenciador de autorização, um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="e5bce-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="e5bce-106">As funções podem ser atribuídas a esse grupo de usuários coletivamente.</span><span class="sxs-lookup"><span data-stu-id="e5bce-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="e5bce-107">Um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) também pode incluir outros objetos **IAzApplicationGroup** como membros.</span><span class="sxs-lookup"><span data-stu-id="e5bce-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="e5bce-108">Para obter mais informações sobre grupos de aplicativos, consulte [usuários e grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e5bce-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="e5bce-109">Um grupo pode ser definido por listas explícitas de membros e não membros, ou por uma consulta LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e5bce-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="e5bce-110">Os exemplos a seguir mostram como criar cada tipo de grupo de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="e5bce-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="e5bce-111">Criando um grupo básico</span><span class="sxs-lookup"><span data-stu-id="e5bce-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="e5bce-112">Criando um grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="e5bce-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="e5bce-113">Criando um grupo básico</span><span class="sxs-lookup"><span data-stu-id="e5bce-113">Creating a Basic Group</span></span>

<span data-ttu-id="e5bce-114">Um grupo de aplicativos básico é definido pelos membros incluídos nas propriedades [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) do objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa o grupo.</span><span class="sxs-lookup"><span data-stu-id="e5bce-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="e5bce-115">Os usuários e grupos listados na propriedade **Members** são incluídos no grupo de aplicativos, e os usuários e grupos listados na propriedade **nonmembers** são excluídos do grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e5bce-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="e5bce-116">Estar listado na propriedade **nonmembers** está sendo listado na propriedade **Members** .</span><span class="sxs-lookup"><span data-stu-id="e5bce-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="e5bce-117">O exemplo a seguir mostra como criar um grupo de aplicativos básico e adicionar todos os usuários locais como membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="e5bce-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="e5bce-118">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.</span><span class="sxs-lookup"><span data-stu-id="e5bce-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

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

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="e5bce-119">Criando um grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="e5bce-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="e5bce-120">Um grupo de consulta LDAP tem uma associação definida pela consulta contida no valor de sua propriedade [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="e5bce-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="e5bce-121">O exemplo a seguir mostra como criar um grupo de aplicativos de consulta LDAP e adicionar todos os usuários como membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="e5bce-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="e5bce-122">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.</span><span class="sxs-lookup"><span data-stu-id="e5bce-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
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



 

 
