---
description: Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delegando a definição de permissões em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f79202a3f8ee21934f890d3c5a66a19be4466fa2b1ecdfe31672a4edfc2319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782050"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Delegando a definição de permissões em C++

Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração. A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo.

Em cada nível, há uma lista de administradores e leitores. Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado. Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.

Um usuário ou grupo que seja um administrador ou um leitor de um aplicativo também deve ser adicionado como um usuário delegado do repositório de políticas que contém esse aplicativo. Da mesma forma, um usuário ou grupo que é um administrador ou um leitor de um escopo deve ser adicionado como um usuário delegado do aplicativo que contém esse escopo.

Por exemplo, para delegar a administração de um escopo, primeiro adicione o usuário ou grupo à lista de usuários delegados do repositório que contém o escopo chamando o método [**IAzAuthorizationStore:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) . Em seguida, adicione o usuário ou grupo à lista de usuários delegados do aplicativo que contém o escopo chamando o método [**IAzApplication:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) . Por fim, adicione o usuário ou grupo à lista de administradores do escopo chamando o método [**IAzScope:: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .

Os repositórios de políticas baseados em XML não dão suporte à delegação em nenhum nível.

Um escopo dentro de um repositório de autorização armazenado no Active Directory não poderá ser delegado se o escopo contiver definições de tarefa que incluem regras de autorização ou definições de função que incluem regras de autorização.

O exemplo a seguir mostra como delegar a administração de um aplicativo. O exemplo supõe que haja um repositório de política de autorização de Active Directory existente no local especificado, que esse repositório de política contém um aplicativo denominado despesas e que este aplicativo não contém tarefas com scripts de regra de negócio.


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



 

 



