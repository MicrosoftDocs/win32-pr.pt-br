---
title: Uso de IADsExtension
description: Este tópico contém exemplos de código C++ para usar a interface IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159296"
---
# <a name="iadsextension-usage"></a><span data-ttu-id="f0d3f-104">Uso de IADsExtension</span><span class="sxs-lookup"><span data-stu-id="f0d3f-104">IADsExtension Usage</span></span>

<span data-ttu-id="f0d3f-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é uma interface opcional implementada pelo gravador de extensão quando pelo menos uma das seguintes condições é atendida:</span><span class="sxs-lookup"><span data-stu-id="f0d3f-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) is an optional interface implemented by the extension writer when at least one of the following conditions are met:</span></span>

-   <span data-ttu-id="f0d3f-106">O componente de extensão requer uma notificação de inicialização, conforme definido pelo **ADSI \_ ext \_ \* dwCode**\* no método [**Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="f0d3f-106">The extension component requires an initialization notification as defined by **ADSI\_EXT\_\*dwCode**\* in the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span>
-   <span data-ttu-id="f0d3f-107">A extensão dá suporte a uma interface dupla ou de expedição.</span><span class="sxs-lookup"><span data-stu-id="f0d3f-107">The extension supports a dual or dispatch interface.</span></span>

<span data-ttu-id="f0d3f-108">Se um componente de extensão oferecer suporte à interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pela primeira razão, os métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) poderão retornar **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="f0d3f-108">If an extension component supports the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for the first reason, the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**IADsExtension::PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods can return **E\_NOTIMPL**.</span></span> <span data-ttu-id="f0d3f-109">Como alternativa, se um componente de extensão oferecer suporte a uma interface dupla ou de expedição, o método [**opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) poderá ignorar os dados e retornar um **HRESULT** de **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="f0d3f-109">Alternatively, if an extension component supports a dual or dispatch interface , the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method can ignore the data and return an **HRESULT** of **E\_NOTIMPL**.</span></span>

<span data-ttu-id="f0d3f-110">O código a seguir mostra uma extensão que implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="f0d3f-110">The following code shows an extension implementing [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>


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



 

 




