---
title: Exemplo de código para pesquisar uma floresta
description: Este tópico contém um código de exemplo que pesquisa uma floresta.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, pesquisando uma floresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c2fb0cde0f42167b19141ad178ea80ff8795b8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640406"
---
# <a name="example-code-for-searching-a-forest"></a><span data-ttu-id="36b3c-104">Exemplo de código para pesquisar uma floresta</span><span class="sxs-lookup"><span data-stu-id="36b3c-104">Example Code for Searching a Forest</span></span>

<span data-ttu-id="36b3c-105">Este tópico contém um código de exemplo que pesquisa uma floresta.</span><span class="sxs-lookup"><span data-stu-id="36b3c-105">This topic contains example code that searches a forest.</span></span>

<span data-ttu-id="36b3c-106">O exemplo de código C/C++ a seguir é associado à raiz do catálogo global e enumera o objeto único, que é a raiz da floresta, para que ele possa ser usado para Pesquisar toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="36b3c-106">The following C/C++ code example binds to the root of the Global Catalog and enumerates the single object, which is the root of the forest, so that it can be used to search the entire forest.</span></span>


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



<span data-ttu-id="36b3c-107">O exemplo de código C/C++ a seguir contém uma função que retorna um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usado para Pesquisar toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="36b3c-107">The following C/C++ code example contains a function that returns an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer used to search the entire forest.</span></span>

<span data-ttu-id="36b3c-108">A função executa uma ligação sem servidor com a raiz do catálogo global, enumera o único item, que é a raiz da floresta e pode ser usado para Pesquisar toda a floresta, chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para o objeto e retorna esse ponteiro para ser usado pelo chamador para pesquisar a floresta.</span><span class="sxs-lookup"><span data-stu-id="36b3c-108">The function performs a serverless bind to the root of the Global Catalog, enumerates the single item, which is the root of the forest and can be used to search the entire forest, calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to the object, and returns that pointer for use by the caller to search the forest.</span></span>


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 