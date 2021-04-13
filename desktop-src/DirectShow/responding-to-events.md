---
description: Este artigo descreve como responder a eventos que ocorrem em um grafo de filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Respondendo a eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500387"
---
# <a name="responding-to-events"></a><span data-ttu-id="bcec2-103">Respondendo a eventos</span><span class="sxs-lookup"><span data-stu-id="bcec2-103">Responding to Events</span></span>

<span data-ttu-id="bcec2-104">Este artigo descreve como responder a eventos que ocorrem em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="bcec2-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="bcec2-105">Como a notificação de eventos funciona</span><span class="sxs-lookup"><span data-stu-id="bcec2-105">How Event Notification Works</span></span>

<span data-ttu-id="bcec2-106">Enquanto um aplicativo do DirectShow está em execução, os eventos podem ocorrer no gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="bcec2-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="bcec2-107">Por exemplo, um filtro pode encontrar um erro de streaming.</span><span class="sxs-lookup"><span data-stu-id="bcec2-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="bcec2-108">Os filtros alertam o Gerenciador de gráfico de filtro enviando eventos, que consistem em um código de evento e dois parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="bcec2-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="bcec2-109">O código do evento indica o tipo de evento e os parâmetros de evento fornecem informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="bcec2-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="bcec2-110">O significado dos parâmetros depende do código do evento.</span><span class="sxs-lookup"><span data-stu-id="bcec2-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="bcec2-111">Para obter uma lista completa de códigos de eventos, consulte [códigos de notificação de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bcec2-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="bcec2-112">Alguns eventos são tratados silenciosamente pelo Gerenciador do grafo de filtro, sem que o aplicativo seja notificado.</span><span class="sxs-lookup"><span data-stu-id="bcec2-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="bcec2-113">Outros eventos são colocados em uma fila para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="bcec2-114">Dependendo do aplicativo, há vários eventos que talvez você precise manipular.</span><span class="sxs-lookup"><span data-stu-id="bcec2-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="bcec2-115">Este artigo se concentra em três eventos que são muito comuns:</span><span class="sxs-lookup"><span data-stu-id="bcec2-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="bcec2-116">O evento [**EC \_ Complete**](ec-complete.md) indica que a reprodução foi concluída normalmente.</span><span class="sxs-lookup"><span data-stu-id="bcec2-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="bcec2-117">O evento [**EC \_ userabort**](ec-userabort.md) indica que o usuário interrompeu a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bcec2-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="bcec2-118">Os renderizadores de vídeo enviam esse evento se o usuário fechar a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="bcec2-119">O [**evento \_ ERRORABORT do EC**](ec-errorabort.md) indica que um erro causou a interrupção da reprodução.</span><span class="sxs-lookup"><span data-stu-id="bcec2-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="bcec2-120">Usando a notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="bcec2-120">Using Event Notification</span></span>

