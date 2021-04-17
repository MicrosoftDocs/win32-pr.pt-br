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
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="fa9c6-103">Etapa 6: manipular eventos de grafo</span><span class="sxs-lookup"><span data-stu-id="fa9c6-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="fa9c6-104">Este tópico é a etapa 6 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="fa9c6-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="fa9c6-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="fa9c6-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="fa9c6-106">Quando o aplicativo cria uma nova instância do Gerenciador de gráfico de filtro, o aplicativo chama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="fa9c6-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="fa9c6-107">Esse método registra a janela do aplicativo para receber eventos do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-107">This method registers the application window to receive events from the filter graph.</span></span>


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



<span data-ttu-id="fa9c6-108">O valor `WM_GRAPH_EVENT` é uma mensagem de janela privada.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="fa9c6-109">Sempre que o aplicativo receber essa mensagem, ele chamará o `DShowPlayer::HandleGraphEvent` método.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="fa9c6-110">O `DShowPlayer::HandleGraphEvent` método faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fa9c6-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="fa9c6-111">Chama [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) em um loop para obter todos os eventos em fila.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="fa9c6-112">Invoca uma função de retorno de chamada (*pfnOnGraphEvent*).</span><span class="sxs-lookup"><span data-stu-id="fa9c6-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="fa9c6-113">Chama [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar os dados associados a cada evento.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


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



<span data-ttu-id="fa9c6-114">O código a seguir mostra a função de retorno de chamada que é passada para `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="fa9c6-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="fa9c6-115">A função manipula o número mínimo de eventos de grafo ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)e [**EC \_ userabort**](ec-userabort.md)); você pode expandir a função para manipular eventos adicionais.</span><span class="sxs-lookup"><span data-stu-id="fa9c6-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa9c6-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa9c6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9c6-117">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa9c6-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="fa9c6-118">Exemplo de reprodução do DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa9c6-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="fa9c6-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa9c6-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="fa9c6-120">Respondendo a eventos</span><span class="sxs-lookup"><span data-stu-id="fa9c6-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



