---
description: Recuperando eventos
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recuperando eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370039"
---
# <a name="retrieving-events"></a><span data-ttu-id="5de74-103">Recuperando eventos</span><span class="sxs-lookup"><span data-stu-id="5de74-103">Retrieving Events</span></span>

<span data-ttu-id="5de74-104">O Gerenciador de gráfico de filtro expõe três interfaces que dão suporte à notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="5de74-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="5de74-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contém o método para filtros para postar eventos.</span><span class="sxs-lookup"><span data-stu-id="5de74-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="5de74-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contém métodos para aplicativos para recuperar eventos.</span><span class="sxs-lookup"><span data-stu-id="5de74-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="5de74-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) herda de e estende a interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="5de74-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="5de74-108">Os filtros postam notificações de eventos chamando o método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5de74-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="5de74-109">Uma notificação de evento consiste em um código de evento, que define o tipo de evento e dois parâmetros que fornecem informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="5de74-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="5de74-110">Dependendo do código do evento, os parâmetros podem conter ponteiros, códigos de retorno, tempos de referência ou outras informações.</span><span class="sxs-lookup"><span data-stu-id="5de74-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="5de74-111">Para obter uma lista completa de códigos de eventos e parâmetros, consulte [códigos de notificação de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5de74-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="5de74-112">Para recuperar um evento da fila, o aplicativo chama o método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5de74-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="5de74-113">Esse método é bloqueado até que haja um evento a ser retornado ou até que um tempo especificado decorra.</span><span class="sxs-lookup"><span data-stu-id="5de74-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="5de74-114">Supondo que haja um evento em fila, o método retorna com o código do evento e os dois parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="5de74-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="5de74-115">Depois de chamar **GetEvent**, um aplicativo sempre deve chamar o método [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar todos os recursos associados aos parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="5de74-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="5de74-116">Por exemplo, um parâmetro pode ser um valor **BSTR** que foi alocado pelo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5de74-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="5de74-117">O exemplo de código a seguir fornece uma descrição de como recuperar eventos da fila.</span><span class="sxs-lookup"><span data-stu-id="5de74-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="5de74-118">Para substituir o tratamento padrão do Gerenciador de grafo de filtro para um evento, chame o método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) com o código do evento como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5de74-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="5de74-119">Você pode restabelecer o tratamento padrão chamando o método [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) .</span><span class="sxs-lookup"><span data-stu-id="5de74-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="5de74-120">Se o grafo de filtro não executar nenhum tratamento padrão para o código de evento especificado, chamar esses métodos não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="5de74-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5de74-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5de74-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5de74-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="5de74-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



