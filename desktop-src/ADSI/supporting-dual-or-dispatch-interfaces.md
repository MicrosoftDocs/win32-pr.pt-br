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
ms.openlocfilehash: b783e9448926d6d29a27e5fb0db519175f82a9af1935e9f13655db743a946bcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930006"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Suporte a interfaces duplas ou de expedição

Assim como a interface de expedição, todas as interfaces duplas devem herdar de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), o que delega todas as suas funções de **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GETTYPEINFOCOUNT**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) de volta para o **IDispatch** do agregador (ADSI). Para delegar, um objeto de extensão deve consultar o **IDispatch** do agregador, chamar o método de agregador apropriado e liberar o ponteiro após o uso.

Se a extensão puder ser um componente autônomo, verifique se ele é agregado. Nesse caso, redirecione as funções de expedição para o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do agregador, caso contrário, você pode chamar sua implementação interna de **IDispatch** ou pode chamar a implementação de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

O exemplo de código a seguir mostra como redirecionar a chamada [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para o **IDispatch** do agregador. Este exemplo de código pressupõe que a variável de membro **m \_ pOuterUnknown** foi inicializada para o ponteiro **IUnknown** do agregador.


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



Os gravadores de extensão são altamente incentivados a dar suporte a interfaces duplas em vez de interfaces de expedição em seus objetos de extensão. Uma interface dupla permite que um cliente tenha acesso mais rápido, desde que o acesso vtable esteja habilitado no cliente. Para obter mais informações, consulte [associação tardia versus acesso vtable no modelo de extensão ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). Com base no modelo atual, a implementação de interfaces duplas não deve ser mais difícil do que a implementação de interfaces de expedição.

 

 