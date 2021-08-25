---
description: Este tópico é a etapa 4 do tutorial Como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Etapa 4: Criar a sessão de mídia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9c31d4c5e07abe8f088aad38fec9f91046a7d4338905dbd917de9d414fd4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847766"
---
# <a name="step-4-create-the-media-session"></a>Etapa 4: Criar a sessão de mídia

Este tópico é a etapa 4 do tutorial Como reproduzir arquivos de [mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no tópico Exemplo de reprodução [de sessão de mídia](media-session-playback-example.md).

O `CPlayer::CreateSession` cria uma nova instância da Sessão de Mídia.


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



Esse método executa as seguintes etapas:

1.  Chama `CPlayer::CloseSession` para fechar qualquer instância anterior da Sessão de Mídia.
2.  Chama [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma nova instância da Sessão de Mídia.
3.  Chama o [**método IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar o próximo evento da Sessão de Mídia. O primeiro parâmetro para **BeginGetEvent** é um ponteiro para o próprio objeto **CPlayer,** que impõe a interface [**IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)

A manipulação de eventos é descrita na etapa 5.

Próximo: [Etapa 5: Manipular eventos de sessão de mídia](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



