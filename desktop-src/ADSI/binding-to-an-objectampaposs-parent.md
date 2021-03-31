---
title: Associando ao pai de um objeto
description: Na ADSI, cada objeto de diretório é representado por um objeto COM ADSI que expõe a interface IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, associando ao pai de um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822234"
---
# <a name="binding-to-an-objects-parent"></a>Associando ao pai de um objeto

Na ADSI, cada objeto de diretório é representado por um objeto COM ADSI que expõe a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Para obter o contêiner pai de um objeto, use o método [**IADs:: get \_ pai**](iads-property-methods.md) para obter o ADsPath do objeto pai e, em seguida, associe ao ADsPath do pai.

O exemplo de código C++ a seguir mostra como obter o pai de um objeto.


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




