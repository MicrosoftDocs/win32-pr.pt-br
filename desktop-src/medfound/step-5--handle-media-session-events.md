---
description: Este tópico é a etapa 5 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Etapa 5: manipular eventos de sessão de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105780406"
---
# <a name="step-5-handle-media-session-events"></a>Etapa 5: manipular eventos de sessão de mídia

Este tópico é a etapa 5 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.

Para obter informações sobre este tópico, leia [geradores de eventos de mídia](media-event-generators.md). Este tópico contém as seguintes seções:

-   [Obtendo eventos de sessão](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [Tópicos relacionados](#related-topics)

## <a name="getting-session-events"></a>Obtendo eventos de sessão

Para obter eventos da sessão de mídia, o objeto CPlayer chama o método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , conforme mostrado na [etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md). Esse método é assíncrono, o que significa que ele retorna ao chamador imediatamente. Quando ocorre o próximo evento de sessão, a sessão de mídia chama o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto CPlayer.

É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de um thread de trabalho, não do thread do aplicativo. Portanto, a implementação de **Invoke** deve ser multithread-safe. Uma abordagem seria proteger os dados do membro com uma seção crítica. No entanto, a `CPlayer` classe mostra uma abordagem alternativa:

1.  No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , o objeto CPlayer posta uma mensagem de **evento do WM \_ app \_ Player \_** para o aplicativo. O parâmetro Message é um ponteiro [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  O aplicativo recebe a mensagem de **evento do WM \_ app \_ Player \_** .
3.  O aplicativo chama o `CPlayer::HandleEvent` método, passando o ponteiro [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
4.  O `HandleEvent` método responde ao evento.

O código a seguir mostra o método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



O método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) executa as seguintes etapas:

1.  Chame [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obter o evento. Esse método retorna um ponteiro para a interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  Chame [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obter o código do evento.
3.  Se o código do evento for [MESessionClosed](mesessionclosed.md), chame unevent para definir o evento *m \_ hCloseEvent* . A razão para essa etapa é explicada na [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md)e também nos comentários de código.
4.  Para todos os outros códigos de evento, chame [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar o próximo evento.
5.  Poste uma mensagem de **evento do WM \_ app \_ Player \_** na janela.

O código a seguir mostra o método HandleEvent, que é chamado quando o aplicativo recebe a mensagem de **evento do WM \_ app \_ Player \_** :


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



Esse método chama [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obter o tipo de evento e [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obter o sucesso do código de falha associado ao evento. A próxima ação executada depende do código do evento.

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

O evento [MESessionTopologyStatus](mesessiontopologystatus.md) sinaliza uma alteração no status da topologia. O atributo de [**\_ status da \_ topologia \_ de evento MF**](mf-event-topology-status-attribute.md) do objeto de evento contém o status. Para este exemplo, o único valor de interesse é **MF \_ TOPOSTATUS \_ Ready**, que indica que a reprodução está pronta para ser iniciada.


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



O `CPlayer::StartPlayback` método é mostrado na [etapa 6: controle de reprodução](step-6--control-playback.md).

Este exemplo também chama [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) do [processador de vídeo aprimorado](enhanced-video-renderer.md) (EVR). Essa interface é necessária para lidar com a repintura e o redimensionamento da janela de vídeo, também mostradas na [etapa 6: controle de reprodução](step-6--control-playback.md).

## <a name="meendofpresentation"></a>MEEndOfPresentation

O evento [MEEndOfPresentation](meendofpresentation.md) sinaliza que a reprodução atingiu o final do arquivo. A sessão de mídia alterna automaticamente para o estado parado.


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

O evento [MENewPresentation](menewpresentation.md) sinaliza o início de uma nova apresentação. Os dados do evento são um ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para a nova apresentação.

Em muitos casos, você não receberá esse evento. Se você fizer isso, use o ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para criar uma nova topologia de reprodução, conforme mostrado na [etapa 3: abrir um arquivo de mídia](step-3--open-a-media-file.md). Em seguida, enfileirar a nova topologia na sessão de mídia.


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



Próximo: [etapa 6: controle de reprodução](step-6--control-playback.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



