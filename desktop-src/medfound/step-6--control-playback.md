---
description: Este tópico é a etapa 6 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Etapa 6: controle de reprodução'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827535"
---
# <a name="step-6-control-playback"></a>Etapa 6: controle de reprodução

Este tópico é a etapa 6 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.

Este tópico contém as seguintes seções:

-   [Iniciando reprodução](#starting-playback)
-   [Pausando reprodução](#pausing-playback)
-   [Parando a reprodução](#stopping-playback)
-   [Repintando a janela de vídeo](#repainting-the-video-window)
-   [Redimensionando a janela de vídeo](#resizing-the-video-window)
-   [Tópicos relacionados](#related-topics)

## <a name="starting-playback"></a>Iniciando reprodução

Para iniciar a reprodução, chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). O código a seguir mostra como iniciar a partir da posição de reprodução atual.


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



O método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) também pode especificar uma posição inicial relativa ao início do arquivo; consulte o tópico referência de API para obter mais informações.

## <a name="pausing-playback"></a>Pausando reprodução

Para pausar a reprodução, chame [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a>Parando a reprodução

Para parar a reprodução, chame [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Enquanto a reprodução é interrompida, a imagem de vídeo é desmarcada e a janela de vídeo é pintada com a cor do plano de fundo (preto por padrão).


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a>Repintando a janela de vídeo

O [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) desenha o vídeo na janela especificada pelo aplicativo. Isso ocorre em um thread separado e, para a maior parte, seu aplicativo não precisa gerenciar esse processo. No entanto, se a reprodução for pausada ou interrompida, o EVR deverá ser notificado sempre que a janela de vídeo receber uma mensagem de [**\_ pintura do WM**](../gdi/wm-paint.md) . Isso permite que o EVR repinte a janela. Para notificar o EVR, chame o método [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
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



O código a seguir mostra o manipulador da mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) . Essa função deve ser chamada do loop de mensagem do aplicativo.


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



O `HasVideo` método retornará **true** se o `CPlayer` objeto tiver um ponteiro [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) válido. (Consulte [a etapa 1: declarar a classe CPlayer](step-1--declare-the-cplayer-class.md).)


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Redimensionando a janela de vídeo

Se você redimensionar a janela de vídeo, atualize o retângulo de destino no EVR chamando o método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



Próximo: [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
