---
title: Exemplo de código para pesquisar uma floresta
description: Este tópico contém um código de exemplo que pesquisa uma floresta.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, pesquisando uma floresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190283"
---
# <a name="example-code-for-searching-a-forest"></a>Exemplo de código para pesquisar uma floresta

Este tópico contém um código de exemplo que pesquisa uma floresta.

O exemplo de código C/C++ a seguir é associado à raiz do catálogo global e enumera o objeto único, que é a raiz da floresta, para que ele possa ser usado para Pesquisar toda a floresta.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



O exemplo de código C/C++ a seguir contém uma função que retorna um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usado para Pesquisar toda a floresta.

A função executa uma ligação sem servidor com a raiz do catálogo global, enumera o único item, que é a raiz da floresta e pode ser usado para Pesquisar toda a floresta, chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para o objeto e retorna esse ponteiro para ser usado pelo chamador para pesquisar a floresta.


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



 

 