---
title: Código de exemplo para obter o nome distinto do domínio
description: Este tópico inclui um exemplo de código que obtém o nome distinto do domínio do qual o computador local é membro usando a associação sem servidor.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory exemplos Active Directory, obtendo o nome distinto do domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159323"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a><span data-ttu-id="7a364-104">Código de exemplo para obter o nome distinto do domínio</span><span class="sxs-lookup"><span data-stu-id="7a364-104">Example Code for Getting the Distinguished Name of the Domain</span></span>

<span data-ttu-id="7a364-105">Este tópico inclui um exemplo de código que obtém o nome distinto do domínio do qual o computador local é membro usando a associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="7a364-105">This topic includes a code example that gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>

<span data-ttu-id="7a364-106">O exemplo de código a seguir Visual Basic Obtém o nome distinto do domínio do qual o computador local é membro usando a associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="7a364-106">The following Visual Basic code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



<span data-ttu-id="7a364-107">O exemplo de código C# a seguir obtém o nome distinto do domínio do qual o computador local é membro usando a associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="7a364-107">The following C# code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



<span data-ttu-id="7a364-108">O exemplo de código C/C++ a seguir obtém o nome distinto do domínio do qual o computador local é membro usando a associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="7a364-108">The following C/C++ code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


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



 

 




