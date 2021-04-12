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
# <a name="step-5-add-video-functionality"></a>Etapa 5: adicionar a funcionalidade de vídeo

Este tópico é a etapa 5 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).

Para garantir que o vídeo seja exibido corretamente, o aplicativo deve responder às mensagens do [**WM \_ Paint**](../gdi/wm-paint.md), do [**WM \_ size**](../winmsg/wm-size.md)e do [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) da seguinte maneira.

### <a name="handle-wm_paint-messages"></a>Manipular mensagens do WM \_ Paint

Quando o aplicativo recebe uma mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) , o processador de vídeo pode precisar redesenhar o último quadro de vídeo. Para o filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ), chame [**IMFVideoDisplayControl:: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


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



Para o [filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9), chame [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


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



Para o [filtro do processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


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



### <a name="handle-wm_size-messages"></a>Manipular mensagens de tamanho do WM \_

Se o tamanho da janela de vídeo for alterado, notifique o renderizador de vídeo para redimensionar o vídeo. Para o EVR, chame [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


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



Para o VMR-9, chame [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


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



Para o VMR-7, chame [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


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



### <a name="handle-wm_displaychange-messages"></a>Manipular mensagens do WM \_ DISPLAYCHANGE

Se o modo de exibição for alterado, você deverá notificar o filtro VMR-9 ou VMR-7. Para o VMR-9, chame [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


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



Para o VMR-7, chame [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


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



O EVR não precisa ser notificado quando o modo de exibição é alterado.

Em seguida: [etapa 6: manipular eventos de grafo](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemplo de reprodução do DirectShow](directshow-playback-example.md)
</dt> <dt>

[Usando o filtro EVR do DirectShow](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
