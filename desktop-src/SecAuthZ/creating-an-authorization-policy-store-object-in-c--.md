---
description: Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Criando um objeto de repositório de política de autorização em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921196"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="1a32f-104">Criando um objeto de repositório de política de autorização em C++</span><span class="sxs-lookup"><span data-stu-id="1a32f-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="1a32f-105">Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1a32f-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="1a32f-106">As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja.</span><span class="sxs-lookup"><span data-stu-id="1a32f-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="1a32f-107">Quando um aplicativo que usa o Gerenciador de autorização é inicializado, ele carrega essas informações da loja.</span><span class="sxs-lookup"><span data-stu-id="1a32f-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="1a32f-108">O repositório de política de autorização deve estar localizado em um sistema confiável, pois os administradores nesse sistema têm um alto grau de acesso à loja.</span><span class="sxs-lookup"><span data-stu-id="1a32f-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="1a32f-109">O Gerenciador de autorização dá suporte ao armazenamento da política de autorização no serviço de diretório Active Directory ou em um arquivo XML, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a32f-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="1a32f-110">Na API do Gerenciador de autorização, um repositório de política de autorização é representado por um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="1a32f-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="1a32f-111">Os exemplos mostram como criar um objeto **AzAuthorizationStore** para um repositório de Active Directory e um repositório XML.</span><span class="sxs-lookup"><span data-stu-id="1a32f-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="1a32f-112">Criando um repositório de Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a32f-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="1a32f-113">Criando um repositório de SQL Server</span><span class="sxs-lookup"><span data-stu-id="1a32f-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="1a32f-114">Criando um repositório XML</span><span class="sxs-lookup"><span data-stu-id="1a32f-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="1a32f-115">Criando um repositório de Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a32f-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="1a32f-116">Para usar Active Directory para armazenar a política de autorização, o domínio deve estar no nível funcional de domínio do **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="1a32f-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="1a32f-117">O repositório de diretivas de autorização não pode estar localizado em um **contexto de nomenclatura que não seja de domínio** (também chamado de partição de aplicativo).</span><span class="sxs-lookup"><span data-stu-id="1a32f-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="1a32f-118">É recomendável que o repositório esteja localizado no contêiner de **dados do programa** em uma nova unidade organizacional criada especificamente para o repositório de políticas de autorização.</span><span class="sxs-lookup"><span data-stu-id="1a32f-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="1a32f-119">Também é recomendável que o repositório esteja localizado na mesma rede de área local que os servidores de aplicativos que executam aplicativos que usam o repositório.</span><span class="sxs-lookup"><span data-stu-id="1a32f-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="1a32f-120">O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a32f-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="1a32f-121">O exemplo supõe que haja uma Active Directory unidade organizacional denominada dados de programa em um domínio chamado authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="1a32f-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="1a32f-122">Criando um repositório de SQL Server</span><span class="sxs-lookup"><span data-stu-id="1a32f-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="1a32f-123">O Gerenciador de autorização dá suporte à criação de um repositório de política de autorização baseado em Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1a32f-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="1a32f-124">Para criar um repositório de autorização baseado em SQL Server, use uma URL que comece com o prefixo **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="1a32f-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="1a32f-125">A URL deve conter uma cadeia de conexão SQL válida, um nome de banco de dados e o nome do repositório de política de autorização: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="1a32f-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="1a32f-126">Se a instância do SQL Server não contiver o banco de dados do Gerenciador de autorização especificado, o Gerenciador de autorização criará um novo banco de dados com esse nome.</span><span class="sxs-lookup"><span data-stu-id="1a32f-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="1a32f-127">As conexões com um repositório de SQL Server não são criptografadas, a menos que você configure explicitamente a criptografia do SQL para a conexão ou configure a criptografia do tráfego de rede que usa o IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="1a32f-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="1a32f-128">O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um banco de dados SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1a32f-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a><span data-ttu-id="1a32f-129">Criando um repositório XML</span><span class="sxs-lookup"><span data-stu-id="1a32f-129">Creating an XML Store</span></span>

<span data-ttu-id="1a32f-130">O Gerenciador de autorização dá suporte à criação de um repositório de política de autorização no formato XML.</span><span class="sxs-lookup"><span data-stu-id="1a32f-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="1a32f-131">O repositório XML pode estar localizado no mesmo computador em que o aplicativo é executado, ou pode ser armazenado remotamente.</span><span class="sxs-lookup"><span data-stu-id="1a32f-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="1a32f-132">Não há suporte para editar o arquivo XML diretamente.</span><span class="sxs-lookup"><span data-stu-id="1a32f-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="1a32f-133">Use o snap-in do MMC do Gerenciador de autorização ou a API do Gerenciador de autorização para editar o repositório de políticas.</span><span class="sxs-lookup"><span data-stu-id="1a32f-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="1a32f-134">O Gerenciador de autorização não dá suporte à delegação de administração de um repositório de políticas XML.</span><span class="sxs-lookup"><span data-stu-id="1a32f-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="1a32f-135">Para obter informações sobre delegação, consulte [delegando a definição de permissões em C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="1a32f-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="1a32f-136">O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="1a32f-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



