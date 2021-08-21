---
description: Este tópico é a etapa 3 do tutorial Como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Etapa 3: Abrir um arquivo de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c198b07358ebbf5d8da591d75d44f4687b600f6bb387c4f55901974397308dc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012346"
---
# <a name="step-3-open-a-media-file"></a>Etapa 3: Abrir um arquivo de mídia

Este tópico é a etapa 3 do tutorial [Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no tópico Exemplo de reprodução [de sessão de mídia](media-session-playback-example.md).

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

1.  Chama **CPlayer::CreateSession** para criar uma nova instância da Sessão de Mídia. Consulte [Etapa 4: Criar a sessão de mídia.](step-4--create-the-media-session.md)
2.  Cria uma fonte de mídia da URL. O código completo para esta etapa é mostrado no tópico [Usando o Resolvedor de Origem](using-the-source-resolver.md).
3.  Chama [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obter o descritor de apresentação da fonte de mídia. O descritor de apresentação descreve cada fluxo no arquivo de origem.
4.  Cria a topologia de reprodução. O código para esta etapa é mostrado no tópico [Criando topologias de reprodução](creating-playback-topologies.md).
5.  Chama [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na Sessão de Mídia.

O [**método SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído de forma assíncrona. Quando ele é concluído, o método [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto CPlayer é chamado; consulte [Etapa 5: Manipular eventos de sessão de mídia.](step-5--handle-media-session-events.md)

Próximo: [Etapa 4: Criar a sessão de mídia](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



