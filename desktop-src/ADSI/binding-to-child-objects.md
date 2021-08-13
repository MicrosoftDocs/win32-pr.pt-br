---
title: Associação a objetos filho
description: No ADSI, um objeto de contêiner expõe a interface IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , usando, associação a objetos filho
- Associação a objetos filho
- Objetos filho, associação a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e454da1aaea93acc404e92da4b9c45ac8d67b4c3cee8a4fe9a04027c7533b39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429033"
---
# <a name="binding-to-child-objects"></a>Associação a objetos filho

No ADSI, um objeto de contêiner expõe a interface [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) O [**método IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) é usado para se vincular diretamente a um objeto filho. O objeto retornado por **IADsContainer::GetObject** tem o mesmo contexto de segurança que o objeto no qual o método foi chamado. Isso significa que, se credenciais alternativas são usadas, as credenciais alternativas não devem ser passadas para a função de associação ou método novamente para manter as mesmas credenciais.

O [**método IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) recebe um RDN (nome diferenciado relativo) relativo relativo ao objeto atual. Esse método também recebe um nome de classe opcional e retorna um ponteiro de interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que representa o objeto filho. Para obter a interface ADSI desejada, como [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads)chame o [**método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) deste ponteiro de interface **IDispatch.**

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



 

 