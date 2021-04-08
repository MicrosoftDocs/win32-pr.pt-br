---
description: Cancelando o registro de um filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Cancelando o registro de um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829062"
---
# <a name="unregistering-a-filter"></a>Cancelando o registro de um filtro

Para cancelar o registro de um filtro, implemente a função **DllUnregisterServer** . Nessa função, chame a função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) do DirectShow com um valor de **false**. Se você tiver chamado **IFilterMapper2:: RegisterFilter** quando registrou o filtro, chame o método [**IFilterMapper2:: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) aqui.

O exemplo a seguir mostra como cancelar o registro de um filtro:


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



 

 



