---
description: Este tópico é a etapa 4 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Etapa 4: Adicionar o processador de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768778"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="78ea9-103">Etapa 4: Adicionar o processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="78ea9-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="78ea9-104">Este tópico é a etapa 4 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="78ea9-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="78ea9-106">O DirectShow fornece vários filtros diferentes que renderizam vídeo:</span><span class="sxs-lookup"><span data-stu-id="78ea9-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="78ea9-107">[**Filtro de processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="78ea9-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="78ea9-108">[Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="78ea9-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="78ea9-109">[Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="78ea9-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="78ea9-110">Para obter mais informações sobre as diferenças entre esses filtros, consulte [escolhendo o processador de vídeo correto](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="78ea9-111">Neste tutorial, cada filtro de processador de vídeo é encapsulado por uma classe que abstrai algumas das diferenças entre eles.</span><span class="sxs-lookup"><span data-stu-id="78ea9-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="78ea9-112">Todas essas classes derivam de uma classe base abstrata denominada `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="78ea9-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="78ea9-113">A declaração de `CVideoRenderer` é mostrada na [etapa 2: declare CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="78ea9-114">O método a seguir tenta criar cada processador de vídeo por vez, começando com o EVR, em seguida, o VMR-9 e, por fim, o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="78ea9-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


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



### <a name="evr-filter"></a><span data-ttu-id="78ea9-115">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="78ea9-115">EVR Filter</span></span>

<span data-ttu-id="78ea9-116">O código a seguir cria o filtro EVR e o adiciona ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="78ea9-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="78ea9-117">A função `AddFilterByCLSID` usada neste exemplo é mostrada no tópico [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


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



<span data-ttu-id="78ea9-118">A `InitializeEVR` função inicializa o filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="78ea9-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="78ea9-119">Essa função executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78ea9-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="78ea9-120">Consulta o filtro para a interface [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="78ea9-121">Chama [**IMFGetService:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="78ea9-122">Chama [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para definir a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="78ea9-123">Chama [**IMFVideoDisplayControl:: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) para configurar o EVR para preservar a taxa de proporção do vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="78ea9-124">O código a seguir mostra a `InitializeEVR` função.</span><span class="sxs-lookup"><span data-stu-id="78ea9-124">The following code shows the `InitializeEVR` function.</span></span>


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



<span data-ttu-id="78ea9-125">Depois que o grafo é compilado, as `DShowPlayer::RenderStreams` chamadas `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="78ea9-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="78ea9-126">Esse método executa qualquer inicialização ou limpeza final.</span><span class="sxs-lookup"><span data-stu-id="78ea9-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="78ea9-127">O código a seguir mostra a `CEVR` implementação desse método.</span><span class="sxs-lookup"><span data-stu-id="78ea9-127">The following code shows the `CEVR` implementation of this method.</span></span>


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



<span data-ttu-id="78ea9-128">Se o EVR não estiver conectado a nenhum outro filtro, esse método removerá o EVR do grafo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="78ea9-129">Isso pode ocorrer se o arquivo de mídia não contiver um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="78ea9-130">Filtro do VMR-9</span><span class="sxs-lookup"><span data-stu-id="78ea9-130">VMR-9 Filter</span></span>

<span data-ttu-id="78ea9-131">O código a seguir cria o filtro VMR-9 e o adiciona ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="78ea9-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


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



<span data-ttu-id="78ea9-132">A `InitWindowlessVMR9` função inicializa o VMR-9 para o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="78ea9-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="78ea9-133">(Para obter mais informações sobre o modo sem janela, consulte [modo sem janela do VMR](vmr-windowless-mode.md).) Essa função executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78ea9-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="78ea9-134">Consulta o filtro do VMR-9 para a interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="78ea9-135">Chama o método [**IVMRFilterConfig9:: Setrenderizamode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) para definir o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="78ea9-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="78ea9-136">Consulta o filtro do VMR-9 para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="78ea9-137">Chama o método [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) para definir a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="78ea9-138">Chama o método [**IVMRWindowlessControl9:: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) para preservar a taxa de proporção do vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="78ea9-139">O código a seguir mostra a `InitWindowlessVMR9` função.</span><span class="sxs-lookup"><span data-stu-id="78ea9-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


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



<span data-ttu-id="78ea9-140">O `CVMR9::FinalizeGraph` método verifica se o filtro do VMR-9 está conectado e, caso contrário, remove-o do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="78ea9-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


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



### <a name="vmr-7-filter"></a><span data-ttu-id="78ea9-141">Filtro do VMR-7</span><span class="sxs-lookup"><span data-stu-id="78ea9-141">VMR-7 Filter</span></span>

<span data-ttu-id="78ea9-142">As etapas para o filtro do VMR-7 são quase idênticas às do VMR-9, exceto que as interfaces do VMR-7 são usadas em vez disso.</span><span class="sxs-lookup"><span data-stu-id="78ea9-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="78ea9-143">O código a seguir cria o filtro VMR-7 e o adiciona ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="78ea9-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


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



<span data-ttu-id="78ea9-144">A `InitWindowlessVMR` função inicializa o VMR-7 para o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="78ea9-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="78ea9-145">Essa função executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78ea9-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="78ea9-146">Consulta o filtro do VMR-7 para a interface [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="78ea9-147">Chama o método [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) para definir o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="78ea9-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="78ea9-148">Consulta o filtro do VMR-7 para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="78ea9-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="78ea9-149">Chama o método [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para definir a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="78ea9-150">Chama o método [**IVMRWindowlessControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) para preservar a taxa de proporção do vídeo.</span><span class="sxs-lookup"><span data-stu-id="78ea9-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="78ea9-151">O código a seguir mostra a `InitWindowlessVMR` função.</span><span class="sxs-lookup"><span data-stu-id="78ea9-151">The following code shows the `InitWindowlessVMR` function.</span></span>


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



<span data-ttu-id="78ea9-152">O `CVMR7::FinalizeGraph` método verifica se o filtro do VMR-7 está conectado e, caso contrário, remove-o do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="78ea9-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="78ea9-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78ea9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ea9-154">Exemplo de reprodução do DirectShow</span><span class="sxs-lookup"><span data-stu-id="78ea9-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="78ea9-155">Usando o filtro EVR do DirectShow</span><span class="sxs-lookup"><span data-stu-id="78ea9-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="78ea9-156">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="78ea9-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
