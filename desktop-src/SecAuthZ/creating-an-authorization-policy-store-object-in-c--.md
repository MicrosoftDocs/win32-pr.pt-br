---
description: Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Criando um objeto de repositório de política de autorização em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be0b39633eb773b84ad16098f24b59cb23e5d9cc234afdfca414e9cba7a640b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782461"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Criando um objeto de repositório de política de autorização em C++

Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja. Quando um aplicativo que usa o Gerenciador de autorização é inicializado, ele carrega essas informações da loja. O repositório de política de autorização deve estar localizado em um sistema confiável, pois os administradores nesse sistema têm um alto grau de acesso à loja.

O Gerenciador de autorização dá suporte ao armazenamento da política de autorização no serviço de diretório Active Directory ou em um arquivo XML, conforme mostrado nos exemplos a seguir. Na API do Gerenciador de autorização, um repositório de política de autorização é representado por um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Os exemplos mostram como criar um objeto **AzAuthorizationStore** para um repositório de Active Directory e um repositório XML.

-   [Criando um repositório de Active Directory](#creating-an-active-directory-store)
-   [criando um repositório de SQL Server](#creating-a-sql-server-store)
-   [Criando um repositório XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Criando um repositório de Active Directory

para usar Active Directory para armazenar a política de autorização, o domínio deve estar no nível funcional de domínio do **Windows Server 2003** . O repositório de diretivas de autorização não pode estar localizado em um **contexto de nomenclatura que não seja de domínio** (também chamado de partição de aplicativo). É recomendável que o repositório esteja localizado no contêiner de **dados do programa** em uma nova unidade organizacional criada especificamente para o repositório de políticas de autorização. Também é recomendável que o repositório esteja localizado na mesma rede de área local que os servidores de aplicativos que executam aplicativos que usam o repositório.

O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização no Active Directory. O exemplo supõe que haja uma Active Directory unidade organizacional denominada dados de programa em um domínio chamado authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>criando um repositório de SQL Server

o gerenciador de autorização dá suporte à criação de um repositório de política de autorização baseado em Microsoft SQL Server. para criar um repositório de autorização baseado em SQL Server, use uma URL que comece com o prefixo **MSSQL://**. a URL deve conter uma cadeia de conexão SQL válida, um nome de banco de dados e o nome do repositório de política de autorização: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

se a instância do SQL Server não contiver o banco de dados do gerenciador de autorização especificado, o gerenciador de autorização criará um novo banco de dados com esse nome.

> [!Note]  
> as conexões com um repositório de SQL Server não são criptografadas, a menos que você configure explicitamente a criptografia de SQL para a conexão ou configure a criptografia do tráfego de rede que usa o IPsec (Internet Protocol Security).

 

o exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um banco de dados SQL Server.


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



## <a name="creating-an-xml-store"></a>Criando um repositório XML

O Gerenciador de autorização dá suporte à criação de um repositório de política de autorização no formato XML. O repositório XML pode estar localizado no mesmo computador em que o aplicativo é executado, ou pode ser armazenado remotamente. Não há suporte para editar o arquivo XML diretamente. Use o snap-in do MMC do Gerenciador de autorização ou a API do Gerenciador de autorização para editar o repositório de políticas.

O Gerenciador de autorização não dá suporte à delegação de administração de um repositório de políticas XML. Para obter informações sobre delegação, consulte [delegando a definição de permissões em C++](delegating-the-defining-of-permissions-in-c--.md).

O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um arquivo XML.


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



 

 



