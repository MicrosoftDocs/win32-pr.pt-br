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
# <a name="unregistering-a-filter"></a><span data-ttu-id="6a2cc-103">Cancelando o registro de um filtro</span><span class="sxs-lookup"><span data-stu-id="6a2cc-103">Unregistering a Filter</span></span>

<span data-ttu-id="6a2cc-104">Para cancelar o registro de um filtro, implemente a função **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="6a2cc-105">Nessa função, chame a função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) do DirectShow com um valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="6a2cc-106">Se você tiver chamado **IFilterMapper2:: RegisterFilter** quando registrou o filtro, chame o método [**IFilterMapper2:: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) aqui.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="6a2cc-107">O exemplo a seguir mostra como cancelar o registro de um filtro:</span><span class="sxs-lookup"><span data-stu-id="6a2cc-107">The following example shows how to unregister a filter:</span></span>


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



 

 



