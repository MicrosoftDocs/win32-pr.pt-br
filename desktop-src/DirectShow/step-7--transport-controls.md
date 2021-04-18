---
description: Este tópico é a etapa 7 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Etapa 7: controles de transporte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810383"
---
# <a name="step-7-transport-controls"></a><span data-ttu-id="0fa5a-103">Etapa 7: controles de transporte</span><span class="sxs-lookup"><span data-stu-id="0fa5a-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="0fa5a-104">Este tópico é a etapa 7 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="0fa5a-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="0fa5a-106">A última etapa é adicionar controles de transporte (reproduzir, pausar e parar).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="0fa5a-107">Para executar o arquivo, chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


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



<span data-ttu-id="0fa5a-108">Para pausar, chame [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


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



<span data-ttu-id="0fa5a-109">Para parar, chame [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0fa5a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fa5a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fa5a-111">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="0fa5a-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0fa5a-112">Exemplo de reprodução do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0fa5a-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="0fa5a-113">Estados de filtro</span><span class="sxs-lookup"><span data-stu-id="0fa5a-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 



