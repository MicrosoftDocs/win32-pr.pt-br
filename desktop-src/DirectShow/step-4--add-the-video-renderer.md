---
description: Este tópico é a etapa 4 do tutorial de reprodução de áudio/vídeo em DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Etapa 4: Adicionar o processador de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2d73dce5bba34f92c8df59cd9730ef1e25b57b9757039d9bda5c2e4432d734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051406"
---
# <a name="step-4-add-the-video-renderer"></a>Etapa 4: Adicionar o processador de vídeo

Este tópico é a etapa 4 do tutorial de [reprodução de áudio/vídeo em DirectShow](audio-video-playback-in-directshow.md). o código completo é mostrado no tópico [DirectShow exemplo de reprodução](directshow-playback-example.md).

DirectShow fornece vários filtros diferentes que renderizam vídeo:

-   [**Filtro de processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR)
-   [Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Para obter mais informações sobre as diferenças entre esses filtros, consulte [escolhendo o processador de vídeo correto](choosing-the-right-renderer.md).

Neste tutorial, cada filtro de processador de vídeo é encapsulado por uma classe que abstrai algumas das diferenças entre eles. Todas essas classes derivam de uma classe base abstrata denominada `CVideoRenderer` . A declaração de `CVideoRenderer` é mostrada na [etapa 2: declare CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).

O método a seguir tenta criar cada processador de vídeo por vez, começando com o EVR, em seguida, o VMR-9 e, por fim, o VMR-7.


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a>Filtro de EVR

O código a seguir cria o filtro EVR e o adiciona ao gráfico de filtro. A função `AddFilterByCLSID` usada neste exemplo é mostrada no tópico [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md).


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



A `InitializeEVR` função inicializa o filtro EVR. Essa função executa as etapas a seguir.

1.  Consulta o filtro para a interface [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .
2.  Chama [**IMFGetService:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .
3.  Chama [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para definir a janela de vídeo.
4.  Chama [**IMFVideoDisplayControl:: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) para configurar o EVR para preservar a taxa de proporção do vídeo.

O código a seguir mostra a `InitializeEVR` função.


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



Depois que o grafo é compilado, as `DShowPlayer::RenderStreams` chamadas `CVideoRenderer::FinalizeGraph` . Esse método executa qualquer inicialização ou limpeza final. O código a seguir mostra a `CEVR` implementação desse método.


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



Se o EVR não estiver conectado a nenhum outro filtro, esse método removerá o EVR do grafo. Isso pode ocorrer se o arquivo de mídia não contiver um fluxo de vídeo.

### <a name="vmr-9-filter"></a>Filtro do VMR-9

O código a seguir cria o filtro VMR-9 e o adiciona ao gráfico de filtro.


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



A `InitWindowlessVMR9` função inicializa o VMR-9 para o modo sem janela. (Para obter mais informações sobre o modo sem janela, consulte [modo sem janela do VMR](vmr-windowless-mode.md).) Essa função executa as etapas a seguir.

1.  Consulta o filtro do VMR-9 para a interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
2.  Chama o método [**IVMRFilterConfig9:: Setrenderizamode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) para definir o modo sem janela.
3.  Consulta o filtro do VMR-9 para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
4.  Chama o método [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) para definir a janela de vídeo.
5.  Chama o método [**IVMRWindowlessControl9:: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) para preservar a taxa de proporção do vídeo.

O código a seguir mostra a `InitWindowlessVMR9` função.


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



O `CVMR9::FinalizeGraph` método verifica se o filtro do VMR-9 está conectado e, caso contrário, remove-o do grafo de filtro.


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a>Filtro do VMR-7

As etapas para o filtro do VMR-7 são quase idênticas às do VMR-9, exceto que as interfaces do VMR-7 são usadas em vez disso. O código a seguir cria o filtro VMR-7 e o adiciona ao gráfico de filtro.


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



A `InitWindowlessVMR` função inicializa o VMR-7 para o modo sem janela. Essa função executa as etapas a seguir.

1.  Consulta o filtro do VMR-7 para a interface [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .
2.  Chama o método [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) para definir o modo sem janela.
3.  Consulta o filtro do VMR-7 para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
4.  Chama o método [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para definir a janela de vídeo.
5.  Chama o método [**IVMRWindowlessControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) para preservar a taxa de proporção do vídeo.

O código a seguir mostra a `InitWindowlessVMR` função.


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



O `CVMR7::FinalizeGraph` método verifica se o filtro do VMR-7 está conectado e, caso contrário, remove-o do grafo de filtro.


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Exemplo de reprodução](directshow-playback-example.md)
</dt> <dt>

[usando o filtro de EVR de DirectShow](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
