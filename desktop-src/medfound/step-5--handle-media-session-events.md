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
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="bcfc0-103">Etapa 5: manipular eventos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="bcfc0-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="bcfc0-104">Este tópico é a etapa 5 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="bcfc0-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="bcfc0-106">Para obter informações sobre este tópico, leia [geradores de eventos de mídia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="bcfc0-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="bcfc0-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bcfc0-108">Obtendo eventos de sessão</span><span class="sxs-lookup"><span data-stu-id="bcfc0-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="bcfc0-109">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="bcfc0-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="bcfc0-110">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="bcfc0-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="bcfc0-111">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="bcfc0-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="bcfc0-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcfc0-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="bcfc0-113">Obtendo eventos de sessão</span><span class="sxs-lookup"><span data-stu-id="bcfc0-113">Getting Session Events</span></span>

<span data-ttu-id="bcfc0-114">Para obter eventos da sessão de mídia, o objeto CPlayer chama o método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , conforme mostrado na [etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="bcfc0-115">Esse método é assíncrono, o que significa que ele retorna ao chamador imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="bcfc0-116">Quando ocorre o próximo evento de sessão, a sessão de mídia chama o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto CPlayer.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="bcfc0-117">É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de um thread de trabalho, não do thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="bcfc0-118">Portanto, a implementação de **Invoke** deve ser multithread-safe.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="bcfc0-119">Uma abordagem seria proteger os dados do membro com uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="bcfc0-120">No entanto, a `CPlayer` classe mostra uma abordagem alternativa:</span><span class="sxs-lookup"><span data-stu-id="bcfc0-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="bcfc0-121">No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , o objeto CPlayer posta uma mensagem de **evento do WM \_ app \_ Player \_** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="bcfc0-122">O parâmetro Message é um ponteiro [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="bcfc0-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="bcfc0-123">O aplicativo recebe a mensagem de **evento do WM \_ app \_ Player \_** .</span><span class="sxs-lookup"><span data-stu-id="bcfc0-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="bcfc0-124">O aplicativo chama o `CPlayer::HandleEvent` método, passando o ponteiro [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="bcfc0-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="bcfc0-125">O `HandleEvent` método responde ao evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="bcfc0-126">O código a seguir mostra o método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="bcfc0-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


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



<span data-ttu-id="bcfc0-127">O método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="bcfc0-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="bcfc0-128">Chame [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obter o evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="bcfc0-129">Esse método retorna um ponteiro para a interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="bcfc0-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="bcfc0-130">Chame [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obter o código do evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="bcfc0-131">Se o código do evento for [MESessionClosed](mesessionclosed.md), chame unevent para definir o evento *m \_ hCloseEvent* .</span><span class="sxs-lookup"><span data-stu-id="bcfc0-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="bcfc0-132">A razão para essa etapa é explicada na [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md)e também nos comentários de código.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="bcfc0-133">Para todos os outros códigos de evento, chame [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar o próximo evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="bcfc0-134">Poste uma mensagem de **evento do WM \_ app \_ Player \_** na janela.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="bcfc0-135">O código a seguir mostra o método HandleEvent, que é chamado quando o aplicativo recebe a mensagem de **evento do WM \_ app \_ Player \_** :</span><span class="sxs-lookup"><span data-stu-id="bcfc0-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


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



<span data-ttu-id="bcfc0-136">Esse método chama [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obter o tipo de evento e [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obter o sucesso do código de falha associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="bcfc0-137">A próxima ação executada depende do código do evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="bcfc0-138">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="bcfc0-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="bcfc0-139">O evento [MESessionTopologyStatus](mesessiontopologystatus.md) sinaliza uma alteração no status da topologia.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="bcfc0-140">O atributo de [**\_ status da \_ topologia \_ de evento MF**](mf-event-topology-status-attribute.md) do objeto de evento contém o status.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="bcfc0-141">Para este exemplo, o único valor de interesse é **MF \_ TOPOSTATUS \_ Ready**, que indica que a reprodução está pronta para ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


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



<span data-ttu-id="bcfc0-142">O `CPlayer::StartPlayback` método é mostrado na [etapa 6: controle de reprodução](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="bcfc0-143">Este exemplo também chama [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) do [processador de vídeo aprimorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="bcfc0-144">Essa interface é necessária para lidar com a repintura e o redimensionamento da janela de vídeo, também mostradas na [etapa 6: controle de reprodução](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="bcfc0-145">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="bcfc0-145">MEEndOfPresentation</span></span>

<span data-ttu-id="bcfc0-146">O evento [MEEndOfPresentation](meendofpresentation.md) sinaliza que a reprodução atingiu o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="bcfc0-147">A sessão de mídia alterna automaticamente para o estado parado.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="bcfc0-148">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="bcfc0-148">MENewPresentation</span></span>

<span data-ttu-id="bcfc0-149">O evento [MENewPresentation](menewpresentation.md) sinaliza o início de uma nova apresentação.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="bcfc0-150">Os dados do evento são um ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para a nova apresentação.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="bcfc0-151">Em muitos casos, você não receberá esse evento.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="bcfc0-152">Se você fizer isso, use o ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para criar uma nova topologia de reprodução, conforme mostrado na [etapa 3: abrir um arquivo de mídia](step-3--open-a-media-file.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc0-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="bcfc0-153">Em seguida, enfileirar a nova topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="bcfc0-153">Then queue the new topology on the Media Session.</span></span>


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



<span data-ttu-id="bcfc0-154">Próximo: [etapa 6: controle de reprodução](step-6--control-playback.md)</span><span class="sxs-lookup"><span data-stu-id="bcfc0-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcfc0-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcfc0-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcfc0-156">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="bcfc0-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="bcfc0-157">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcfc0-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



