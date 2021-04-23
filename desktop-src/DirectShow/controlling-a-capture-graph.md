---
description: Controlando um grafo de captura
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlando um grafo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909044"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="33259-103">Controlando um grafo de captura</span><span class="sxs-lookup"><span data-stu-id="33259-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="33259-104">A interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) do Gerenciador de grafo de filtro tem métodos para executar, parar e pausar todo o grafo.</span><span class="sxs-lookup"><span data-stu-id="33259-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="33259-105">No entanto, se o grafo de filtro tiver fluxos de captura e visualização, provavelmente você desejará controlar os dois fluxos de forma independente.</span><span class="sxs-lookup"><span data-stu-id="33259-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="33259-106">Por exemplo, talvez você queira Visualizar o vídeo sem capturá-lo.</span><span class="sxs-lookup"><span data-stu-id="33259-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="33259-107">Você pode fazer isso por meio do método [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .</span><span class="sxs-lookup"><span data-stu-id="33259-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="33259-108">Esse método não funciona ao capturar para um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="33259-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="33259-109">Controlando o fluxo de captura</span><span class="sxs-lookup"><span data-stu-id="33259-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="33259-110">O código a seguir define o fluxo de captura de vídeo para ser executado por quatro segundos, iniciando um segundo após a execução do grafo:</span><span class="sxs-lookup"><span data-stu-id="33259-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="33259-111">O primeiro parâmetro especifica qual fluxo controlar, como um GUID de categoria de PIN.</span><span class="sxs-lookup"><span data-stu-id="33259-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="33259-112">O segundo parâmetro fornece o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="33259-112">The second parameter gives the media type.</span></span> <span data-ttu-id="33259-113">O terceiro parâmetro é um ponteiro para o filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="33259-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="33259-114">Para controlar todos os fluxos de captura no grafo, defina o segundo e terceiro parâmetros como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="33259-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="33259-115">Os próximos dois parâmetros definem os horários em que o fluxo será iniciado e interrompido, em relação à hora em que o grafo começa a ser executado.</span><span class="sxs-lookup"><span data-stu-id="33259-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="33259-116">Chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o grafo.</span><span class="sxs-lookup"><span data-stu-id="33259-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="33259-117">Até que você execute o grafo, o método **ControlStream** não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="33259-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="33259-118">Se o grafo já estiver em execução, as configurações entrarão em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="33259-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="33259-119">Os dois últimos parâmetros são usados para obter notificações de eventos quando o fluxo é iniciado e interrompido.</span><span class="sxs-lookup"><span data-stu-id="33259-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="33259-120">Para cada fluxo que você controla usando esse método, o grafo de filtro envia um par de eventos: o [**controle de fluxo do EC \_ \_ \_ foi iniciado**](ec-stream-control-started.md) quando o fluxo é iniciado e o [**controle de fluxo do EC \_ \_ \_ foi interrompido**](ec-stream-control-stopped.md) quando o fluxo é interrompido.</span><span class="sxs-lookup"><span data-stu-id="33259-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="33259-121">Os valores de **wStartCookie** e **wStopCookie** são usados como o segundo parâmetro de evento.</span><span class="sxs-lookup"><span data-stu-id="33259-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="33259-122">Portanto, *lParam2* no evento de início é igual a **wStartCookie** e *lParam2* no evento Stop é igual a **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="33259-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="33259-123">O código a seguir mostra como obter esses eventos:</span><span class="sxs-lookup"><span data-stu-id="33259-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="33259-124">O método **ControlStream** define alguns valores especiais para os horários de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="33259-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="33259-125">Label</span><span class="sxs-lookup"><span data-stu-id="33259-125">Label</span></span> | <span data-ttu-id="33259-126">Valor</span><span class="sxs-lookup"><span data-stu-id="33259-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="33259-127">Iniciar</span><span class="sxs-lookup"><span data-stu-id="33259-127">Start</span></span>                                  | <span data-ttu-id="33259-128">Stop</span><span class="sxs-lookup"><span data-stu-id="33259-128">Stop</span></span>                               |
| <span data-ttu-id="33259-129">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="33259-129">MAXLONGLONG</span></span> | <span data-ttu-id="33259-130">Nunca inicie este fluxo.</span><span class="sxs-lookup"><span data-stu-id="33259-130">Never start this stream.</span></span>               | <span data-ttu-id="33259-131">Não pare até que o grafo pare.</span><span class="sxs-lookup"><span data-stu-id="33259-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="33259-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="33259-132">**NULL**</span></span>    | <span data-ttu-id="33259-133">Inicie imediatamente quando o grafo for executado.</span><span class="sxs-lookup"><span data-stu-id="33259-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="33259-134">Pare imediatamente.</span><span class="sxs-lookup"><span data-stu-id="33259-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="33259-135">Por exemplo, o código a seguir interrompe o fluxo de captura imediatamente:</span><span class="sxs-lookup"><span data-stu-id="33259-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="33259-136">Embora você possa parar o fluxo de captura e reiniciá-lo mais tarde, isso criará uma lacuna nos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="33259-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="33259-137">Na reprodução, o vídeo aparecerá paralisado durante a lacuna (dependendo do formato de arquivo).</span><span class="sxs-lookup"><span data-stu-id="33259-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="33259-138">Controlando o fluxo de visualização</span><span class="sxs-lookup"><span data-stu-id="33259-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="33259-139">Para controlar o pino de visualização, chame **ControlStream** , mas defina o primeiro parâmetro como fixar a \_ Visualização da categoria \_ .</span><span class="sxs-lookup"><span data-stu-id="33259-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="33259-140">Isso funciona exatamente como faz para \_ a captura de categoria de PIN \_ , exceto que você não pode usar tempos de referência para especificar o início e parar, pois os quadros de visualização não têm carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="33259-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="33259-141">Portanto, você deve usar **NULL** ou MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="33259-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="33259-142">Use **NULL** para iniciar o fluxo de visualização:</span><span class="sxs-lookup"><span data-stu-id="33259-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="33259-143">Use MAXLONGLONG para interromper o fluxo de visualização:</span><span class="sxs-lookup"><span data-stu-id="33259-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="33259-144">Não importa se o fluxo de visualização é proveniente de um PIN de visualização no filtro de captura ou do filtro de "t" inteligente.</span><span class="sxs-lookup"><span data-stu-id="33259-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="33259-145">O método **ControlStream** funciona de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="33259-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="33259-146">Para Pins de porta de vídeo, no entanto, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="33259-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="33259-147">Nesse caso, outra abordagem é ocultar a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="33259-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="33259-148">Consulte o grafo para **IVideoWindow** e use o método [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar ou ocultar a janela.</span><span class="sxs-lookup"><span data-stu-id="33259-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="33259-149">Além disso, se você chamar [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) com o valor OAFALSE antes de executar o grafo, o filtro de processamento de vídeo ocultará a janela até que você especifique o contrário.</span><span class="sxs-lookup"><span data-stu-id="33259-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="33259-150">Por padrão, o renderizador de vídeo mostra a janela quando você executa o grafo.</span><span class="sxs-lookup"><span data-stu-id="33259-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="33259-151">Comentários sobre o controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="33259-151">Remarks about Stream Control</span></span>

