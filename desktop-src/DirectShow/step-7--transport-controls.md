---
description: Este tópico é a etapa 7 do tutorial de reprodução de áudio/vídeo em DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Etapa 7: controles de transporte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8253efab566f5dc14a0d0210a26e84cb0a50113389d54b7a871d818a17296ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072410"
---
# <a name="step-7-transport-controls"></a>Etapa 7: controles de transporte

Este tópico é a etapa 7 do tutorial de [reprodução de áudio/vídeo em DirectShow](audio-video-playback-in-directshow.md). o código completo é mostrado no tópico [DirectShow exemplo de reprodução](directshow-playback-example.md).

A última etapa é adicionar controles de transporte (reproduzir, pausar e parar). Para executar o arquivo, chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



Para pausar, chame [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



Para parar, chame [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo em DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Exemplo de reprodução](directshow-playback-example.md)
</dt> <dt>

[Estados de filtro](filter-states.md)
</dt> </dl>

 

 



