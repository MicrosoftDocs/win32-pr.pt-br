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
# <a name="step-3-open-a-media-file"></a>Etapa 3: abrir um arquivo de mídia

Este tópico é a etapa 3 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.

O `CPlayer::OpenURL` método abre um arquivo de mídia de uma URL.


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



Esse método executa as seguintes etapas:

1.  Chama **CPlayer:: CreateSession** para criar uma nova instância da sessão de mídia. Consulte [a etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md).
2.  Cria uma fonte de mídia a partir da URL. O código completo para essa etapa é mostrado no tópico [usando o resolvedor de origem](using-the-source-resolver.md).
3.  Chama [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obter o descritor de apresentação da fonte de mídia. O descritor de apresentação descreve cada fluxo no arquivo de origem.
4.  Cria a topologia de reprodução. O código para essa etapa é mostrado no tópico [criando topologias de reprodução](creating-playback-topologies.md).
5.  Chama [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na sessão de mídia.

O método [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído de forma assíncrona. Quando concluído, o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto CPlayer é chamado; consulte [Step 5: tratar eventos de sessão de mídia](step-5--handle-media-session-events.md).

Em seguida: [etapa 4: criar a sessão de mídia](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