<span data-ttu-id="bcec2-121">Um aplicativo pode instruir o Gerenciador de gráficos de filtro a enviar uma mensagem do Windows para uma janela designada sempre que um novo evento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="bcec2-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="bcec2-122">Isso permite que o aplicativo responda dentro do loop de mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="bcec2-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="bcec2-123">Primeiro, defina a mensagem que será enviada para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="bcec2-124">Os aplicativos podem usar números de mensagem no intervalo do \_ aplicativo do WM por meio do 0xBFFF como mensagens particulares:</span><span class="sxs-lookup"><span data-stu-id="bcec2-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="bcec2-125">Em seguida, consulte o Gerenciador do grafo de filtro para a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) e chame o método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :</span><span class="sxs-lookup"><span data-stu-id="bcec2-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="bcec2-126">Esse método designa a janela especificada (g \_ HWND) como o destinatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bcec2-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="bcec2-127">Chame o método depois de criar o gráfico de filtro, mas antes de executar o grafo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="bcec2-128">\_O WM GRAPHNOTIFY é uma mensagem comum do Windows.</span><span class="sxs-lookup"><span data-stu-id="bcec2-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="bcec2-129">Sempre que o Gerenciador de gráfico de filtro coloca um novo evento na fila de eventos, ele posta uma \_ mensagem do WM GRAPHNOTIFY na janela do aplicativo designada.</span><span class="sxs-lookup"><span data-stu-id="bcec2-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="bcec2-130">O parâmetro *lParam* da mensagem é igual ao terceiro parâmetro em [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="bcec2-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="bcec2-131">Esse parâmetro permite que você envie dados de instância com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bcec2-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="bcec2-132">O parâmetro *wParam* da mensagem da janela é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="bcec2-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="bcec2-133">Na função **WindowProc** do seu aplicativo, adicione uma instrução Case para a mensagem do WM \_ GRAPHNOTIFY:</span><span class="sxs-lookup"><span data-stu-id="bcec2-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="bcec2-134">Na função do manipulador de eventos, chame o método [**IMediaEvent:: getuniforme**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para recuperar eventos da fila:</span><span class="sxs-lookup"><span data-stu-id="bcec2-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="bcec2-135">O método [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera o código do evento e os dois parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="bcec2-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="bcec2-136">O quarto parâmetro **GetEvent** especifica o período de tempo a aguardar por um evento, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="bcec2-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="bcec2-137">Como o aplicativo chama esse método em resposta a uma \_ mensagem do WM GRAPHNOTIFY, o evento já está na fila.</span><span class="sxs-lookup"><span data-stu-id="bcec2-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="bcec2-138">Portanto, definimos o valor de tempo limite como zero.</span><span class="sxs-lookup"><span data-stu-id="bcec2-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="bcec2-139">A notificação de eventos e o loop de mensagem são assíncronas, portanto, a fila pode conter mais de um evento no momento em que seu aplicativo responde à mensagem.</span><span class="sxs-lookup"><span data-stu-id="bcec2-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="bcec2-140">Além disso, o Gerenciador de gráfico de filtro pode remover determinados eventos da fila, se eles se tornarem inválidos.</span><span class="sxs-lookup"><span data-stu-id="bcec2-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="bcec2-141">Portanto, você deve chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) até que ele retorne um código de falha, indicando que a fila está vazia.</span><span class="sxs-lookup"><span data-stu-id="bcec2-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="bcec2-142">Neste exemplo, o aplicativo responde ao [**EC \_ concluído**](ec-complete.md), ao [**EC \_ userabort**](ec-userabort.md)e ao [**EC \_ ERRORABORT**](ec-errorabort.md) invocando a função de limpeza definida pelo aplicativo, o que faz com que o aplicativo saia normalmente.</span><span class="sxs-lookup"><span data-stu-id="bcec2-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="bcec2-143">O exemplo ignora os dois parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="bcec2-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="bcec2-144">Depois de recuperar um evento, chame [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para todos os recursos gratuitos associados aos parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="bcec2-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="bcec2-145">Observe que um evento de [**\_ conclusão de EC**](ec-complete.md) não faz com que o grafo de filtro pare.</span><span class="sxs-lookup"><span data-stu-id="bcec2-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="bcec2-146">O aplicativo pode parar ou pausar o grafo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="bcec2-147">Se você parar o grafo, os filtros liberarão todos os recursos que estiverem mantendo.</span><span class="sxs-lookup"><span data-stu-id="bcec2-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="bcec2-148">Se você pausar o grafo, os filtros continuarão a manter os recursos.</span><span class="sxs-lookup"><span data-stu-id="bcec2-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="bcec2-149">Além disso, quando um processador de vídeo é pausado, ele exibe uma imagem estática do quadro mais recente.</span><span class="sxs-lookup"><span data-stu-id="bcec2-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="bcec2-150">Antes de liberar o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele a notificação de eventos chamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) com um identificador de janela **nulo** :</span><span class="sxs-lookup"><span data-stu-id="bcec2-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="bcec2-151">No manipulador de \_ mensagens GRAPHNOTIFY do WM, verifique o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) antes de chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span><span class="sxs-lookup"><span data-stu-id="bcec2-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="bcec2-152">Isso impede um possível erro que pode ocorrer se o aplicativo receber a notificação de eventos depois de liberar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="bcec2-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcec2-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcec2-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcec2-154">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcec2-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="bcec2-155">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcec2-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



