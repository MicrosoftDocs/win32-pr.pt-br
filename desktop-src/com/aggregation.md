---
title: Agregação
description: A agregação é o mecanismo de reutilização de objeto no qual o objeto externo expõe interfaces do objeto interno como se elas estivessem implementadas no próprio objeto externo.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4855b1fa3a614d190b8f192aeee2e7cf3d3d53bbdce589a1363e0398f70430c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731716"
---
# <a name="aggregation"></a>Agregação

A agregação é o mecanismo de reutilização de objeto no qual o objeto externo expõe interfaces do objeto interno como se elas estivessem implementadas no próprio objeto externo. Isso é útil quando o objeto externo delega todas as chamadas para uma de suas interfaces para a mesma interface no objeto interno. A agregação está disponível como uma conveniência para evitar uma sobrecarga de implementação extra no objeto externo nesse caso. A agregação é, na verdade, um caso especializado de [contenção/delegação](containment-delegation.md).

A agregação é quase tão simples de implementar como confinamento, exceto para as três funções [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). O problema é que, da perspectiva do cliente, qualquer função **IUnknown** no objeto externo deve afetar o objeto externo. Ou seja, **AddRef** e **Release** afetam o objeto externo e **QueryInterface** expõe todas as interfaces disponíveis no objeto externo. No entanto, se o objeto externo simplesmente expõe a interface de um objeto interno como seu próprio, os membros **IUnknown** do objeto interno chamados por meio dessa interface se comportarão de forma diferente dos membros **IUnknown** nas interfaces do objeto externo, uma violação absoluta das regras e propriedades que governam **IUnknown**.

A solução é que a agregação requer uma implementação explícita de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) no objeto interno e a delegação dos métodos **IUnknown** de qualquer outra interface para os métodos **IUnknown** do objeto externo.

## <a name="creating-aggregable-objects"></a>Criando objetos Aggregable

A criação de objetos que podem ser agregados é opcional; no entanto, é simples fazer e fornecer benefícios significativos. As regras a seguir se aplicam à criação de um objeto aggregable:

-   A implementação do objeto aggregable (ou interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para sua interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controla a contagem de referência do objeto interno, e essa implementação não deve delegar ao desconhecido do objeto externo (o **IUnknown** de controle).
-   A implementação do objeto aggregable (ou interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para suas outras interfaces deve delegar ao [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle e não deve afetar diretamente a contagem de referência do objeto interno.
-   O [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interno deve implementar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) somente para o objeto interno.
-   O objeto aggregable não deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ao manter uma referência para o ponteiro de controle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .
-   Quando o objeto for criado, se qualquer interface diferente de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for solicitada, a criação deverá falhar com E \_ nointerface.

O fragmento de código a seguir ilustra uma implementação correta de um objeto aggregable usando o método de classe aninhado da implementação de interfaces:


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a>Agregando objetos

Ao desenvolver um objeto aggregable, as seguintes regras se aplicam:

-   Ao criar o objeto interno, o objeto externo deve solicitar explicitamente seu [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).
-   O objeto externo deve proteger sua implementação de [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) da reentrância com uma contagem de referência artificial em volta de seu código de destruição.
-   O objeto externo deve chamar seu método de liberação **de controle de** [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , caso ele consulte um ponteiro para qualquer uma das interfaces do objeto interno. Para liberar esse ponteiro, o objeto externo chama seu método  [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) de controle IUnknown, seguido por **Release** no ponteiro do objeto interno.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   O objeto externo não deve delegar indistintamente uma consulta para qualquer interface não reconhecida para o objeto interno, a menos que esse comportamento seja especificamente a intenção do objeto externo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contenção/delegação](containment-delegation.md)
</dt> </dl>

 

 