---
title: Obtendo um ponteiro para o objeto leitor (SDK do Windows Media Format 11)
description: Obtendo um ponteiro para o objeto leitor
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, objetos do Reader
- SDK do Windows Media Format, interface IWMReaderAdvanced2
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), objetos de leitor
- ASF (formato de sistemas avançados), objetos de leitor
- Formato de sistema avançado (ASF), interface IWMReaderAdvanced2
- ASF (formato de sistemas avançados), interface IWMReaderAdvanced2
- DirectShow, objetos de leitor
- DirectShow, ponteiros para objetos de leitor
- DirectShow, interface IWMReaderAdvanced2
- objetos de leitor, obtendo ponteiros
- fluxos, objetos de leitor
- fluxos, ponteiros para objetos do leitor
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e0bb6611ba1d4e3c41fb2c00a68dd9c898505f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294705"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="d0afa-119">Obtendo um ponteiro para o objeto leitor (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="d0afa-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d0afa-120">Em determinados casos, por exemplo, ao determinar quais extensões de unidade de dados são definidas em um determinado fluxo, talvez seja necessário acessar o [objeto leitor](reader-object.md) do SDK do Windows Media Format diretamente.</span><span class="sxs-lookup"><span data-stu-id="d0afa-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="d0afa-121">A função a seguir mostra como obter a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) no próprio objeto Reader:</span><span class="sxs-lookup"><span data-stu-id="d0afa-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
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
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
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



 

 




