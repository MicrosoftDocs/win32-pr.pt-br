---
description: Saiba mais sobre como obter um Ponteiro para o Objeto de Leitor do SDK Windows Media Format usando a interface IWMReaderAdvanced2 no DirectShow.
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Obtendo um ponteiro para o objeto Reader (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e131b9e111aa5e779d1208b68e04c9979e3b1d7f
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989102"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a><span data-ttu-id="57029-103">Obtendo um ponteiro para o objeto Reader (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="57029-103">Obtaining a Pointer to the Reader Object (DirectShow)</span></span>

<span data-ttu-id="57029-104">Em determinados casos, por exemplo, ao determinar quais extensões de unidade de dados são definidas em um determinado fluxo, talvez seja necessário acessar o Objeto de Leitor do SDK do Windows Media Format diretamente.</span><span class="sxs-lookup"><span data-stu-id="57029-104">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the Reader Object of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="57029-105">A função a seguir mostra como obter a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) no próprio Objeto de Leitor:</span><span class="sxs-lookup"><span data-stu-id="57029-105">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


```C++
#include <wmsdk.h>
HRESULT GetReaderAdvanced(IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. 
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;
      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



## <a name="related-topics"></a><span data-ttu-id="57029-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57029-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57029-107">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="57029-107">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
