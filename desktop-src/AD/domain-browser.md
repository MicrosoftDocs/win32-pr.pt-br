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
# <a name="domain-browser"></a><span data-ttu-id="5861f-104">Navegador de domínio</span><span class="sxs-lookup"><span data-stu-id="5861f-104">Domain Browser</span></span>

<span data-ttu-id="5861f-105">Usando a interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , um aplicativo pode exibir uma caixa de diálogo de navegador de domínio e obter o nome DNS do domínio selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5861f-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="5861f-106">Um aplicativo também pode usar a interface **IDsBrowseDomainTree** para obter dados sobre todos os domínios e árvores de domínio em uma floresta.</span><span class="sxs-lookup"><span data-stu-id="5861f-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="5861f-107">Uma instância da interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) é criada chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de **classe \_ DsDomainTreeBrowser do CLSID** , como mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="5861f-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="5861f-108">O método [**IDsBrowseDomainTree:: setcomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) pode ser usado para especificar quais computadores e credenciais são usados como base para recuperar os dados do domínio.</span><span class="sxs-lookup"><span data-stu-id="5861f-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="5861f-109">Quando **setcomputer** é chamado em uma instância [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) específica, [**IDsBrowseDomainTree:: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) deve ser chamado antes que **setcomputer** seja chamado novamente.</span><span class="sxs-lookup"><span data-stu-id="5861f-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="5861f-110">O método [**IDsBrowseDomainTree:: browseto**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) é usado para exibir a caixa de diálogo navegador de domínio.</span><span class="sxs-lookup"><span data-stu-id="5861f-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="5861f-111">Quando o usuário seleciona um domínio e clica no botão **OK** , **IDsBrowseDomainTree:: Browseto** retorna **S \_ OK** e o parâmetro *ppszTargetPath* contém o nome do domínio selecionado.</span><span class="sxs-lookup"><span data-stu-id="5861f-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="5861f-112">Quando a cadeia de caracteres de nome não é mais necessária, o chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="5861f-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="5861f-113">O exemplo de código a seguir mostra como usar a interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) para exibir a caixa de diálogo navegador de domínio.</span><span class="sxs-lookup"><span data-stu-id="5861f-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


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



<span data-ttu-id="5861f-114">O método [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) é usado para obter dados da árvore de domínio.</span><span class="sxs-lookup"><span data-stu-id="5861f-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="5861f-115">Os dados de domínio são fornecidos em uma estrutura [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) .</span><span class="sxs-lookup"><span data-stu-id="5861f-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="5861f-116">A estrutura **DOMAINTREE** contém o tamanho da estrutura e o número de elementos de domínio na árvore.</span><span class="sxs-lookup"><span data-stu-id="5861f-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="5861f-117">A estrutura **DOMAINTREE** também contém uma ou mais estruturas [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) .</span><span class="sxs-lookup"><span data-stu-id="5861f-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="5861f-118">O **DOMAINDESC** contém dados sobre um único elemento na árvore de domínio, incluindo dados filho e irmãos.</span><span class="sxs-lookup"><span data-stu-id="5861f-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="5861f-119">Os irmãos de um domínio podem ser enumerados acessando o membro **pdNextSibling** de cada estrutura de **DOMAINDESC** subsequente.</span><span class="sxs-lookup"><span data-stu-id="5861f-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="5861f-120">Os filhos do domínio podem ser recuperados de maneira semelhante, acessando o membro **pdChildList** de cada estrutura de **DOMAINDESC** subsequente.</span><span class="sxs-lookup"><span data-stu-id="5861f-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="5861f-121">O exemplo de código a seguir mostra como obter e acessar os dados da árvore de domínio usando o método [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .</span><span class="sxs-lookup"><span data-stu-id="5861f-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


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



 

 