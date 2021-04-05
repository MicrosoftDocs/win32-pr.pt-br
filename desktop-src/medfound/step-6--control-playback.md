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
# <a name="step-6-control-playback"></a><span data-ttu-id="b4f2c-103">Etapa 6: controle de reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-103">Step 6: Control Playback</span></span>

<span data-ttu-id="b4f2c-104">Este tópico é a etapa 6 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="b4f2c-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="b4f2c-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="b4f2c-106">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b4f2c-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b4f2c-107">Iniciando reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="b4f2c-108">Pausando reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="b4f2c-109">Parando a reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="b4f2c-110">Repintando a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4f2c-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="b4f2c-111">Redimensionando a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4f2c-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="b4f2c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4f2c-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="b4f2c-113">Iniciando reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-113">Starting Playback</span></span>

<span data-ttu-id="b4f2c-114">Para iniciar a reprodução, chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="b4f2c-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="b4f2c-115">O código a seguir mostra como iniciar a partir da posição de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-115">The following code shows how to start from the current playback position.</span></span>


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



<span data-ttu-id="b4f2c-116">O método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) também pode especificar uma posição inicial relativa ao início do arquivo; consulte o tópico referência de API para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="b4f2c-117">Pausando reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-117">Pausing Playback</span></span>

<span data-ttu-id="b4f2c-118">Para pausar a reprodução, chame [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="b4f2c-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


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



## <a name="stopping-playback"></a><span data-ttu-id="b4f2c-119">Parando a reprodução</span><span class="sxs-lookup"><span data-stu-id="b4f2c-119">Stopping Playback</span></span>

<span data-ttu-id="b4f2c-120">Para parar a reprodução, chame [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="b4f2c-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="b4f2c-121">Enquanto a reprodução é interrompida, a imagem de vídeo é desmarcada e a janela de vídeo é pintada com a cor do plano de fundo (preto por padrão).</span><span class="sxs-lookup"><span data-stu-id="b4f2c-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


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



## <a name="repainting-the-video-window"></a><span data-ttu-id="b4f2c-122">Repintando a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4f2c-122">Repainting the Video Window</span></span>

<span data-ttu-id="b4f2c-123">O [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) desenha o vídeo na janela especificada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="b4f2c-124">Isso ocorre em um thread separado e, para a maior parte, seu aplicativo não precisa gerenciar esse processo.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="b4f2c-125">No entanto, se a reprodução for pausada ou interrompida, o EVR deverá ser notificado sempre que a janela de vídeo receber uma mensagem de [**\_ pintura do WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f2c-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="b4f2c-126">Isso permite que o EVR repinte a janela.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="b4f2c-127">Para notificar o EVR, chame o método [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :</span><span class="sxs-lookup"><span data-stu-id="b4f2c-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


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



<span data-ttu-id="b4f2c-128">O código a seguir mostra o manipulador da mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f2c-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="b4f2c-129">Essa função deve ser chamada do loop de mensagem do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-129">This function should be called from the application's message loop.</span></span>


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



<span data-ttu-id="b4f2c-130">O `HasVideo` método retornará **true** se o `CPlayer` objeto tiver um ponteiro [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) válido.</span><span class="sxs-lookup"><span data-stu-id="b4f2c-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="b4f2c-131">(Consulte [a etapa 1: declarar a classe CPlayer](step-1--declare-the-cplayer-class.md).)</span><span class="sxs-lookup"><span data-stu-id="b4f2c-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="b4f2c-132">Redimensionando a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="b4f2c-132">Resizing the Video Window</span></span>

<span data-ttu-id="b4f2c-133">Se você redimensionar a janela de vídeo, atualize o retângulo de destino no EVR chamando o método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :</span><span class="sxs-lookup"><span data-stu-id="b4f2c-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


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



<span data-ttu-id="b4f2c-134">Próximo: [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="b4f2c-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4f2c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4f2c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4f2c-136">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="b4f2c-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="b4f2c-137">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4f2c-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
