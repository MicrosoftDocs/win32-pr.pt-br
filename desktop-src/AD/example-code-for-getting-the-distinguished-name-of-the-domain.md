---
title: Código de exemplo para obter o nome diferenciado do domínio
description: Este tópico inclui um exemplo de código que obtém o nome diferenciado do domínio do que o computador local é membro usando a associação sem servidor.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Exemplos do Active Directory do Active Directory, obter o nome diferenciado do domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693640"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Código de exemplo para obter o nome diferenciado do domínio

Este tópico inclui um exemplo de código que obtém o nome diferenciado do domínio do que o computador local é membro usando a associação sem servidor.

O exemplo Visual Basic código a seguir obtém o nome diferenciado do domínio do que o computador local é membro usando a associação sem servidor.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



O exemplo de código C# a seguir obtém o nome diferenciado do domínio do que o computador local é membro usando a associação sem servidor.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



O exemplo de código C/C++ a seguir obtém o nome diferenciado do domínio do que o computador local é membro usando a associação sem servidor.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




