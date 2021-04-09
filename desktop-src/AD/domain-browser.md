---
title: Navegador de domínio
description: Usando a interface IDsBrowseDomainTree, um aplicativo pode exibir uma caixa de diálogo de navegador de domínio e obter o nome DNS do domínio selecionado pelo usuário.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- navegador de domínio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007321"
---
# <a name="domain-browser"></a>Navegador de domínio

Usando a interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , um aplicativo pode exibir uma caixa de diálogo de navegador de domínio e obter o nome DNS do domínio selecionado pelo usuário. Um aplicativo também pode usar a interface **IDsBrowseDomainTree** para obter dados sobre todos os domínios e árvores de domínio em uma floresta.

Uma instância da interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) é criada chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de **classe \_ DsDomainTreeBrowser do CLSID** , como mostrado abaixo.

O método [**IDsBrowseDomainTree:: setcomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) pode ser usado para especificar quais computadores e credenciais são usados como base para recuperar os dados do domínio. Quando **setcomputer** é chamado em uma instância [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) específica, [**IDsBrowseDomainTree:: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) deve ser chamado antes que **setcomputer** seja chamado novamente.

O método [**IDsBrowseDomainTree:: browseto**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) é usado para exibir a caixa de diálogo navegador de domínio. Quando o usuário seleciona um domínio e clica no botão **OK** , **IDsBrowseDomainTree:: Browseto** retorna **S \_ OK** e o parâmetro *ppszTargetPath* contém o nome do domínio selecionado. Quando a cadeia de caracteres de nome não é mais necessária, o chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

O exemplo de código a seguir mostra como usar a interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) para exibir a caixa de diálogo navegador de domínio.


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



O método [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) é usado para obter dados da árvore de domínio. Os dados de domínio são fornecidos em uma estrutura [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) . A estrutura **DOMAINTREE** contém o tamanho da estrutura e o número de elementos de domínio na árvore. A estrutura **DOMAINTREE** também contém uma ou mais estruturas [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) . O **DOMAINDESC** contém dados sobre um único elemento na árvore de domínio, incluindo dados filho e irmãos. Os irmãos de um domínio podem ser enumerados acessando o membro **pdNextSibling** de cada estrutura de **DOMAINDESC** subsequente. Os filhos do domínio podem ser recuperados de maneira semelhante, acessando o membro **pdChildList** de cada estrutura de **DOMAINDESC** subsequente.

O exemplo de código a seguir mostra como obter e acessar os dados da árvore de domínio usando o método [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
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

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
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

//  Entry point for application
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



 

 