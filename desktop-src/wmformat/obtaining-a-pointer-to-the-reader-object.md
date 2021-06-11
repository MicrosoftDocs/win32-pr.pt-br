---
title: Obtendo um ponteiro para o objeto Reader (Windows Media Format SDK 11)
description: Saiba mais sobre como obter um Ponteiro para o Objeto de Leitor do SDK Windows Media Format usando a interface IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, objetos de leitor
- Windows Media Format SDK, interface IWMReaderAdvanced2
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- FORMATO DE SISTEMAS Avançados (ASF), objetos de leitor
- ASF (Formato de Sistemas Avançados), objetos de leitor
- AsF (Advanced Systems Format), interface IWMReaderAdvanced2
- ASF (formato de sistemas avançados), interface IWMReaderAdvanced2
- DirectShow,Reader Objects
- DirectShow,ponteiros para objetos de leitor
- Interface DirectShow,IWMReaderAdvanced2
- objetos de leitor, obtendo ponteiros
- streams,Reader Objects
- fluxos, ponteiros para objetos de leitor
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd31bd868365b87b38eefd0c0c81e8beafef51c
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989131"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Obtendo um ponteiro para o objeto Reader (Windows Media Format SDK 11)

Em determinados casos, por exemplo, ao determinar quais extensões de unidade de [](reader-object.md) dados são definidas em um determinado fluxo, talvez seja necessário acessar o Objeto de Leitor do SDK do Windows Media Format diretamente. A função a seguir mostra como obter a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) no próprio Objeto de Leitor:


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



 

 




