---
description: Este tópico é a etapa 3 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Etapa 3: abrir um arquivo de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011942"
---
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="b68b3-103">Etapa 3: abrir um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="b68b3-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="b68b3-104">Este tópico é a etapa 3 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="b68b3-105">O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.</span><span class="sxs-lookup"><span data-stu-id="b68b3-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="b68b3-106">O `CPlayer::OpenURL` método abre um arquivo de mídia de uma URL.</span><span class="sxs-lookup"><span data-stu-id="b68b3-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
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

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="b68b3-107">Esse método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b68b3-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="b68b3-108">Chama **CPlayer:: CreateSession** para criar uma nova instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b68b3-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="b68b3-109">Consulte [a etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="b68b3-110">Cria uma fonte de mídia a partir da URL.</span><span class="sxs-lookup"><span data-stu-id="b68b3-110">Creates a media source from the URL.</span></span> <span data-ttu-id="b68b3-111">O código completo para essa etapa é mostrado no tópico [usando o resolvedor de origem](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="b68b3-112">Chama [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obter o descritor de apresentação da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="b68b3-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="b68b3-113">O descritor de apresentação descreve cada fluxo no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="b68b3-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="b68b3-114">Cria a topologia de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b68b3-114">Creates the playback topology.</span></span> <span data-ttu-id="b68b3-115">O código para essa etapa é mostrado no tópico [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="b68b3-116">Chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b68b3-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="b68b3-117">O método [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b68b3-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="b68b3-118">Quando concluído, o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto CPlayer é chamado; consulte [Step 5: tratar eventos de sessão de mídia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="b68b3-119">Em seguida: [etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="b68b3-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b68b3-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b68b3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b68b3-121">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="b68b3-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="b68b3-122">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b68b3-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



