---
description: Este tópico é a etapa 2 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Etapa 2: declarar CVideoRenderer e classes derivadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780042"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="90f63-103">Etapa 2: declarar CVideoRenderer e classes derivadas</span><span class="sxs-lookup"><span data-stu-id="90f63-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="90f63-104">Este tópico é a etapa 2 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="90f63-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="90f63-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="90f63-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="90f63-106">O DirectShow fornece vários filtros diferentes que renderizam vídeo:</span><span class="sxs-lookup"><span data-stu-id="90f63-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="90f63-107">[**Filtro de processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="90f63-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="90f63-108">[Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="90f63-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="90f63-109">[Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="90f63-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="90f63-110">Para obter mais informações sobre as diferenças entre esses filtros, consulte [escolhendo o processador de vídeo correto](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="90f63-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="90f63-111">Neste tutorial, a seguinte classe abstrata é usada para encapsular o filtro de processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="90f63-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="90f63-112">Observações:</span><span class="sxs-lookup"><span data-stu-id="90f63-112">Notes:</span></span>

-   <span data-ttu-id="90f63-113">O `HasVideo` método retornará **true** se o processador de vídeo tiver sido criado.</span><span class="sxs-lookup"><span data-stu-id="90f63-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="90f63-114">O `AddToGraph` método adiciona o renderizador de vídeo ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="90f63-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="90f63-115">O `FinalizeGraph` método conclui a etapa de criação de grafo.</span><span class="sxs-lookup"><span data-stu-id="90f63-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="90f63-116">O `UpdateVideoWindow` método atualiza o retângulo de destino do vídeo.</span><span class="sxs-lookup"><span data-stu-id="90f63-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="90f63-117">O `Repaint` método redesenha o quadro de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="90f63-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="90f63-118">O `DisplayModeChanged` método manipula as alterações no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="90f63-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="90f63-119">Cada um desses métodos é descrito em detalhes posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="90f63-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="90f63-120">Em seguida, declare uma classe derivada para encapsular cada um dos três renderizadores de vídeo: o EVR, o VMR-9 e o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="90f63-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="90f63-121">Classe CEVR</span><span class="sxs-lookup"><span data-stu-id="90f63-121">CEVR Class</span></span>

<span data-ttu-id="90f63-122">A `CEVR` classe gerencia o EVR.</span><span class="sxs-lookup"><span data-stu-id="90f63-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="90f63-123">Ele contém um ponteiro para as interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) do EVR.</span><span class="sxs-lookup"><span data-stu-id="90f63-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="90f63-124">Classe CVMR9</span><span class="sxs-lookup"><span data-stu-id="90f63-124">CVMR9 Class</span></span>

<span data-ttu-id="90f63-125">A `CVMR9` classe gerencia o VMR-9.</span><span class="sxs-lookup"><span data-stu-id="90f63-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="90f63-126">Ele contém um ponteiro para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="90f63-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="90f63-127">Classe CVMR7</span><span class="sxs-lookup"><span data-stu-id="90f63-127">CVMR7 Class</span></span>

<span data-ttu-id="90f63-128">A `CVMR7` classe gerencia o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="90f63-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="90f63-129">Ele contém um ponteiro para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="90f63-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="90f63-130">Em seguida: [etapa 3: criar o grafo de filtro](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="90f63-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90f63-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90f63-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f63-132">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="90f63-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="90f63-133">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="90f63-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="90f63-134">Renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="90f63-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
