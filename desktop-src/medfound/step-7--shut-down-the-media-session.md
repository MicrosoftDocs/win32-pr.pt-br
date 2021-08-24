---
description: Este tópico é a etapa 7 do tutorial Como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Etapa 7: Desligar sessão de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1eec6e798ee260c83fc1532c2012aed8a53625b12195848ac00fcdcf8fae3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721936"
---
# <a name="step-7-shut-down-the-media-session"></a>Etapa 7: Desligar sessão de mídia

Este tópico é a etapa 7 do tutorial Como reproduzir arquivos de [mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no tópico Exemplo de reprodução [de sessão de mídia](media-session-playback-example.md).

Para desligar a Sessão [de Mídia](media-session.md)do , execute as seguintes etapas:

1.  Chame [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a apresentação atual.
2.  Aguarde o [evento MESessionClosed.](mesessionclosed.md) Esse evento tem a garantia de ser o último evento da Sessão de Mídia.
3.  Chame [**IMFMediaSession::Shutdown.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) Esse método faz com que as Sessões de Mídia liberem recursos.
4.  Chame [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na fonte de mídia atual.

O método a seguir desliga a Sessão de Mídia. Ele usa um handle de evento (*m \_ hCloseEvent*) para aguardar o [evento MESessionClosed.](mesessionclosed.md) Consulte [Etapa 5: Manipular eventos de sessão de mídia.](step-5--handle-media-session-events.md)


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



Antes de o aplicativo ser encerrado, desligue a Sessão de Mídia e, em seguida, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a Microsoft Media Foundation plataforma.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



