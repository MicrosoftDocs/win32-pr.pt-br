---
description: Este tópico é a etapa 4 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Etapa 4: criar a sessão de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930216"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="dee54-103">Etapa 4: criar a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dee54-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="dee54-104">Este tópico é a etapa 4 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="dee54-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="dee54-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="dee54-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="dee54-106">O `CPlayer::CreateSession` cria uma nova instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dee54-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



<span data-ttu-id="dee54-107">Esse método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="dee54-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="dee54-108">Chama `CPlayer::CloseSession` para fechar qualquer instância anterior da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dee54-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="dee54-109">Chama [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma nova instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dee54-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="dee54-110">Chama o método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar o próximo evento da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dee54-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="dee54-111">O primeiro parâmetro para **BeginGetEvent** é um ponteiro para o próprio objeto **CPlayer** , que implents a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="dee54-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="dee54-112">A manipulação de eventos é descrita na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="dee54-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="dee54-113">Em seguida: [etapa 5: manipular eventos de sessão de mídia](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="dee54-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="dee54-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dee54-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dee54-115">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="dee54-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="dee54-116">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dee54-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



