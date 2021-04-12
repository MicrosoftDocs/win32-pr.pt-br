---
title: Agregação
description: A agregação é o mecanismo de reutilização de objeto no qual o objeto externo expõe interfaces do objeto interno como se elas estivessem implementadas no próprio objeto externo.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294526"
---
# <a name="aggregation"></a><span data-ttu-id="e902b-103">Agregação</span><span class="sxs-lookup"><span data-stu-id="e902b-103">Aggregation</span></span>

<span data-ttu-id="e902b-104">A agregação é o mecanismo de reutilização de objeto no qual o objeto externo expõe interfaces do objeto interno como se elas estivessem implementadas no próprio objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e902b-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="e902b-105">Isso é útil quando o objeto externo delega todas as chamadas para uma de suas interfaces para a mesma interface no objeto interno.</span><span class="sxs-lookup"><span data-stu-id="e902b-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="e902b-106">A agregação está disponível como uma conveniência para evitar uma sobrecarga de implementação extra no objeto externo nesse caso.</span><span class="sxs-lookup"><span data-stu-id="e902b-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="e902b-107">A agregação é, na verdade, um caso especializado de [contenção/delegação](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="e902b-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="e902b-108">A agregação é quase tão simples de implementar como confinamento, exceto para as três funções [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="e902b-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="e902b-109">O problema é que, da perspectiva do cliente, qualquer função **IUnknown** no objeto externo deve afetar o objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e902b-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="e902b-110">Ou seja, **AddRef** e **Release** afetam o objeto externo e **QueryInterface** expõe todas as interfaces disponíveis no objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e902b-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="e902b-111">No entanto, se o objeto externo simplesmente expõe a interface de um objeto interno como seu próprio, os membros **IUnknown** do objeto interno chamados por meio dessa interface se comportarão de forma diferente dos membros **IUnknown** nas interfaces do objeto externo, uma violação absoluta das regras e propriedades que governam **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e902b-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="e902b-112">A solução é que a agregação requer uma implementação explícita de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) no objeto interno e a delegação dos métodos **IUnknown** de qualquer outra interface para os métodos **IUnknown** do objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e902b-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="e902b-113">Criando objetos Aggregable</span><span class="sxs-lookup"><span data-stu-id="e902b-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="e902b-114">A criação de objetos que podem ser agregados é opcional; no entanto, é simples fazer e fornecer benefícios significativos.</span><span class="sxs-lookup"><span data-stu-id="e902b-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="e902b-115">As regras a seguir se aplicam à criação de um objeto aggregable:</span><span class="sxs-lookup"><span data-stu-id="e902b-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="e902b-116">A implementação do objeto aggregable (ou interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para sua interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controla a contagem de referência do objeto interno, e essa implementação não deve delegar ao desconhecido do objeto externo (o **IUnknown** de controle).</span><span class="sxs-lookup"><span data-stu-id="e902b-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="e902b-117">A implementação do objeto aggregable (ou interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para suas outras interfaces deve delegar ao [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle e não deve afetar diretamente a contagem de referência do objeto interno.</span><span class="sxs-lookup"><span data-stu-id="e902b-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="e902b-118">O [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interno deve implementar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) somente para o objeto interno.</span><span class="sxs-lookup"><span data-stu-id="e902b-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="e902b-119">O objeto aggregable não deve chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ao manter uma referência para o ponteiro de controle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e902b-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="e902b-120">Quando o objeto for criado, se qualquer interface diferente de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for solicitada, a criação deverá falhar com E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="e902b-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="e902b-121">O fragmento de código a seguir ilustra uma implementação correta de um objeto aggregable usando o método de classe aninhado da implementação de interfaces:</span><span class="sxs-lookup"><span data-stu-id="e902b-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


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



## <a name="aggregating-objects"></a><span data-ttu-id="e902b-122">Agregando objetos</span><span class="sxs-lookup"><span data-stu-id="e902b-122">Aggregating Objects</span></span>

<span data-ttu-id="e902b-123">Ao desenvolver um objeto aggregable, as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="e902b-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="e902b-124">Ao criar o objeto interno, o objeto externo deve solicitar explicitamente seu [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="e902b-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="e902b-125">O objeto externo deve proteger sua implementação de [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) da reentrância com uma contagem de referência artificial em volta de seu código de destruição.</span><span class="sxs-lookup"><span data-stu-id="e902b-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="e902b-126">O objeto externo deve chamar seu método de liberação **de controle de** [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , caso ele consulte um ponteiro para qualquer uma das interfaces do objeto interno.</span><span class="sxs-lookup"><span data-stu-id="e902b-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="e902b-127">Para liberar esse ponteiro, o objeto externo chama seu método  [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) de controle IUnknown, seguido por **Release** no ponteiro do objeto interno.</span><span class="sxs-lookup"><span data-stu-id="e902b-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="e902b-128">O objeto externo não deve delegar indistintamente uma consulta para qualquer interface não reconhecida para o objeto interno, a menos que esse comportamento seja especificamente a intenção do objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e902b-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e902b-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e902b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e902b-130">Contenção/delegação</span><span class="sxs-lookup"><span data-stu-id="e902b-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 