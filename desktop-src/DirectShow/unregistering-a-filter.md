---
description: Não registro de um filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Não registro de um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049676"
---
# <a name="unregistering-a-filter"></a>Não registro de um filtro

Para não fazer o registro de um filtro, implemente a **função DllUnregisterServer.** Dentro dessa função, chame a DirectShow [**função AMovieDllRegisterServer2**](amoviedllregisterserver2.md) com um valor **false**. Se você chamou **IFilterMapper2::RegisterFilter** quando registrou o filtro, chame o [**método IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) aqui.

O exemplo a seguir mostra como fazer o registro de um filtro:


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



