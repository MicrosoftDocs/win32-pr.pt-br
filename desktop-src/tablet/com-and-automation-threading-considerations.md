---
description: As seguintes considerações de Threading do Tablet PC são específicas para quando Component Object Model (COM) e a automação são usadas.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considerações de Threading COM e de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796245"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="296f1-103">Considerações de Threading COM e de automação</span><span class="sxs-lookup"><span data-stu-id="296f1-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="296f1-104">As seguintes considerações de Threading do Tablet PC são específicas para quando Component Object Model (COM) e a automação são usadas.</span><span class="sxs-lookup"><span data-stu-id="296f1-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="296f1-105">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="296f1-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="296f1-106">Aplicativos STA e MTA</span><span class="sxs-lookup"><span data-stu-id="296f1-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="296f1-107">InkCollector e InkOverlay</span><span class="sxs-lookup"><span data-stu-id="296f1-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="296f1-108">Coletores de eventos</span><span class="sxs-lookup"><span data-stu-id="296f1-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="296f1-109">Exceções nos manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="296f1-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="296f1-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="296f1-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="296f1-111">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="296f1-111">Thread Safety</span></span>

<span data-ttu-id="296f1-112">Exceto pelos controles [InkPicture](inkpicture-control.md) e [InkEdit](inkedit-control.md) , os objetos do Tablet PC são thread-safe e são marcados como ambos.</span><span class="sxs-lookup"><span data-stu-id="296f1-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="296f1-113">Ao ser marcado como ambos, eles podem ser executados em um STA (single-threaded apartment) ou em um MTA (multithreaded apartment).</span><span class="sxs-lookup"><span data-stu-id="296f1-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="296f1-114">O Windows Forms usa o modelo STA porque o Windows Forms se baseia em janelas nativas do Win32 que são inerentemente segmentadas em apartamento.</span><span class="sxs-lookup"><span data-stu-id="296f1-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="296f1-115">Aplicativos STA e MTA</span><span class="sxs-lookup"><span data-stu-id="296f1-115">STA and MTA Applications</span></span>

<span data-ttu-id="296f1-116">Se seu aplicativo for executado em um MTA ou usar o FTM (marshaled Threading) gratuito, você deverá escrever código de thread-safe; no entanto, ao fazer isso, você pode melhorar certos problemas de desempenho de manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="296f1-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="296f1-117">InkCollector e InkOverlay</span><span class="sxs-lookup"><span data-stu-id="296f1-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="296f1-118">Seu aplicativo não deve liberar sua referência final para o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) , destruindo, assim, o objeto diretamente do thread de tinta.</span><span class="sxs-lookup"><span data-stu-id="296f1-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="296f1-119">Em vez disso, o aplicativo deve liberar o **InkCollector** ou o objeto **InkOverlay** de um thread de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="296f1-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="296f1-120">**Cuidado:** Um aplicativo que está marcado como MTA ou usa o FTM, que permite chamadas diretas do thread de tinta para o apartamento do aplicativo, pode liberar sua referência final para o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) diretamente do thread de tinta; no entanto, isso causa falha de aplicativo irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="296f1-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="296f1-121">Coletores de eventos</span><span class="sxs-lookup"><span data-stu-id="296f1-121">Event Sinks</span></span>

<span data-ttu-id="296f1-122">Se seu aplicativo não estiver usando o FTM e um objeto e seu coletor de eventos forem criados em diferentes Apartments, o evento será executado no thread que está atendendo ao coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="296f1-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="296f1-123">Exceções nos manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="296f1-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="296f1-124">As exceções geradas de dentro de manipuladores de eventos do Tablet PC são consumidas e não são visíveis para o restante ou seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="296f1-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="296f1-125">Da mesma forma, os valores HRESULT não são propagados de manipuladores de eventos do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="296f1-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="296f1-126">Se um aplicativo que usa a camada COM gera uma exceção, o thread em segundo plano é encerrado e a exceção será perdida.</span><span class="sxs-lookup"><span data-stu-id="296f1-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="296f1-127">Nenhum manipulador de eventos adicional será chamado.</span><span class="sxs-lookup"><span data-stu-id="296f1-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="296f1-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="296f1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296f1-129">Exemplo de coletores de eventos do C++</span><span class="sxs-lookup"><span data-stu-id="296f1-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="296f1-130">Considerações gerais sobre Threading</span><span class="sxs-lookup"><span data-stu-id="296f1-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="296f1-131">Considerações sobre Threading de biblioteca gerenciada</span><span class="sxs-lookup"><span data-stu-id="296f1-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 



