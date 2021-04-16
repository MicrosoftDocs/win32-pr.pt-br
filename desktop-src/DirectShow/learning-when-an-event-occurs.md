---
description: Aprendendo quando ocorre um evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Aprendendo quando ocorre um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500554"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="22e4e-103">Aprendendo quando ocorre um evento</span><span class="sxs-lookup"><span data-stu-id="22e4e-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="22e4e-104">Para processar eventos do DirectShow, um aplicativo precisa de uma maneira de descobrir quando os eventos estão aguardando na fila.</span><span class="sxs-lookup"><span data-stu-id="22e4e-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="22e4e-105">O Gerenciador de gráfico de filtro fornece duas maneiras de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="22e4e-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="22e4e-106">**Notificação de janela:** O Gerenciador de gráfico de filtro envia uma mensagem do Windows definida pelo usuário para uma janela de aplicativo sempre que houver um novo evento.</span><span class="sxs-lookup"><span data-stu-id="22e4e-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="22e4e-107">**Sinalização de evento:** O Gerenciador do grafo de filtro sinalizará um evento do Windows se houver eventos do DirectShow na fila e redefinirá o evento se a fila estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="22e4e-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="22e4e-108">Um aplicativo pode usar qualquer técnica.</span><span class="sxs-lookup"><span data-stu-id="22e4e-108">An application can use either technique.</span></span> <span data-ttu-id="22e4e-109">A notificação de janela é geralmente mais simples.</span><span class="sxs-lookup"><span data-stu-id="22e4e-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="22e4e-110">**Notificação de janela**</span><span class="sxs-lookup"><span data-stu-id="22e4e-110">**Window Notification**</span></span>

<span data-ttu-id="22e4e-111">Para configurar a notificação de janela, chame o método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) e especifique uma mensagem privada.</span><span class="sxs-lookup"><span data-stu-id="22e4e-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="22e4e-112">Os aplicativos podem usar números de mensagem no intervalo do \_ aplicativo do WM por meio do 0xBFFF como mensagens particulares.</span><span class="sxs-lookup"><span data-stu-id="22e4e-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="22e4e-113">Sempre que o Gerenciador de gráfico de filtro coloca uma nova notificação de evento na fila, ele posta essa mensagem na janela designada.</span><span class="sxs-lookup"><span data-stu-id="22e4e-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="22e4e-114">O aplicativo responde à mensagem de dentro do loop de mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="22e4e-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="22e4e-115">O exemplo de código a seguir mostra como definir a janela de notificação.</span><span class="sxs-lookup"><span data-stu-id="22e4e-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="22e4e-116">A mensagem é uma mensagem comum do Windows e é postada separadamente da fila de notificação de eventos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="22e4e-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="22e4e-117">A vantagem dessa abordagem é que a maioria dos aplicativos já implementa um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="22e4e-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="22e4e-118">Portanto, você pode incorporar a manipulação de eventos do DirectShow sem muito trabalho adicional.</span><span class="sxs-lookup"><span data-stu-id="22e4e-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="22e4e-119">O exemplo de código a seguir mostra uma estrutura de tópicos de como responder à mensagem de notificação.</span><span class="sxs-lookup"><span data-stu-id="22e4e-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="22e4e-120">Para obter um exemplo completo, consulte [respondendo a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="22e4e-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="22e4e-121">Como a notificação de eventos e o loop de mensagem são assíncronas, a fila pode conter mais de um evento no momento em que seu aplicativo responde à mensagem.</span><span class="sxs-lookup"><span data-stu-id="22e4e-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="22e4e-122">Além disso, os eventos podem, às vezes, ser limpos da fila se se tornarem inválidos.</span><span class="sxs-lookup"><span data-stu-id="22e4e-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="22e4e-123">Portanto, no código de manipulação de eventos, chame [**IAMMediaEvent:: getregular**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) até que ele retorne um código de falha, indicando que a fila está vazia.</span><span class="sxs-lookup"><span data-stu-id="22e4e-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="22e4e-124">Antes de liberar o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele a notificação de eventos chamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) com um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="22e4e-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="22e4e-125">Em seu código de processamento de eventos, verifique se o ponteiro **IMediaEventEx** é válido antes de chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="22e4e-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="22e4e-126">Essas etapas impedem um possível erro, no qual o aplicativo recebe a notificação de eventos depois de liberar o ponteiro **IMediaEventEx** .</span><span class="sxs-lookup"><span data-stu-id="22e4e-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="22e4e-127">**Sinalização de evento**</span><span class="sxs-lookup"><span data-stu-id="22e4e-127">**Event Signaling**</span></span>

<span data-ttu-id="22e4e-128">O Gerenciador de gráficos de filtro mantém um evento de redefinição manual que reflete o estado da fila de eventos.</span><span class="sxs-lookup"><span data-stu-id="22e4e-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="22e4e-129">Se a fila contiver notificações de eventos pendentes, o Gerenciador de gráfico de filtro sinalizará o evento de redefinição manual.</span><span class="sxs-lookup"><span data-stu-id="22e4e-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="22e4e-130">Se a fila estiver vazia, uma chamada para o método [**IMediaEvent:: Getuniforme**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) redefinirá o evento.</span><span class="sxs-lookup"><span data-stu-id="22e4e-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="22e4e-131">Um aplicativo pode usar esse evento para determinar o estado da fila.</span><span class="sxs-lookup"><span data-stu-id="22e4e-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="22e4e-132">A terminologia pode ser confusa aqui.</span><span class="sxs-lookup"><span data-stu-id="22e4e-132">The terminology can be confusing here.</span></span> <span data-ttu-id="22e4e-133">O evento de redefinição manual é o tipo de evento criado pela função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) do Windows; Ele não tem nada a ver com os eventos definidos pelo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="22e4e-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="22e4e-134">Chame o método [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) para obter um identificador para o evento de redefinição manual.</span><span class="sxs-lookup"><span data-stu-id="22e4e-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="22e4e-135">Aguarde até que o evento seja sinalizado chamando uma função como [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="22e4e-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="22e4e-136">Depois que o evento for sinalizado, chame [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obter o evento do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="22e4e-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="22e4e-137">O código de exemplo a seguir ilustra essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="22e4e-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="22e4e-138">Ele obtém o identificador de evento e aguarda em intervalos de 100 milissegundos para que o evento seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="22e4e-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="22e4e-139">Se o evento for sinalizado, **ele chamará GetEvent e** imprime o código do evento e os parâmetros do evento na janela do console.</span><span class="sxs-lookup"><span data-stu-id="22e4e-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="22e4e-140">O loop termina quando o evento [**EC \_ Complete**](ec-complete.md) ocorre, indicando que a reprodução foi concluída.</span><span class="sxs-lookup"><span data-stu-id="22e4e-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="22e4e-141">Como o grafo de filtro define ou redefine automaticamente o evento quando apropriado, o aplicativo não deve fazer isso.</span><span class="sxs-lookup"><span data-stu-id="22e4e-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="22e4e-142">Além disso, quando você libera o gráfico de filtro, o grafo de filtro fecha o identificador de evento, portanto, não use o identificador de evento após esse ponto.</span><span class="sxs-lookup"><span data-stu-id="22e4e-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
