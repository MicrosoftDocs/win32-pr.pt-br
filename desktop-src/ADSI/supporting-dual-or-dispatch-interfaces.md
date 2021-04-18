---
title: Suporte a interfaces duplas ou de expedição
description: Assim como a interface de expedição, todas as interfaces duplas devem herdar de IDispatch, o que delega todas as suas funções de IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) de volta para o IDispatch do agregador (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Suporte a ADSI de interfaces duplas ou de expedição
- extensões ADSI, dual ou Dispatch interfaces
- ADSI ADSI, código de exemplo C/C++, delegando métodos IDispatch para o agregador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105756282"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="d261c-106">Suporte a interfaces duplas ou de expedição</span><span class="sxs-lookup"><span data-stu-id="d261c-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="d261c-107">Assim como a interface de expedição, todas as interfaces duplas devem herdar de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), o que delega todas as suas funções de **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GETTYPEINFOCOUNT**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) de volta para o **IDispatch** do agregador (ADSI).</span><span class="sxs-lookup"><span data-stu-id="d261c-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="d261c-108">Para delegar, um objeto de extensão deve consultar o **IDispatch** do agregador, chamar o método de agregador apropriado e liberar o ponteiro após o uso.</span><span class="sxs-lookup"><span data-stu-id="d261c-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="d261c-109">Se a extensão puder ser um componente autônomo, verifique se ele é agregado.</span><span class="sxs-lookup"><span data-stu-id="d261c-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="d261c-110">Nesse caso, redirecione as funções de expedição para o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do agregador, caso contrário, você pode chamar sua implementação interna de **IDispatch** ou pode chamar a implementação de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="d261c-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="d261c-111">O exemplo de código a seguir mostra como redirecionar a chamada [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para o **IDispatch** do agregador.</span><span class="sxs-lookup"><span data-stu-id="d261c-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="d261c-112">Este exemplo de código pressupõe que a variável de membro **m \_ pOuterUnknown** foi inicializada para o ponteiro **IUnknown** do agregador.</span><span class="sxs-lookup"><span data-stu-id="d261c-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



<span data-ttu-id="d261c-113">Os gravadores de extensão são altamente incentivados a dar suporte a interfaces duplas em vez de interfaces de expedição em seus objetos de extensão.</span><span class="sxs-lookup"><span data-stu-id="d261c-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="d261c-114">Uma interface dupla permite que um cliente tenha acesso mais rápido, desde que o acesso vtable esteja habilitado no cliente.</span><span class="sxs-lookup"><span data-stu-id="d261c-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="d261c-115">Para obter mais informações, consulte [associação tardia versus acesso vtable no modelo de extensão ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="d261c-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="d261c-116">Com base no modelo atual, a implementação de interfaces duplas não deve ser mais difícil do que a implementação de interfaces de expedição.</span><span class="sxs-lookup"><span data-stu-id="d261c-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 