---
description: Este tópico é a etapa 3 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Etapa 3: criar o gráfico de filtro'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758670"
---
# <a name="step-3-build-the-filter-graph"></a>Etapa 3: criar o gráfico de filtro

Este tópico é a etapa 3 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).

A próxima etapa é criar um grafo de filtro para reproduzir o arquivo de mídia.

### <a name="opening-a-media-file"></a>Abrindo um arquivo de mídia

O `DShowPlayer::OpenFile` método abre um arquivo de mídia para reprodução. Esse método faz o seguinte:

1.  Cria um novo grafo de filtro (vazio).
2.  Chama [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar um filtro de origem para o arquivo especificado.
3.  Renderiza os fluxos no filtro de origem.


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a>Criando o Gerenciador de gráfico de filtro

O `DShowPlayer::InitializeGraph` método cria um novo grafo de filtro. Esse método faz o seguinte:

1.  Chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma nova instância do [Gerenciador de gráfico de filtro](filter-graph-manager.md).
2.  Consulta o Gerenciador de gráfico de filtro para as interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .
3.  Chama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) para configurar a notificação de eventos. Para obter mais informações, consulte [notificação de eventos no DirectShow](event-notification-in-directshow.md).


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a>Renderizando os fluxos

A próxima etapa é conectar o filtro de origem a um ou mais filtros de renderizador.

O `DShowPlayer::RenderStreams` método executa as etapas a seguir.

1.  Consulta o Gerenciador de gráfico de filtro para a interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .
2.  Adiciona um filtro de processador de vídeo ao grafo de filtro.
3.  Adiciona o [filtro de renderizador DirectSound](directsound-renderer-filter.md) ao grafo de filtro para dar suporte à reprodução de áudio. Para obter mais informações sobre como adicionar filtros ao grafo de filtro, consulte [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md).
4.  Enumera os Pins de saída no filtro de origem. Para obter mais informações sobre como enumerar Pins, consulte [enumerando Pins](enumerating-pins.md).
5.  Para cada PIN, chama o método [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) . Esse método conecta o pino de saída a um filtro de processador, adicionando filtros intermediários, se necessário (como decodificadores).
6.  Chamadas `CVideoRenderer::FinalizeGraph` para concluir a inicialização do processador de vídeo.
7.  Remove o filtro de [renderizador DirectSound](directsound-renderer-filter.md) se esse filtro não estiver conectado a outro filtro. Isso pode ocorrer se o arquivo de origem não contiver um fluxo de áudio.


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



Este é o código para a `RemoveUnconnectedRenderer` função, que é usado no exemplo anterior.


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a>Liberando o gráfico de filtro

Quando o aplicativo é encerrado, ele deve liberar o gráfico de filtro, conforme mostrado no código a seguir.


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



Em seguida: [etapa 4: Adicionar o processador de vídeo](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemplo de reprodução do DirectShow](directshow-playback-example.md)
</dt> <dt>

[Criando o grafo de filtro](building-the-filter-graph.md)
</dt> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> </dl>

 

 
