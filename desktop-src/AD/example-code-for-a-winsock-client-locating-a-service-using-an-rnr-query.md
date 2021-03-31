---
title: Código de exemplo para localizar um serviço usando uma consulta RnR
description: O exemplo de código a seguir localiza o serviço Winsock de exemplo e se conecta a ele.
ms.assetid: c05c7f69-d510-4feb-b426-1ae3a3ed5e16
ms.tgt_platform: multiple
keywords:
- Código de exemplo para localizar um serviço usando um anúncio de consulta do RnR
- Registro do Windows Sockets, anúncio de resolução, código de exemplo, localizando um serviço usando uma consulta RnR
- Localizando um serviço usando um anúncio de consulta do RnR, código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1202c981de8b4f1e0bd4f4299b1aabf1be520d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634964"
---
# <a name="example-code-for-locating-a-service-using-an-rnr-query"></a><span data-ttu-id="06078-106">Código de exemplo para localizar um serviço usando uma consulta RnR</span><span class="sxs-lookup"><span data-stu-id="06078-106">Example Code for Locating a Service Using an RnR Query</span></span>

<span data-ttu-id="06078-107">O exemplo de código a seguir localiza o serviço Winsock de exemplo e se conecta a ele.</span><span class="sxs-lookup"><span data-stu-id="06078-107">The following code example locates the example Winsock service and connects to it.</span></span>


```C++
#include "stdafx.h"
#include "shlobj.h"
#include "dsclient.h"


//  The PrintDomain() function displays the domain name.
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;
    
    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//  The WalkDomainTree() function prints the current domain name and walks the tree.
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);
        
        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                dwIndentLevel + 1);
        }
    }
}

//  Entry point for the application.
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;

        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        
        pBrowseTree->Release();
    }
    
    CoUninitialize();
}
```



 

 