<span data-ttu-id="33259-152">O comportamento padrão de um PIN é fornecer exemplos quando o grafo é executado.</span><span class="sxs-lookup"><span data-stu-id="33259-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="33259-153">Por exemplo, suponha que você chame **ControlStream** com a \_ captura de categoria de PIN \_ , mas não com a visualização de categoria de PIN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="33259-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="33259-154">Quando você executa o grafo, o fluxo de visualização será executado imediatamente, enquanto o fluxo de captura será executado em qualquer momento que você especificar em **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="33259-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="33259-155">Se você estiver capturando mais de um fluxo e enviando-os a um filtro Mux — por exemplo, se você estiver capturando áudio e vídeo em um arquivo AVI, você deve controlar ambos os fluxos em tandem.</span><span class="sxs-lookup"><span data-stu-id="33259-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="33259-156">Caso contrário, o filtro Mux pode bloquear a espera de um fluxo, pois ele tenta intercalar os dois fluxos.</span><span class="sxs-lookup"><span data-stu-id="33259-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="33259-157">Defina os mesmos horários de início e de término em todos os fluxos de captura antes de executar o grafo:</span><span class="sxs-lookup"><span data-stu-id="33259-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="33259-158">Internamente, o método **ControlStream** usa a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , que é exposta nos Pins do filtro de captura, no filtro de "t" inteligente (se presente) e possivelmente no filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="33259-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="33259-159">Você pode usar essa interface diretamente, em vez de chamar **ControlStream**, embora não haja nenhuma vantagem específica para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="33259-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33259-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33259-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33259-161">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="33259-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



