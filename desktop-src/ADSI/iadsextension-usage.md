---
title: Uso de IADsExtension
description: Este tópico contém exemplos de código C++ para usar a interface IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab6813a87701fe2d7e130a03540476412c9e13b9d5d3ca96bdd0e63b2dad54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023484"
---
# <a name="iadsextension-usage"></a>Uso de IADsExtension

[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é uma interface opcional implementada pelo gravador de extensão quando pelo menos uma das seguintes condições é atendida:

-   O componente de extensão requer uma notificação de inicialização, conforme definido pelo **ADSI \_ ext \_ * dwCode*** no método [**Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .
-   A extensão dá suporte a uma interface dupla ou de expedição.

Se um componente de extensão oferecer suporte à interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pela primeira razão, os métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) poderão retornar **e \_ NOTIMPL**. Como alternativa, se um componente de extensão oferecer suporte a uma interface dupla ou de expedição, o método [**opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) poderá ignorar os dados e retornar um **HRESULT** de **E \_ NOTIMPL**.

O código a seguir mostra uma extensão que implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




