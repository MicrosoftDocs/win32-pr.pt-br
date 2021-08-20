---
description: Este tópico é a etapa 5 do tutorial Reprodução de áudio/vídeo DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Etapa 5: Adicionar funcionalidade de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951775"
---
# <a name="step-5-add-video-functionality"></a>Etapa 5: Adicionar funcionalidade de vídeo

Este tópico é a etapa 5 do tutorial [Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no tópico DirectShow [Exemplo de Reprodução](directshow-playback-example.md).

Para garantir que o vídeo seja exibido corretamente, o aplicativo deve responder às mensagens [**WM \_ PAINT,**](../gdi/wm-paint.md) [**WM \_ SIZE**](../winmsg/wm-size.md)e [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) da seguinte maneira.

### <a name="handle-wm_paint-messages"></a>Manipular mensagens WM \_ PAINT

Quando o aplicativo recebe uma mensagem [**WM \_ PAINT,**](../gdi/wm-paint.md) o renderador de vídeo pode precisar redesenhar o último quadro de vídeo. Para o [**filtro EVR (Renderização**](enhanced-video-renderer-filter.md) de Vídeo Aprimorado), chame [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


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



Para o [filtro de renderização](video-mixing-renderer-filter-9.md) de combinação de vídeo 9 (VMR-9), chame [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


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



Para o [Filtro de Renderização](video-mixing-renderer-filter-7.md) de Combinação de Vídeo 7 (VMR-7), chame [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


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



### <a name="handle-wm_size-messages"></a>Manipular mensagens WM \_ SIZE

Se o tamanho da janela de vídeo mudar, notifique o renderador de vídeo para reutilizar o vídeo. Para o EVR, chame [**IMFVideoDisplayControl::SetVideoPosition.**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)


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



Para a VMR-9, chame [**IVMRWindowlessControl9::SetVideoPosition.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)


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



Para a VMR-7, chame [**IVMRWindowlessControl::SetVideoPosition.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition)


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



### <a name="handle-wm_displaychange-messages"></a>Manipular mensagens \_ DISPLAYCHANGE wm

Se o modo de exibição mudar, você deverá notificar o filtro VMR-9 ou VMR-7. Para a VMR-9, chame [**IVMRWindowlessControl9::D isplayModeChanged.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)


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



Para a VMR-7, chame [**IVMRWindowlessControl::D isplayModeChanged.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)


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



O EVR não precisa ser notificado quando o modo de exibição muda.

Próximo: [Etapa 6: manipular Graph eventos](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Exemplo de reprodução](directshow-playback-example.md)
</dt> <dt>

[Usando o filtro DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Usando o renderador de combinação de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
