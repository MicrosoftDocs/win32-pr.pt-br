---
title: Exemplo de código para alterar o escopo de um grupo
description: Este tópico contém código de exemplo para alterar o escopo de um grupo.
ms.assetid: 4ae61101-f123-44bd-8bec-bade51d22217
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, alterando o escopo de um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641ad43604785a6aae5bb250061ff0a3b62c294e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004930"
---
# <a name="example-code-for-changing-the-scope-of-a-group"></a><span data-ttu-id="44fb5-104">Exemplo de código para alterar o escopo de um grupo</span><span class="sxs-lookup"><span data-stu-id="44fb5-104">Example Code for Changing the Scope of a Group</span></span>

<span data-ttu-id="44fb5-105">O exemplo de código C++ a seguir altera o escopo de um grupo.</span><span class="sxs-lookup"><span data-stu-id="44fb5-105">The following C++ code example changes the scope of a group.</span></span>


```C++

    WCHAR *pwszLDAPPath = 
        L"LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com";
 
    HRESULT hr;
    IADsGroup * pGroup = NULL;
 
    // Initialize COM.
    CoInitialize(0);
 
    // Bind to the passed container. 
    hr = ADsGetObject( pwszLDAPPath, IID_IADsGroup,(void **)&pGroup);
 
    if (SUCCEEDED(hr))
    {
        VARIANT vValue;
        BSTR    bsValue = SysAllocString(L"groupType");
        VariantInit(&vValue);
    // Set a new GroupType Value.
        vValue.vt = VT_I4;
        vValue.lVal = ADS_GROUP_TYPE_GLOBAL_GROUP ;
 
        hr = pGroup->Put(bsValue,vValue);
        hr = pGroup->SetInfo();
        pGroup->Release();
        pGroup= NULL;
        SysFreeString(bsValue);
    }
 
    CoUninitialize();
```



<span data-ttu-id="44fb5-106">O exemplo de código a seguir Visual Basic altera o escopo de um grupo.</span><span class="sxs-lookup"><span data-stu-id="44fb5-106">The following Visual Basic code example changes the scope of a group.</span></span>


```VB
Dim x as IADs
On Error GoTo CleanUp
Set x = GetObject("LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com")
x.Put "groupType", 
    ADS_GROUP_TYPE_UNIVERSAL_GROUP|ADS_GROUP_TYPE_SECURITY_ENABLED
Exit Sub

CleanUp:
    MsgBox("An error has occurred.")
    x = Nothing
```



 

 




