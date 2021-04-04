---
title: Exemplo de código para associação ao contêiner do usuário
description: Este tópico inclui um exemplo de código que será associado ao contêiner de usuários no domínio atual e a interface de retorno e IADsContainer para o contêiner.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Active Directory exemplos Active Directory, associação ao contêiner do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db1ccb3d2331c4ccef5bbf28f58fa5c046337c7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007317"
---
# <a name="example-code-for-binding-to-the-users-container"></a><span data-ttu-id="366e4-104">Exemplo de código para associação ao contêiner do usuário</span><span class="sxs-lookup"><span data-stu-id="366e4-104">Example Code for Binding to the User's Container</span></span>

<span data-ttu-id="366e4-105">O exemplo de código C++ a seguir é associado ao contêiner de usuários no domínio atual e à interface de retorno e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="366e4-105">The following C++ code example binds to the users container in the current domain and return and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface for the container.</span></span> <span data-ttu-id="366e4-106">Para obter mais informações sobre associação a objetos conhecidos, consulte [Binding to Well-Known Objects using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="366e4-106">For more information about binding to well-known objects, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 