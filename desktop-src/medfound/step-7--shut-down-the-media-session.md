---
description: Este tópico é a etapa 7 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Etapa 7: desligar a sessão de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091890"
---
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="d912e-103">Etapa 7: desligar a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d912e-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="d912e-104">Este tópico é a etapa 7 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d912e-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="d912e-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="d912e-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="d912e-106">Para desligar a [sessão de mídia](media-session.md), execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d912e-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="d912e-107">Chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="d912e-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="d912e-108">Aguarde o evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="d912e-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="d912e-109">Esse evento é garantido como sendo o último evento da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d912e-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="d912e-110">Chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="d912e-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="d912e-111">Esse método faz com que as sessões de mídia liberem recursos.</span><span class="sxs-lookup"><span data-stu-id="d912e-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="d912e-112">Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na fonte de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d912e-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="d912e-113">O método a seguir desliga a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d912e-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="d912e-114">Ele usa um identificador de evento (*m \_ hCloseEvent*) para aguardar o evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="d912e-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="d912e-115">Consulte [Step 5: tratar eventos de sessão de mídia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="d912e-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



<span data-ttu-id="d912e-116">Antes de o aplicativo sair, desligue a sessão de mídia e, em seguida, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a plataforma de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d912e-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d912e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d912e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d912e-118">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="d912e-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="d912e-119">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d912e-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



