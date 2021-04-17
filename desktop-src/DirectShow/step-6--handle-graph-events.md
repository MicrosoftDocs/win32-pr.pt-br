---
description: Este tópico é a etapa 6 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Etapa 6: manipular eventos de grafo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786964"
---
# <a name="step-6-handle-graph-events"></a>Etapa 6: manipular eventos de grafo

Este tópico é a etapa 6 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).

Quando o aplicativo cria uma nova instância do Gerenciador de gráfico de filtro, o aplicativo chama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Esse método registra a janela do aplicativo para receber eventos do gráfico de filtro.


```C++
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
```



O valor `WM_GRAPH_EVENT` é uma mensagem de janela privada. Sempre que o aplicativo receber essa mensagem, ele chamará o `DShowPlayer::HandleGraphEvent` método.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



O `DShowPlayer::HandleGraphEvent` método faz o seguinte:

1.  Chama [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) em um loop para obter todos os eventos em fila.
2.  Invoca uma função de retorno de chamada (*pfnOnGraphEvent*).
3.  Chama [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar os dados associados a cada evento.


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



O código a seguir mostra a função de retorno de chamada que é passada para `DShowPlayer::HandleGraphEvent` . A função manipula o número mínimo de eventos de grafo ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)e [**EC \_ userabort**](ec-userabort.md)); você pode expandir a função para manipular eventos adicionais.


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemplo de reprodução do DirectShow](directshow-playback-example.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Respondendo a eventos](responding-to-events.md)
</dt> </dl>

 

 



