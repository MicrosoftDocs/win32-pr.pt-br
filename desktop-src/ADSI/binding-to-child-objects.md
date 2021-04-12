---
title: Associação a objetos filho
description: No ADSI, um objeto de contêiner expõe a interface IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associação a objetos filho
- Associação a objetos filho
- Objetos filho, associando a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454338"
---
# <a name="binding-to-child-objects"></a>Associação a objetos filho

No ADSI, um objeto de contêiner expõe a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . O método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) é usado para associar diretamente a um objeto filho. O objeto retornado por **IADsContainer:: GetObject** tem o mesmo contexto de segurança que o objeto no qual o método foi chamado. Isso significa que, se credenciais alternativas forem usadas, as credenciais alternativas não precisarão ser passadas para a função ou método de associação novamente para manter as mesmas credenciais.

O método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) usa um RDN (nome distinto relativo) relativo ao objeto atual. Esse método também usa um nome de classe opcional e retorna um ponteiro de interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que representa o objeto filho. Para obter a interface ADSI desejada, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), chame o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) desse ponteiro de interface **IDispatch** .

O exemplo de código C++ a seguir mostra uma função que recupera um objeto filho especificado.


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 