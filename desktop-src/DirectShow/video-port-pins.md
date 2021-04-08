---
description: Pins de porta de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Pins de porta de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829047"
---
# <a name="video-port-pins"></a><span data-ttu-id="8481e-103">Pins de porta de vídeo</span><span class="sxs-lookup"><span data-stu-id="8481e-103">Video Port Pins</span></span>

<span data-ttu-id="8481e-104">Um dispositivo de captura com uma porta de vídeo de hardware pode usar as VPE (extensões de porta de vídeo) no Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="8481e-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="8481e-105">Nesse caso, o filtro de captura terá um PIN de porta de vídeo (VP).</span><span class="sxs-lookup"><span data-stu-id="8481e-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="8481e-106">Nenhum dado de vídeo viaja do VP do pino por meio do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="8481e-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="8481e-107">Em vez disso, os quadros de vídeo são produzidos em hardware e enviados diretamente para a memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="8481e-108">O VP de fixação permite que as mensagens de controle sejam enviadas ao hardware.</span><span class="sxs-lookup"><span data-stu-id="8481e-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="8481e-109">É importante conectar o VP de fixação, mesmo que seu aplicativo execute apenas a captura de arquivos sem visualização.</span><span class="sxs-lookup"><span data-stu-id="8481e-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="8481e-110">Se você deixar o PIN desconectado, o grafo não será executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="8481e-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="8481e-111">Isso é diferente dos Pins de visualização, que não precisam ser conectados.</span><span class="sxs-lookup"><span data-stu-id="8481e-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="8481e-112">Os diferentes renderizadores de vídeo do DirectShow fornecem suporte variado para os Pins de VP:</span><span class="sxs-lookup"><span data-stu-id="8481e-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="8481e-113">Renderizador de vídeo: Conecte o VP de fixação ao pino 0 no filtro de [mixer de sobreposição](overlay-mixer-filter.md) e conecte o filtro do mixer de sobreposição ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="8481e-114">VMR-7: Conecte o pino VP ao filtro do [Gerenciador de portas de vídeo](video-port-manager.md) e conecte o Gerenciador de portas de vídeo ao VMR-7.</span><span class="sxs-lookup"><span data-stu-id="8481e-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="8481e-115">VMR-9: você não poderá usar o VMR-9 se o dispositivo tiver um VP PIN, pois o Direct3D 9 não oferece suporte a portas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="8481e-116">Use o renderizador de vídeo ou o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="8481e-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="8481e-117">Para cenários de porta de vídeo, o mixer de sobreposição e o processador de vídeo são recomendados no Gerenciador de portas de vídeo e no VMR-7, pois nem todos os drivers dão suporte ao Gerenciador de portas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="8481e-118">Em geral, o mixer de sobreposição é a opção mais confiável para portas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="8481e-119">O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente o mixer de sobreposição, se houver um pino VP.</span><span class="sxs-lookup"><span data-stu-id="8481e-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="8481e-120">Se você estiver criando o grafo sem usar esse método, deverá verificar se há um PIN de porta de vídeo no filtro de captura e, se houver, conectá-lo ao filtro de mixer de sobreposição, como mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="8481e-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![Conectando um PIN de porta de vídeo ao filtro de mixer de sobreposição.](images/vidcap11.png)

<span data-ttu-id="8481e-122">Você pode usar o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para procurar um VP Pin no filtro de captura:</span><span class="sxs-lookup"><span data-stu-id="8481e-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="8481e-123">Depois de adicionar o mixer de sobreposição ao grafo, chame **FindPin** novamente para localizar o pino 0 no mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="8481e-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="8481e-124">O PIN 0 é sempre o primeiro PIN de entrada no filtro.</span><span class="sxs-lookup"><span data-stu-id="8481e-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="8481e-125">Conecte os dois Pins chamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="8481e-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="8481e-126">Em seguida, conecte o pino de saída do mixer de sobreposição ao filtro de processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8481e-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="8481e-127">Você pode ocultar o vídeo chamando os métodos [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::P UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) no Gerenciador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="8481e-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="8481e-128">Para sintonizadores de TV, o filtro de captura também pode ter uma porta de vídeo VBI PIN (PIN \_ Category \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="8481e-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="8481e-129">Nesse caso, conecte esse PIN ao filtro de [alocador de superfície VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="8481e-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="8481e-130">Para obter mais informações, consulte [exibindo legendas ocultas](viewing-closed-captions.md).</span><span class="sxs-lookup"><span data-stu-id="8481e-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8481e-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8481e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8481e-132">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="8481e-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="8481e-133">Usando o mixer de sobreposição na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8481e-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



