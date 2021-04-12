---
description: Este tópico é a etapa 5 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Etapa 5: adicionar a funcionalidade de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170970"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="0a0a3-103">Etapa 5: adicionar a funcionalidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a0a3-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="0a0a3-104">Este tópico é a etapa 5 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="0a0a3-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="0a0a3-106">Para garantir que o vídeo seja exibido corretamente, o aplicativo deve responder às mensagens do [**WM \_ Paint**](../gdi/wm-paint.md), do [**WM \_ size**](../winmsg/wm-size.md)e do [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0a0a3-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="0a0a3-107">Manipular mensagens do WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="0a0a3-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="0a0a3-108">Quando o aplicativo recebe uma mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) , o processador de vídeo pode precisar redesenhar o último quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a0a3-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="0a0a3-109">Para o filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ), chame [**IMFVideoDisplayControl:: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="0a0a3-110">Para o [filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9), chame [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="0a0a3-111">Para o [filtro do processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a><span data-ttu-id="0a0a3-112">Manipular mensagens de tamanho do WM \_</span><span class="sxs-lookup"><span data-stu-id="0a0a3-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="0a0a3-113">Se o tamanho da janela de vídeo for alterado, notifique o renderizador de vídeo para redimensionar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a0a3-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="0a0a3-114">Para o EVR, chame [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="0a0a3-115">Para o VMR-9, chame [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="0a0a3-116">Para o VMR-7, chame [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="0a0a3-117">Manipular mensagens do WM \_ DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a0a3-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="0a0a3-118">Se o modo de exibição for alterado, você deverá notificar o filtro VMR-9 ou VMR-7.</span><span class="sxs-lookup"><span data-stu-id="0a0a3-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="0a0a3-119">Para o VMR-9, chame [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="0a0a3-120">Para o VMR-7, chame [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="0a0a3-121">O EVR não precisa ser notificado quando o modo de exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="0a0a3-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="0a0a3-122">Em seguida: [etapa 6: manipular eventos de grafo](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="0a0a3-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0a3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a0a3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0a3-124">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a0a3-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0a0a3-125">Exemplo de reprodução do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a0a3-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="0a0a3-126">Usando o filtro EVR do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a0a3-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="0a0a3-127">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a0a3-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
